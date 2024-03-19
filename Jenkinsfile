pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the Java code
                sh 'javac HelloWorld.java'
            }
        }
        stage('Test') {
            steps {
                // No specific tests in this example
            }
        }
        stage('Package') {
            steps {
                // Create a JAR file
                sh 'jar cvfe HelloWorld.jar HelloWorld *.class'
            }
        }
        stage('Deploy') {
            steps {
                // Copy files to deployment directory
                sh 'mkdir -p deploy'
                sh 'cp HelloWorld.jar deploy/'
                sh 'cp HelloWorld.jar deploy/'
                
                
                // Your deployment step here, it could be deploying to Azure App Service, etc.
                // For Azure App Service, you'd need to upload the deployment directory.
                // Example: sh 'az webapp deployment source config-zip --resource-group RESOURCE_GROUP_NAME --name APP_NAME --src deploy/'
            }
        }
    }
}
