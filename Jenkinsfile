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
        stage('Deploye')
        {
            steps{
                bat 'cd "C:/WINDOWS/system32/config/systemprofile/.m2/repository/dev/wael/jaxRS/0.0.1-SNAPSHOT/"'
                bat 'copy jaxRS-0.0.1-SNAPSHOT.war "C:/Program Files/apache-tomcat-9.0.34/webapps" /y'
                echo 'Deploy  ............'
            }
        }
        stage('Notify') {
            steps {
                build "Email_Job"
                echo 'Notify Ended ............'
            }     
        }
    }
}
