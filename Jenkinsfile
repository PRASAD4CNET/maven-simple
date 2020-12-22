pipeline {
    agent any
   
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
