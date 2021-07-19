pipeline {
    agent any
    environment {
        FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"
        GIT_BRANCH = FULL_PATH_BRANCH.substring(FULL_PATH_BRANCH.lastIndexOf('/') + 1, FULL_PATH_BRANCH.length())
    }
    stages {
      stage('main') {   
           when { branch 'main' }

            steps {
                echo "main steps"
         } 
      }
      stage('dev') {   
           when { branch 'dev' }
            steps {
                echo "dev steps"
         } 
      }
   }
}
