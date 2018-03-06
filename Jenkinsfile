pipeline {
  agent any
  stages {
    stage('Test REST') {
      parallel {
        stage('Test REST') {
          steps {
            sh 'mvn test'
          }
        }
        stage('Test SOAP NDC') {
          steps {
            sh 'mvn test'
          }
        }
        stage('Test SOAP CVC') {
          steps {
            sh 'mvn test'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        input(message: 'Continuar?', id: 'a', ok: 'b')
      }
    }
    stage('') {
      steps {
        sh 'echo teste'
      }
    }
  }
}