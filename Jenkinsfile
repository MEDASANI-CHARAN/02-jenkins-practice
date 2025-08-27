/// sample script ///

// pipeline {
// 	agent any
// 	stages{
// 		stage('Devops'){
// 			steps {
// 				echo 'Am learning devops'
// 			}
// 		}
// 		stage('Jenkins'){
// 			steps {
// 				sh 'echo Am learning jenkins'
// 			}
// 		}
// 		stage('K8s'){
// 			steps {
// 				sh 'echo Am learning k8s'
// 			}
// 		}
// 	}
// }


/// Icluded particular agent ///

pipeline {
	agent node {
        label 'AGENT-1'
    }
	stages{
		stage('Devops'){
			steps {
				echo 'Am learning devops'
			}
		}
		stage('Jenkins'){
			steps {
				sh 'echo Am learning jenkins'
			}
		}
		stage('K8s'){
			steps {
				sh 'echo Am learning k8s'
			}
		}
	}
}
