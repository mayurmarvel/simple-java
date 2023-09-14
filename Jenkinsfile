pipeline {
    agent any

    stages {
        stage('Hello World') {
            steps {
                // Checkout code from the 'main' branch
                checkout([$class: 'GitSCM', 
                          branches: [[name: 'main']], // Adjust the branch name as needed
                          doGenerateSubmoduleConfigurations: false,
                          extensions: [],
                          userRemoteConfigs: [[url: 'https://github.com/mayurmarvel/simple-java']]])
                
                // Compile and run Java code on Windows
                bat 'javac HelloWorld.java'
                bat 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Hello World Job Succeeded!'
        }
    }
}
