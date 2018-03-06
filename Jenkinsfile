pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "Building...."'
      }
    }
    stage('deploy') {
      steps {
        echo 'Deploy'
      }
    }
    stage('Testes') {
      parallel {
        stage('Testes') {
          steps {
            echo 'Testesss'
          }
        }
        stage('SOAP NDC') {
          steps {
            sh 'echo aa'
          }
        }
        stage('REST') {
          steps {
            sh 'echo "OK"'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        build(job: '../Deploy/master', propagate: true)
      }
    }
  }
}