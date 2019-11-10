pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'wget https://nodejs.org/dist/v6.11.4/node-v6.11.4-linux-x64.tar.xz'
        sh 'chown -R 1000 node-v6.11.4-linux-x64.tar.xz'
        sh 'tar -C /var/jenkins_home --strip-components 1 -xJf node-v6.11.4-linux-x64.tar.xz'
        sh 'cd /var/jenkins_home/bin && ./node npm install -g protractor@4.0.14'
        sh 'cd /var/jenkins_home/lib/node_modules/protractor/node_modules/webdriver-manager &&  /var/jenkins_home/bin/node ./bin/webdriver-manager update'
        sh 'wget http://www.slimjetbrowser.com/chrome/lnx/chrome64_55.0.2883.75.deb && mv /opt/google/chrome/google-chrome /opt/google/chrome/mychrome && echo '#!/usr/bin/env bash' > /google-chrome && echo 'exec /opt/google/chrome/mychrome --no-sandbox --disable-gpu $@' >> /google-chrome && mv /google-chrome /opt/google/chrome/google-chrome && chmod +x /opt/google/chrome/google-chrome'
      }
    }

  }
}