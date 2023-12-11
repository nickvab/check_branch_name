pipeline {
  agent any
  stages {
    stage('Check branch name') {
      steps {
        script { 
          def BRANCH = sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
          echo BRANCH
            if (env.BRANCH_NAME != 'master') {
                echo env.BRANCH_NAME
                echo 'This is NOT master branch'
            } else {
                echo 'This is master branch'
            }
        }
      }
    }
  }
}
