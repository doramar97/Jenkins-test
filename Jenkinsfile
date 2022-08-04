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
        message "Which Version?"
        ok "Deploy"
        parameters {
            choice(name: 'APP_VERSION', choices: "v1.1\nv1.2\nv1.3", description: 'What to deploy?')
        }
      }
      steps {
        echo "Deploying ${APP_VERSION}."
      }
    }

    
    
    
  }
}
