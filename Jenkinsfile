pipeline {
    agent any

    stages {
        stage('CompileJob') {
            steps {
		echo 'code validate'
		sh 'mvn validate'
            }
        }
        stage('UnitTest') {
            steps {
		echo 'code test'
		sh 'mvn test'
            }
        }
        stage('SonarAnalysis') {
            steps {
		 echo 'code analysis'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://54.89.253.207:9000 -Dsonar.login=96c6cc5ddabeb96383db283c87b768f2132e0bc7'
            }
        }
    }
}

