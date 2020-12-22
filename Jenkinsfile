pipeline {
    agent any
    
    environment{
        NEW_VERSION = '1..0.0'
        OLD_VERSION = '0.0.0'
    }
   
    stages {
        stage("init") {
            steps {
                script {
                    echo 'init stage'
                   //gv = load "script.groovy" 
                }
            }
        }
        stage("build") {
            steps {
                script {
                    echo 'build stage'
                    echo "new version ${NEW_VERSION}"
                    echo 'old version ${OLD_VERSION}'
                    //gv.buildApp()
                }
            }
        }
        
        stage("deploy") {
            steps {
                script {
                    echo 'deploy stage'
                    //gv.deployApp()
                }
            }
        }
    } 
    post {
        always{
            echo 'this is the post stage execution'
        }
    }
}
