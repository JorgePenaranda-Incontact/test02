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
            echo "First Paralel task(01)"
            sh 'scripts/./hello.sh'
          },
          Second: {
            echo "Second Paralel task(02)"
            sh 'scripts/./bye.sh'
          }
        )
      }
    }
  }
}