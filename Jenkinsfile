pipeline {
    agent any
    environment {
        CI = 'true npm build'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
         stage('Deliver') {
            steps {
                sh "chmod +x -R ${env.WORKSPACE}"
                sh './Scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
            }
        }
    }
}