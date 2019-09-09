pipeline {
  agent any
  stages {
    stage('Run Scripts') {
      steps {
        sh '''scripts/./hello.sh
'''
        sh 'scripts/./bye.sh'
      }
    }
  }
}