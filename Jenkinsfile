pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    
    stage('Test') {
      steps {
        sh "${SNYK_HOME}/snyk-linux test"
        echo 'Testing...'
        snykSecurity(
          snykInstallation: 'snyk@latest',
          snykTokenId: '634e23f6-f926-4e18-9dd6-4c17ac5994bf',
          // place other parameters here
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
