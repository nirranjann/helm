pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building... now'
      }
    }
    stage('Test Firefox') {
      parallel {
        stage('Test Firefox') {
          steps {
            
           dir(build){
               sh('./getlatest.sh')
           }
            
            
          }
        }
        stage('Test Chrome') {
          steps {
            sh 'echo \'Testing Chrome\''
          }
        }
        stage('Test Edge') {
          steps {
            sh 'echo \'Testing Edge\''
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}
