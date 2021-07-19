pipeline {
    agent any
    environment {
        FULL_PATH_BRANCH = "${sh(script:'git name-rev --name-only HEAD', returnStdout: true)}"
        GIT_BRANCH = FULL_PATH_BRANCH.substring(FULL_PATH_BRANCH.lastIndexOf('/') + 1, FULL_PATH_BRANCH.length())
    }
    stages {
        stage('Build if branch master'){
            steps {
                
                if ${env.GIT_BRANCH} == "main" {
                    echo "Building from ${env.GIT_BRANCH} Branch"
                } else {
                    echo "Building from ${env.GIT_BRANCH} Branch"
                }
        } 
    }
}
