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
                sh script: 'docker images -a'
                sh script: 'cd azure-vote/'
                sh script: 'docker images -a'
                sh script: 'docker build -t jenkins-pipeline . docker images -a'
                sh script:'cd.. '
            }
        }
    }
}