pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''sudo -i
yum install -y git
cd /home/centos
git clone https://github.com/rosskopfsache/docker-build.git
cd docker-build
docker build .'''
      }
    }
  }
}