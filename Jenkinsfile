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
            echo POD_CONTAINER // displays 'busybox'
            sh 'hostname'
        }
    }
}