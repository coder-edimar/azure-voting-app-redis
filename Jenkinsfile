pipeline {
    agent any

    stages {
        
        stage('Verfiy Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
         stage('Docker Build') {
            steps {
                sh script: 'cd azure-vote/'
                sh script: 'docker build -t jenkins-pipeline -f DockerFile .'
                sh script:'cd..'
            }
        }
    }
}