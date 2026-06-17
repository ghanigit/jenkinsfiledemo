node {
    stage ("github")
    {
        git 'https://github.com/ghanigit/demoapp.git'
    }
    stage ("build")
    {
        bat 'mvn package'
    }
    stage("deploy")
    {
        deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: '966be318-54ed-4f5d-87bb-f5f42a8490e0', path: '', url: 'http://localhost:9090/')], contextPath: 'scriptedapp', war: '**/*.war'
    }
}
