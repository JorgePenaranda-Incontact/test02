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
          Perms: {
            echo "Set permissions"
            sh 'chmod -R +x scripts/'
          },
          First: {
            echo "First Paralel task(001)"
            sh 'scripts/./hello.sh'
          },
          Second: {
            echo "Second Paralel task(002)"
            sh 'scripts/./bye.sh'
          },
          Download111: {
            sh 'scripts/./download.sh'
          },
          Download222: {
            sh 'scripts/./download2.sh'
          }
        )
      }
    }
  }
}