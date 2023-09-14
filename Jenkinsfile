pipeline {
    agent any

    stages {
        stage('Hello World') {
            steps {
                // Checkout code from the specified branch
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']], // Adjust the branch name as needed
                          doGenerateSubmoduleConfigurations: false,
                          extensions: [],
                          userRemoteConfigs: [[url: 'https://github.com/mayurmarvel/simple-java']]])

                // Execute the run.bat batch file
                bat 'run.bat'
            }
        }
    }

    post {
        success {
            echo 'Hello World Job Succeeded!'
        }
    }
}
