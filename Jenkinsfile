pipeline {
    agent any
	
	tools {
		maven 'maven 3'
		jdk 'java 8'
	}
	
    stages {
        stage('Build') { 
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        }
		stage('Test') {
			post {
				always {
					'/src/test/java/org/apache/commons/mail/TemplateTest.java'
				}
			}
		}
    }
	
	post {
		always {
			cleanWs()
		}
	}
}