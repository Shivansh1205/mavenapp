pipeline {
    agent any

    tools {
        jdk 'JDK'
        gradle 'gradle'   // 👈 use gradle instead of maven
    }

    stages {

        stage('Build') {
            steps {
                sh 'gradle clean build'
            }
        }

        stage('Run') {
            steps {
                sh 'gradle run'
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
