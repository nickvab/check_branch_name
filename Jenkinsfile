pipeline {
  agent any
  stages {
    stage('Check branch name') {
      steps {
        script { 
            if (env.BRANCH_NAME =~ /^(.*feature).*$/) {
                echo 'This is feature branch'
            } else {
                echo env.BRANCH_NAME
                echo 'This is NOT develop branch'
            }
        }
      }
    }
    stage('Check tag') {                                              
      steps {                                                       
        echo 'some steps here that should always be executed'
        script {                                                    
          if (env.TAG_NAME) {                                       
            echo "triggered by the TAG:"                                 
            echo env.TAG_NAME                                       
          } else {                                                  
            echo "triggered by branch, PR or ..."                              
          }                                                         
        }                                                           
      }                                                             
    }
  }
}


