pipeline {
  agent {
    node {
      label 'ec2'
    }

  }
  stages {
    stage('Say Hello') {
      steps {
        sh '''echo \'Hello!\'
java --version'''
      }
    }

  }
}