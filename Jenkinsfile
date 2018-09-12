pipeline {
    agent {
        node {
            label 'docker-slave'
        } 
    }
    stages {

        stage('Clone repository') {
             agent {
                node {
                    label 'docker-slave'
                } 
            }
            steps {
                scm checkout
                echo "checkout"
            }
        }

        stage('Build') {
             agent {
                node {
                    label 'docker-slave'
                } 
            }
            steps {
                sh "docker build ."
                echo "build"
            }
        }
        stage('Test') {
             agent {
                node {
                    label 'docker-slave'
                } 
            }
            steps {
                sh "echo 'all is fine!'"
            }
        }
    }
}
