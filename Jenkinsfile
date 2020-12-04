pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v C:\Windows\System32\config\systemprofile\AppData\Local\Jenkins\.jenkins\workspace\kct711-final' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
		stage('Test1') {
			steps{
				sh 'mvn test'
			}
			post{
				always {
					junit 'target/surefire-reports/*.xml'
				}
			}
		}
		stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}