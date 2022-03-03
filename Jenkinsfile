pipeline {
    agent any

    stages {
        stage('countinuous download') {
            steps {
                git 'https://github.com/boxfuse/boxfuse-sample-java-war-hello.git'
            }
        }
        stage('countinuous build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('countinuous deployment') {
            steps {
                sh 'cp target/hello-1.0.war /opt/apache-tomcat-9.0.59/webapps'
            }
        }
    }
}

