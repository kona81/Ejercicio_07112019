pipeline {
    agent none
	tools {
        maven 'LocalMaven' 
        jdk 'LocalJDK8'
    }
    stages {
		stage('BUILD') {
			agent {
                       label "build"
                }
			steps {
				echo 'ETAPA BUILD EN UN NODO CON LABEL BUILD'
				git 'https://github.com/kona81/Ejercicio_07112019.git'
				bat 'mvn -B clean'
				bat 'mvn -B compile'
                }
        }
		stage('QUALITY') {
			agent {
                       label "quality"
                }
			steps {
				echo 'Etapa Quality con un nodo con label quality'
                }
        }
		stage('DEPLOY') {
			agent {
                       label "deploy"
                }
			steps {
				echo 'Etapa deploy en un nodo con label deploy'
                }
        }
    }
}
