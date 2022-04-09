pipeline {
    agent any
    
    tools  {

        nodejs 'nodejs16'
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'npm install' 
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing..'
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying is awaiting'
                echo 'current working directory'
                sh 'pwd'
                withAWS(credentials: 's3deployment') {
                sh 'aws s3 ls'
                sh 'aws s3 ./build/* s3://www.mylab.html'
                
                        }
                
                    }

                }
        }
    }

