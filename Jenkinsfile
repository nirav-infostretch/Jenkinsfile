pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://bitbucket.org/jpmobapp/im-mobile-app.git', changelog: true, branch: 'uat')
      }
    }

  }
}