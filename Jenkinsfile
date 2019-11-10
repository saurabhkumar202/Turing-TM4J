pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'wget https://nodejs.org/dist/v6.11.4/node-v6.11.4-linux-x64.tar.xz'
        sh 'chown -R 1000 node-v6.11.4-linux-x64.tar.xz'
        sh 'tar -C /var/jenkins_home --strip-components 1 -xJf node-v6.11.4-linux-x64.tar.xz'
        sh 'cd /var/jenkins_home/bin'
        sh './npm install -g protractor@5.4.2'
        sh 'webdriver-manager update'
      }
    }

  }
}