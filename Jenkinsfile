pipeline {
  agent any
  environment {
    ChromeDriverPath = 'C://ProfilePath/Driver'
  }
  stages {
    stage('Build and Test') {
      parallel {
        stage('Compile') {
          steps {
            echo 'Building the Java project'
          }
        }
        stage('Run Tests') {
          steps {
            echo 'Test the project after build'
            echo "Get the driver path ${ChromeDriverPath}"
          }
        }
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy the project in IIS server'
      }
    }
  }
}