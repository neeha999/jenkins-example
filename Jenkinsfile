pipeline {
    agent any
    tools{
        maven 'maven'
        sonar scanner 'sonar'
    }
    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'mvn clean compile sonar:sonar'
            }
        }

        stage ('Testing Stage') {

            steps {
                    sh 'mvn test sonar:sonar'
            }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'mvn deploy sonar:sonar'
            }
        }
    }
}
