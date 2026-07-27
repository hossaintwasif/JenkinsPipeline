pipeline {
  agent any
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

        stage('Test Logs') {
          steps {
            writeFile(file: 'LogTestFile.txt', text: 'This is an automation file logs')
          }
        }

      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy') {
          steps {
            echo 'Deploy the project in IIS server'
          }
        }

        stage('Artifacts') {
          steps {
            archiveArtifacts 'LogTestFile.txt'
          }
        }

      }
    }

  }
  environment {
    ChromeDriverPath = 'C://ProfilePath/Driver'
  }
}