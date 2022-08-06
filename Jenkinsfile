pipeline {
    agent any
     tools { 
        maven 'Maven 3.3.9' 
        jdk 'jdk8' 
    }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_3_9') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_3_9') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_3_9') {
                    echo "Deployment Successful"
                    sh 'mvn deploy'
                }
            }
        }
    }
}
