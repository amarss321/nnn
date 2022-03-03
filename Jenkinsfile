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
                sh 'cp target/java-war-deploy-example-0.1-SNAPSHOT /opt/apache-tomcat-9.0.59/webapps'
            }
        }
    }
}

