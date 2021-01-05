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
                sh 'pwsh script: 'docker images -a''
                sh 'pwsh script: """
               cd azure-vote/
               docker images -a
               docker build -t jenkins-pipeline .
               docker images -a
               cd ..
            """'
            }
        }
    }
}