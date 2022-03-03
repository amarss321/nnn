pipeline {
    agent any

    stages {
        stage('countinuous download') {
            steps {
                git 'https://github.com/daticahealth/java-war-deploy-example.git'
            }
        }
        stage('countinuous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('countinuous deployment') {
            steps {
                sh 'sshpass -p "nath" scp target/java-war-deploy-example-0.1-SNAPSHOT nath@172.17.0.4:/opt/apache-tomcat-9.0.59/webapps'
            }
        }
    }
}

