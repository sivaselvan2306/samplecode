pipeline {
    agent any
  
    stages {
        stage('Destroy Infrastructure') {
            steps {
                withAWS(credentials: 'siva') {
                    sh 'terraform init'
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }
}


