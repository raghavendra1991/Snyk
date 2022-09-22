pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    
    stage('Test') {
      environment {
        SNYK_HOME = tool 'Synk'
      }
      steps {
        sh "${SNYK_HOME}/snyk-linux test"
        echo 'Testing...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
