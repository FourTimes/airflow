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
                   def branch = "${env.GIT_BRANCH}" 
                   if [ branch == 'main' ] 
                   then 
                      echo "Building from ${branch} Branch"                   
                   else
                        echo "Building from non ${branch} Branch"
     
                }

         } 
      }
   }
}
