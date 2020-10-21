pipeline {
    agent any
    stages {   
        stage('Clean') {
            steps {
                bat "mvn clean"
                echo 'Clean Ended ............'
            }
        }   
        stage('Test') {
            steps {
                bat "mvn test"
                echo 'Test Ended ............'
            }
        }   
        stage('Install') {
            steps {
                bat "mvn install"
                echo 'install Ended ............'
            }     
        }        
        stage('Notify') {
            steps {
                build "Email_Job"
                echo 'install Ended ............'
            }     
        }
    }
}
