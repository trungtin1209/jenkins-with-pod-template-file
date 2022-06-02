// pipeline {

// 	agent {
//         kubernetes {
//             defaultContainer 'kaniko'
//             yaml '''
//     kind: Pod
//     spec:
//     containers:
//     - name: kaniko
//         image: gcr.io/kaniko-project/executor:debug
//         imagePullPolicy: Always
//         command:
//         - sleep
//         args:
//         - 99d
//         volumeMounts:
//         - name: aws-secret
//             mountPath: /root/.aws/
//         - name: docker-registry-config
//             mountPath: /kaniko/.docker
//     volumes:
//         - name: aws-secret
//         secret:
//             secretName: aws-secret
//         - name: docker-registry-config
//         configMap:
//             name: docker-registry-config
//     '''
//         }
//     }

// 	stages {
// 		 stage('Clean workspace') {
// 			steps {
// 				cleanWs()
// 			}
// 		}
// 	}
// }

podTemplate(yaml: readTrusted('pod.yaml')) {
    node(POD_LABEL) {
        container('busybox') {
            echo POD_CONTAINER // displays 'busybox'
            sh 'hostname'
        }
    }
}