pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
		echo 'code validate'
		sh 'mvn validate'
            }
        }
        stage('Unit Test') {
            steps {
		echo 'code test'
		sh 'mvn test'
            }
        }
        stage('Sonar Analysis') {
            steps {
		 echo 'code analysis'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://34.250.132.236:9000 -Dsonar.login=d10497607a1b7a42cad0dc655668f26bd16fba32'
            }
        }
    }
}

