pipeline {
  agent any
  stages {
    stage('Check branch name') {
      steps {
        script { 
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
