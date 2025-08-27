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

// pipeline {
// 	agent {
//         label 'AGENT-1'
//     }
//     environment { 
//         COURSE = 'Jenkins'
//     }
// 	stages{
// 		stage('Build'){
// 			steps {
// 				script {
//                     echo 'Building'
//                 }
// 			}
// 		}
// 		stage('Test'){
// 			steps {
// 				script {
//                     sh 'echo Testing'
//                 }
// 			}
// 		}
// 		stage('Deploy'){
// 			steps {
// 				script {
//                     sh 'echo Deploying'
//                 }
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

///// Environmnet /////

// pipeline {
// 	agent {
//         label 'AGENT-1'
//     }
//     environment {
//         COURSE = 'Jenkins'
//     }
// 	stages{
// 		stage('Build'){
// 			steps {
// 				script {
//                     sh """
//                         echo 'Building'
//                         env
//                     """
//                 }
// 			}
// 		}
// 		stage('Test'){
// 			steps {
// 				script {
//                     sh 'echo Testing'
//                 }
// 			}
// 		}
// 		stage('Deploy'){
// 			steps {
// 				script {
//                     sh 'echo Deploying'
//                 }
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

///// Options - timeout /////

/// - It sets a global timeout for the entire pipeline (not just one stage).
/// - If the whole pipeline runs longer than 1 second, Jenkins will abort it automatically.

// pipeline {
// 	agent {
//         label 'AGENT-1'
//     }
//     environment {
//         COURSE = 'Jenkins'
//     }
//     options {
//         timeout(time: 5, unit: 'Seconds') // abort if pipeline runs more than 5 seconds
//     }
// 	stages{
// 		stage('Build'){
// 			steps {
// 				script {
//                     sh """
//                         echo 'Building'
//                         sleep 10
//                         env
//                     """
//                 }
// 			}
// 		}
// 		stage('Test'){
// 			steps {
// 				script {
//                     sh 'echo Testing'
//                 }
// 			}
// 		}
// 		stage('Deploy'){
// 			steps {
// 				script {
//                     sh 'echo Deploying'
//                 }
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


///// Options - disableConcurrentBuilds /////

pipeline {
	agent {
        label 'AGENT-1'
    }
    environment {
        COURSE = 'Jenkins'
    }
    options {
        timeout(time: 10, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
	stages{
		stage('Build'){
			steps {
				script {
                    sh """
                        echo 'Building'
                        sleep 10
                        env
                    """
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