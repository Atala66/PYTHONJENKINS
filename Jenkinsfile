pipeline {
  agent any
  stages {
    stage('version') {
      steps {
        bat 'python --version'
      }
    }
    stage('hello- world') {
      steps {
        echo ' Hello World '
      }
    }
    stage('clone') {
      steps {
        script {
              try {    // Attempt to clone the repository
                git 'https://github.com/Atala66/PYTHONJENKINS.git'
                echo 'Repository has been successfully cloned.'
               } catch (Exception e) {
                // Handle errors if the git command fails
                echo "Failed to clone repository: ${e.getMessage()}"
              // Optionally, you can add additional steps to handle the error, like sending notifications
               }
        }
      }
    }
  }
}