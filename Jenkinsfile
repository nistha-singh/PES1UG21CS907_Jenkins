pipeline{
  agent any 
  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS90-1'
        sh 'cd main\n g++ hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './main/output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
    post {
      failure {
        error 'Pipeline failed'
      }
    }
}
