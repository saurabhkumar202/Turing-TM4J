pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'wget https://nodejs.org/dist/v6.11.4/node-v6.11.4-linux-x64.tar.xz'
        sh 'chown -R 1000 node-v6.11.4-linux-x64.tar.xz'
        sh 'tar -C /var/jenkins_home --strip-components 1 -xJf node-v6.11.4-linux-x64.tar.xz'
        sh 'cd /var/jenkins_home/bin && ./node npm install -g protractor@5.4.2'
        sh 'cd /var/jenkins_home/lib/node_modules/protractor/node_modules/webdriver-manager/   /var/jenkins_home/bin/node ./bin/webdriver-manager update'
      }
    }

  }
}