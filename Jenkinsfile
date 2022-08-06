pipeline {
    agent any
     tools { 
         maven 'maven3.8.6'  
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven3.8.6') {
                    sh 'mvn clean compile'
                     echo "Compilation Successful"
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven3.8.6') {
                    sh 'mvn test'
                     echo "Testing Successful"
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven3.8.6') {
                    sh 'mvn deploy'
                     echo "Deployment Successful"
                }
            }
        }
    }
}
