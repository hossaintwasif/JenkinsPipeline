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
}