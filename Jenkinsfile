pipeline {
  agent any
  stages {
    stage('Test REST') {
      parallel {
        stage('Test REST') {
          steps {
            sh 'echo "mvn test"'
          }
        }
        stage('Test SOAP NDC') {
          steps {
            sh 'echo "mvn test"'
          }
        }
        stage('Test SOAP CVC') {
          steps {
            sh 'echo "mvn test"'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        input(message: 'Continuar?', id: 'a', ok: 'b')
      }
    }
    stage('error') {
      steps {
        sh 'echo teste'
      }
    }
  }
}