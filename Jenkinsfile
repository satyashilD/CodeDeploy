pipeline {
    agent any 

     environment {
        AWS_ACCESS_KEY_ID     = credentials('jenkins-aws-secret-key-id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins-aws-secret-access-key')
    }      

    stages {
        stage('Git checkout') {
            steps {
                checkout scm    
            } 
        }
        stage('Build') {
            steps {
                 sh 'echo Hellp build'
            }
        }
        stage('Test') {
           steps {
                 sh 'echo hey test'
            }
        }
        stage('EKS deploy') {
            steps {
                 sh 'aws ec2 describe-instances --region ap-south-1'
            }
           
        }
    }
}
