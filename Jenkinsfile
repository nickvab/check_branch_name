pipeline {
  agent any
  stages {
    stage('Check branch name') {
      steps {
        script { 
            if (env.BRANCH_NAME == ^(.*develop).*$) {
                echo 'This is develop branch'
            } else {
                echo env.BRANCH_NAME
                echo 'This is NOT develop branch'
            }
        }
      }
    }
  }
}
