pipeline {
    agent any
    tools{
        maven 'maven'
    }
    stages {
        stage ('Compile Stage') {

            steps {
                    sh 'mvn clean compile -Dsonar:sonar -Dsonar.url=http://35.185.76.118:9000'
            }
        }

        stage ('Testing Stage') {

            steps {
                    sh 'mvn test -Dsonar:sonar -Dsonar.url=http://35.185.76.118:9000'
            }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'mvn deploy -Dsonar:sonar -Dsonar.url=http://35.185.76.118:9000'
            }
        }
    }
}
