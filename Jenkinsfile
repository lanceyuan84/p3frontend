pipeline {
    agent any
    
    tools  {

        nodejs 'nodejs16'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                //sh 'npm install' 
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing..'
                //sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                //echo 'Deploying is awaiting'
                echo 'current working directory'
                sh 'pwd'
                
                withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 's3deployment', usernameVariable: 'AWS_ACCESS_KEY_ID', passwordVariable: 'AWS_SECRET_ACCESS_KEY']]) {
              
                sh 'aws s3 ls'
                }

            }
        }
    }
}
