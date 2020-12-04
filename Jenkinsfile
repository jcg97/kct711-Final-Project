pipeline {
    agent any
	
	tools {
		maven 
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