pipeline {
    agent any
     tools { 
         maven 'maven-3.5.4'  
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_6_3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_6_3') {
                    echo "Deployment Successful"
                    sh 'mvn deploy'
                }
            }
        }
    }
}
