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
        parallel(
          a: {
            echo "First Paralel task"
            sh 'scripts/./hello.sh'
          },
          b: {
            echo "Second Paralel task"
            sh 'scripts/./bye.sh'
          }
        )
      }
    }
  }
}