pipeline {
    agent any
    environment {
        TF_VAR_credentials = credentials('siva')
    }
    stages {
        stage('Destroy Infrastructure') {
            steps {
                withAWS(credentials: 'siva') {
                    sh 'terraform init'
                    sh 'terraform destroy -auto-approve'
                }
            }
        }
    }
}


