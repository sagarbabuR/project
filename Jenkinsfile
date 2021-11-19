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
		sh 'mvn sonar:sonar -Dsonar.host.url=http://3.83.42.214:9000 -Dsonar.login=c13305ff34b859ab756d887dbe2edd3c783a6a29
'
            }
        }
    }
}
