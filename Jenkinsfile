pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
   

    stages{
        stage('build'){
            steps{
                echo 'this is the maven build job'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'this is the maven test job'
                sh 'mvn clean test'
            }
        }
        stage('package'){
            steps{
                echo 'this is the maven package job'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
<<<<<<< HEAD:Jenkinsfile
    
=======

  }
>>>>>>> 456c002d9a827223dbd63b0ec71f7678a755c6b8:Jenkinsfile-template
}
