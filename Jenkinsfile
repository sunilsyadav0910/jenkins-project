pipeline {
    agent any

    environment {                                      
        accessKeyVariable = credentials('AWS_ACCESS_KEY_ID')
        secretKeyVariable = credentials('AWS_SECRET_ACCESS_KEY')
        
    }
    
    stages {
        stage("AWS Demo") {
            steps {
                    sh "packer init aws-ami-v1.pkr.hcl"
                    sh "packer build aws-ami-v1.pkr.hcl"
                }
            }
        }
    }
