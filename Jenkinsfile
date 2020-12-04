pipeline {
    agent any&lt;/code&gt;
	
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
    }
	
	post {
		always {
			cleanWs()
		}
	}
}