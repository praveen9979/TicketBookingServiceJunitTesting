pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                echo "rmdir  /s /q TicketBookingServiceJunitTesting"
                echo "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                echo "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                echo "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                echo "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                echo "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
