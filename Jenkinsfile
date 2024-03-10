pipeline {
  agent any
  stages {
    stage('Build') { // corrected the spelling
      steps {
        build 'PES2UG21CS484-1'
        sh 'g++ W.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') { // corrected the spacing and typo
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
