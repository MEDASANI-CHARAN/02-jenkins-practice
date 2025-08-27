///// sample script /////

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


///// agent /////

// pipeline {
// 	agent {
//         label 'AGENT-1'
//     }
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


///// post & delete Dir /////

// pipeline {
// 	agent {
//         label 'AGENT-1'
//     }
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
//     post { 
//         always { 
//             echo 'I will always say Hello again!'
//             deleteDir()
//         }
//         success { 
//             echo 'I will always say success!'
//         }
//         failure { 
//             echo 'I will always say failure!'
//         }
//     }
// }

// Note: By default, Jenkins agents do not delete the workspace or downloaded files after a job is done. If the next job runs on the same agent, the old files that are still there (code, dependencies, or build results) can cause problems like conflicts or errors. //


///// script /////

pipeline {
	agent {
        label 'AGENT-1'
    }
	stages{
		stage('Build'){
			steps {
				script {
                    echo 'Building'
                }
			}
		}
		stage('Test'){
			steps {
				script {
                    sh 'echo Testing'
                }
			}
		}
		stage('Deploy'){
			steps {
				script {
                    sh 'echo Deploying'
                }
			}
		}
	}
    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'I will always say success!'
        }
        failure { 
            echo 'I will always say failure!'
        }
    }
}