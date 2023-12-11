pipeline {
  agent any
  stages {
    stage('Check branch name') {
      steps {
        script { 
            if (env.BRANCH_NAME == '^(.*develop).*$') {
                echo env.BRANCH_NAME
                echo 'This is master branch'
            } else {
                echo 'This is NOT master branch'
            }
        }
      }
    }
  }
}
