pipeline {
    agent any
    options {
        ansiColor('xterm')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		withGradle {
			sh './gradlew assemble'
		}
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		withGradle {
			sh './gradlew test'
		}
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
