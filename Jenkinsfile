pipeline {
    agent any
	
	tools {
		maven "3.6.3"
	}
	
    stages {
        stage('Build') { 
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        }
    }
	
	post {
		always {
			cleanWs()
		}
	}
}