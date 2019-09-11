pipeline {
  agent any
  stages {
    stage('Download(-consecutively-)') {
      steps {
        sh 'chmod -R +x scripts/'
        sh 'scripts/./download.sh'
        sh 'scripts/./download2.sh'
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
            echo "Paralel Download(0.1)"
            sh 'scripts/./hello.sh'
            sh 'scripts/./download.sh'
          },
          Second: {
            echo "Paralel Download(0.2)"
            sh 'scripts/./download2.sh'
            sh 'scripts/./bye.sh'
          }
        )
      }
    }
  }
}