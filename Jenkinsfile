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
          First: {
            echo "First Paralel task"
            sh 'scripts/./hello.sh'
          },
          Second: {
            echo "Second Paralel task"
            sh 'scripts/./bye.sh'
          }
        )
      }
    }
  }
}