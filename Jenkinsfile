pipeline {
  agent any
  stages {
    stage('Run Scripts(consecutively)') {
      steps {
        sh '''scripts/./hello.sh
'''
        sh 'scripts/./bye.sh'
      }
    }
    stage('Run Scripts(Paralel)') {
      steps {
        sh 'scripts/./hello.sh'
      }
    }
  }
}