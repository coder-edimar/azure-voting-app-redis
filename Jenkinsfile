pipeline {
    agent any

    stages {
        stage('Initialize'){
         def dockerHome = tool 'myDocker'
            env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
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