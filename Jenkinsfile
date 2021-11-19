pipeline {
    agent any

    stages {
        stage('Validate') {
            steps {
                echo 'Code Validation'
		sh 'mvn compile'
            }
        }
        stage('Unit Test') {
            steps {
                echo 'Unit Testing..'
		sh 'mvn test'
            }
        }
        stage('Sonar Analysis') {
            steps {
                echo 'Sonar Analysis....'
		sh 'mvn sonar:sonar -Dsonar.host.url=http://3.83.42.214:9000 -Dsonar.login=47c2f542b88d2b05a2dc6ff2f39644ee6245e7c2'
            }
        }
    }
}
