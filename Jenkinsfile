pipeline {
  agent any
  stages {
    stage('Test REST') {
      parallel {
        stage('Test REST') {
          parallel {
           stage('Test REST AA') {
             steps {
               sh 'echo "mvn test"'
             }
           }
           stage('Test REST BB') {
             steps {
               sh 'echo "mvn test"'
             }
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
    stage('Deploy?') {
      steps {
        input(message: 'Continuar?', id: 'a', ok: 'SIM')
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo teste'
      }
    }
  }
}
