pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        checkout scm
        sh 'sudo apt-get update && sudo apt-get install -y nano bzip2 ffmpeg xvfb ca-certificates openjdk-8-jre-headless xz-utils vim sudo wget x11vnc'
        sh 'wget https://nodejs.org/dist/v6.11.4/node-v6.11.4-linux-x64.tar.xz && 	tar -C /usr --strip-components 1 -xJf node-v6.11.4-linux-x64.tar.xz'
        sh 'npm install -g protractor@5.4.2'
        sh 'webdriver-manager update'
      }
    }

  }
}
