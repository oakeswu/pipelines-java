pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo "mavenTest"'
            waitUntil() {
              sh 'echo "mSonar"'
            }

          }
        }

        stage('Build') {
          steps {
            sh 'echo "build"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }

  }
}