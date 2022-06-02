pipeline {

	agent {
        kubernetes {
            
            defaultContainer 'golang'
        }
    }

	stages {
		 stage('Clean workspace') {
			steps {
				cleanWs()
			}
		}
	}
}

podTemplate(yaml: readTrusted('pod.yaml')) {
    node(golang) {
        container('golang') {
            echo golang // displays 'busybox'
            sh 'hostname'
        }
    }
}