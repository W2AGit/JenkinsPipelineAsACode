pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Pipeline Build success'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Pipeline Deploy success'
            }
        }
        stage('Test') {
            steps {
                echo 'Pipeline Test success'
            }
            post { 
             always { 
                junit allowEmptyResults: true, testResults: 'target/surefire-reports/*.xml' 
        }
    }
        }
        stage('Release') {
            steps {
                echo 'Pipeline ReleaseDeploy success'
            }
        }
        
    }
}
