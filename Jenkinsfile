pipeline {
  agent any
  stages {
    stage('Check branch name') {
      steps {
        script { 
          def BRANCH_NAME = sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
          echo BRANCH_NAME
            if (BRANCH_NAME != 'master') {
                echo {env.BRANCH_NAME}
                echo 'This is NOT master branch'
            } else {
                echo 'This is master branch'
            }
        }
      }
    }
  }
}
