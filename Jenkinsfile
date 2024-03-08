pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        build 'PES1UG21CS429-1'
        sh 'g++ main/hello.cpp -o output'
        echo "Hey, I'm Pranav Bookanakere"
      }
    }
    stage ('Test') {
      steps {
        sh './output'
        echo "Hey, I'm TEST"
      }
    }
    stage ('Deploy') {
      steps {
        echo 'deploy'
        echo "Hey. I'm DEPLOY"
      }
    }
  }
  post {
    failure {
      error 'Pipeline failed'
      echo 'Oops'
    }
  }
}
