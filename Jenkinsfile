pipeline {
  agent any
  environment {
      MY_NAME = 'DOR'
   }
  stages {
    stage('Say Hello') {
      steps {
        sh 'echo "Hello ${MY_NAME}!"'
      }
    }
     stage('Deploy') {
      input {
        message "Should we continue?"
      }
      steps {
        echo "Continuing with deployment"
      }
    }

  }
}
