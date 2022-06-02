pipeline {

	agent any
	stages {
		 stage('Clean workspace') {
			steps {
				cleanWs()
			}
		}
	}
}

// pipeline {

//     podTemplate(yaml: readTrusted('pod.yaml')) {
//         node(POD_LABEL) {
//             container('busybox') {
//                 echo POD_CONTAINER // displays 'busybox'
//                 sh 'hostname'
//             }

//             stages {
// 		        stage('Clean workspace') {
// 			        steps {
// 				    cleanWs()
// 			        }
// 		        }
// 	        }
//         }
//     }
// }

