pipeline {
  agent any
  stages {
    stage('build') {
      steps {
       checkout scm
       sh "apt-get update && apt-get install -y nano bzip2 ffmpeg xvfb ca-certificates openjdk-8-jre-headless xz-utils vim sudo wget x11vnc \"
        sh  "sed -i 's/securerandom\.source=file:\/dev\/random/securerandom\.source=file:\/dev\/urandom/' ./usr/lib/jvm/java-8-openjdk-amd64/jre/lib/security/java.security"
        sh "wget https://nodejs.org/dist/v6.11.4/node-v6.11.4-linux-x64.tar.xz && 	tar -C /usr --strip-components 1 -xJf node-v6.11.4-linux-x64.tar.xz \"
        sh "npm install -g protractor@5.4.2"
        sh "webdriver-manager update"
      }
    }

  }
}
