pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('Maven Test') {
          steps {
            bat(script: 'mvn clean test', label: 'Maven Test')
          }
        }

        stage('Maven Version') {
          steps {
            bat(script: 'mvn --version', label: 'Maven Version ')
          }
        }

      }
    }

  }
}