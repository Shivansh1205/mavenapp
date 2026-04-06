pipeline {
    agent any

    tools {
        jdk 'JDK'
        maven 'maven'
    }

    stages {

        stage('Build') {
            steps {
                dir('mavenapp') {   // 👈 FIX HERE
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Test') {
            steps {
                dir('mavenapp') {
                    sh 'mvn test'
                }
            }
        }

        stage('Package') {
            steps {
                dir('mavenapp') {
                    sh 'mvn package'
                }
            }
        }
    }

    post {
        success {
            echo 'Build Successful ✅'
        }
        failure {
            echo 'Build Failed ❌'
        }
    }
}
