pipeline {pipeline {
    agent  {
    }

    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
                sh 'npm run build --verbose'
                sh 'CI=true npm build' 
            }
        }
    }
}
