pipeline {
    agent any
    environment {
        version = $BUILD_NUMBER
    }

    stages{
        stage("create zip file"){
            steps{
               
           sh 'zip middlewasreScript-$version.zip *.sh'  
            
            }
        }
        
    }
}
