pipeline {
    agent any
    
    tools  {

        nodejs '16.0.0'
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
            }
        }
    }
}
