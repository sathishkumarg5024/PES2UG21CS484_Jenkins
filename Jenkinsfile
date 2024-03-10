
pipeline {
  agent any
  stages {
    stage('Build') {
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
