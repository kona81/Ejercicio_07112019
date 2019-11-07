pipeline {
    agent none
    stages {
		stage('BUILD') {
			agent {
                       label "build"
                }
			steps {
				sleep 10
                echo 'ETAPA BUILD EN UN NODO CON LABEL BUILD'
                }
        }
		stage('QUALITY') {
			agent {
                       label "quality"
                }
			steps {
				sleep 10
                echo 'Etapa Quality con un nodo con label quality'
                }
        }
		stage('DEPLOY') {
			agent {
                       label "deploy"
                }
			steps {
				sleep 10
                echo 'Etapa deploy en un nodo con label deploy'
                }
        }
    }
}
