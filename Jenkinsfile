pipeline {
    agent any
     tools { 
         maven 'maven3.8.6'  
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_8_6') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_8_6') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_8_6') {
                    echo "Deployment Successful"
                    sh 'mvn deploy'
                }
            }
        }
    }
}
