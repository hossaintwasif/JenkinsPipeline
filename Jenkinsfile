pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building the Java project'
          }
        }

        stage('Test') {
          steps {
            echo 'Test the project after build'
            echo '"Get the driver path ${ChromeDriverPath}"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy the project in llS server'
      }
    }

  }
  environment {
    ChromeDriverPath = 'C://ProfilePath/Driver'
  }
}