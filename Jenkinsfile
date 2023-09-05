pipeline {
    agent any
    environment {
        version = "${BUILD_NUMBER}"
    }

    stages{
        stage("create zip file"){
            steps{
               
           sh 'zip middlewasreScript-$version.zip *.sh'  
            
            }
        }
        stage("upload to nexus")
        steps{
            sh 'curl --upload-file middlewasreScript-$version.zip -u admin:devops -v http://198.58.119.40:8081/repository/prof-repo/
        }
    }
}
