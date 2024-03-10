pipeline {
  agent any
  stages {
    stage('Bui1d') {
      steps {
      build 'PES2UG21CS484-1'
      sh 'g++ w.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
        
      }
    }
    stage( 'Deploy') {
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
