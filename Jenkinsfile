pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                sh "rm -rf TicketBookingServiceJunitTesting"
                sh "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                sh "mvn clean"
            }
        }
        stage('install') {
            steps {
                sh "mvn install"
            }
        }
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
        stage('package') {
            steps {
                sh "mvn package"
            }
        }
    }
}
