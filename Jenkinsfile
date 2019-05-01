pipeline {
    agent any
    tools{
        maven 'maven'
    }
    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'mvn clean compile sonar:sonar -Dsonar.login=admin -Dsonar.password=admin -Dsonar.host.url=http://104.196.173.188:9000'
            }
        }

        stage ('Testing Stage') {

            steps {
                    sh 'mvn test'
            }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'mvn deploy sonar:sonar'
            }
        }
    }
}
