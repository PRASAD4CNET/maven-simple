pipeline {
    agent any
    
    parameters{
        string(name: 'version',defaultValue: '',description: 'version to deploy on prod')
        choice(name: 'VERSION',choices:['1.1.0','1.2.0','1.3.0'],description:'')
        booleanParam(name:'executetestes',defaultValue:false,description:'')
    }
    
    environment{
        NEW_VERSION = '1..0.0'
        OLD_VERSION = '0.0.0'
    }
   
    stages {
        stage("init") {
            when{
                expression{
                    params.executeTests
                }
            }
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
                    echo "new version ${NEW_VERSION}" //displays the version 1.0.0
                    echo 'old version ${OLD_VERSION}' //displays as it is ${OLD_Version}
                   
                    //gv.buildApp()
                }
            }
        }
        
        stage("deploy") {
            steps {
                script {
                    echo 'deploy stage'
                    echo "deploying version ${params.VERSION}"
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
