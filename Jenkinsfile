pipeline {
  agent any
  stages {
    stage('Find IP') {
      parallel {
        stage('Find IP') {
          steps {
            sh 'ip a'
          }
        }

        stage('Create and Validate file') {
          steps {
            writeFile(file: 'config.conf', text: 'This is a configuration file for our application.')
            fileExists 'config.conf'
          }
        }

      }
    }

    stage('Development') {
      steps {
        echo 'This step prints to development'
      }
    }

    stage('Test') {
      steps {
        echo ' This step prints to test'
      }
    }

    stage('Production') {
      steps {
        echo 'This step prints to production'
      }
    }

  }
}