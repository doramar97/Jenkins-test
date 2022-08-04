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
    
    //This stage is wating for user input.
     stage('Deploy') {
       options {
        timeout(time: 30, unit: 'SECONDS') 
      }
      input {
        message "Should we continue?"
      }
      steps {
        echo "Continuing with deployment"
      }
    }

    
    
    
  }
}
