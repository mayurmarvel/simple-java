pipeline {
    agent any
    
    stages {
        stage('Hello World') {
            steps {
                // Checkout code from Git
                checkout scm
                
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
