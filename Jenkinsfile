pipiline {
    agent none
    stages {
        stage ('Build') {
            agent any
        }

        stage ('Test on Linux') {
            agent {
                label 'linux'
            }
            steps {
                sh 'apt-get install -y python'
                sh 'python testPython.py'
                echo 'Test Linux'
            }
        }

        stage ('Test on Windows') {
            agent {
                label 'windows'
            }
            steps {
                echo 'Test Windows'
            }
        }
    }
}
