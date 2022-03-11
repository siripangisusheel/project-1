pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
		sh 'mvn validate'
            }
        }
        stage('Unit Test') {
            steps {
		sh 'mvn test'
            }
        }
        stage('Sonar Analysis') {
            steps {
		sh 'mvn sonar:sonar -Dsonar.host.url=http://34.250.132.236:9000 -Dsonar.login=d10497607a1b7a42cad0dc655668f26bd16fba32'
            }
        }
    }
}

