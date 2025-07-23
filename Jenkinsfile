pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/aliaa-elzahaby/iot-sre-java-app.git'
            }
        }
        stage('Build') {
    steps {
        dir('my-java-app') {
            bat 'mvn clean package -DskipTests'
              }
          }
        }

        stage('Test') {
            steps {
                dir('my-java-app') {
                    bat 'mvn test'
                }
            }
        }
        // Add deploy stages similarly with dir('my-java-app') if needed
    }
}
