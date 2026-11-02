pipeline {
    agent any

    stages {
        stage('Check Linux') {
            steps {
                sh '''
                    echo "Hello from Jenkins!"
                    echo "Current user:"
                    whoami
                    echo "Hostname:"
                    hostname
                    echo "Ubuntu version:"
                    cat /etc/os-release
                '''
            }
        }

        stage('Check Disk and Memory') {
            steps {
                sh '''
                    echo "Disk usage:"
                    df -h /
                    echo "Memory usage:"
                    free -h
                '''
            }
        }

        stage('Build Successful') {
            steps {
                echo 'Ubuntu Linux lab pipeline completed!'
            }
        }
    }
}