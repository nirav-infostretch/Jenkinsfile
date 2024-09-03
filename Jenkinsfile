pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://bitbucket.org/jpmobapp/im-mobile-app.git', changelog: true, branch: 'uat', credentialsId: 'rahul_credentials')
      }
    }

    stage('Install dependencies') {
      steps {
        echo 'Install dependencies'
      }
    }

    stage('Build Android App') {
      parallel {
        stage('Build Android App') {
          steps {
            echo 'Build Android App'
            echo 'Upload'
          }
        }

        stage('Pod') {
          steps {
            echo 'Pod'
          }
        }

      }
    }

    stage('Build iOS App') {
      steps {
        echo 'Build iOS App'
      }
    }

    stage('Upload iOS to Firebase') {
      steps {
        echo 'Upload iOS to Firebase'
      }
    }

    stage('Unit Test') {
      parallel {
        stage('Unit Test') {
          steps {
            echo 'Unit Test'
          }
        }

        stage('Sonar') {
          steps {
            echo 'Sonar'
          }
        }

      }
    }

  }
}