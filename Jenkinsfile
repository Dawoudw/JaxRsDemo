pipeline {
    agent any

    stages {   
        stage('Clean') {
            steps {
                bat "mvn clean -f JaxRsDemo"
                echo 'Clean Ended ............'
            }
        }   
        stage('Test') {
            steps {
                bat "mvn test -f JaxRsDemo"
                echo 'Test Ended ............'
            }
        }   
        stage('Install') {
            steps {
                bat "mvn install -f JaxRsDemo"
                echo 'install Ended ............'
            }     
        }     
        stage('Deploy') {
            steps {
                bat 'Xcopy /E  "C:/WINDOWS/system32/config/systemprofile/.m2/repository/dev/wael/jaxRS/0.0.1-SNAPSHOT/jaxRS-0.0.1-SNAPSHOT.war"  "C:/Program Files/apache-tomcat-9.0.34/webapps"'
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
