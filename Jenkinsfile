pipeline {
    agent {
        docker {
            image 'maven:3.9.9-openjdk-21'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
