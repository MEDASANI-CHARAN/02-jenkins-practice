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

/// - Prevents Jenkins from running two builds of the same pipeline job at the same time.
/// - If a new build is triggered while another is already running: 
   // - The new one will wait in the queue until the running one finishes (default) 
   // - Or, if you configure disableConcurrentBuilds(abortPrevious: true), it will stop the old one 
   //   and  run the new one.

// pipeline {
// 	agent {
//         label 'AGENT-1'
//     }
//     environment {
//         COURSE = 'Jenkins'
//     }
//     options {
//         timeout(time: 10, unit: 'MINUTES') 
//         disableConcurrentBuilds()
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


///// Parameters /////

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
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
         stage('parameters') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
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