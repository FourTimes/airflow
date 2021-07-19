pipeline {
    agent any
    environment {
        FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"
        GIT_BRANCH = FULL_PATH_BRANCH.substring(FULL_PATH_BRANCH.lastIndexOf('/') + 1, FULL_PATH_BRANCH.length())
    }
    stages {
        stage('Build if branch master'){
            steps {
              script { 
                def gender = "${env.GIT_BRANCH}"
                if (gender == 'main') {
                        echo "Building from ${gender} Branch"                   
                   } else {
                        echo "Building from ${gender} Branch"
                        echo "none main branch"
                 }
             }
         } 
      }
   }
}
