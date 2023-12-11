pipeline {
  agent any
  }
  stages {
    stage('Check branch name') {
      steps {
        script { 
          def BRANCH_NAME = sh(returnStdout: true, script: 'git rev-parse --abbrev-ref HEAD').trim()
          echo ${BRANCH_NAME}
            if (env.BRANCH_NAME != 'master') {
                echo ${BRANCH_NAME}
                echo 'This is NOT master branch'
            } else {
                echo ${env.BRANCH_NAME}
                echo 'This is master branch'
            }
        }
      }
    }
    stage('Test') {
      steps {
        echo ${BRANCH_NAME}
      }
    }
  }
  }
}
