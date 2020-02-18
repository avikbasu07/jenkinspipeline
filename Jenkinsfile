pipeline {
    agent any
/*    
    parameters { 
         string(name: 'tomcat_dev', defaultValue: '35.166.210.154', description: 'Staging Server')
         string(name: 'tomcat_prod', defaultValue: '34.209.233.6', description: 'Production Server')
    } 

    triggers {
         pollSCM('* * * * *') // Polling Source Control
     }
*/

stages{
        stage('Init'){
            steps {
                //sh 'mvn clean package'
				echo 'Now Initialising ...'
            }
            /* post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            } */
        }
		
		stage('Build'){
            steps {
                //sh 'mvn clean package'
				echo 'Now Building ...'
            }
            /*post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            } */
        }

        stage ('Deployments'){
            /*parallel{
                stage ('Deploy to Staging'){
                    steps {
                        sh "scp -i /home/jenkins/tomcat-demo.pem **/target/*.war ec2-user@${params.tomcat_dev}:/var/lib/tomcat7/webapps"
                    }
                }

                stage ("Deploy to Production"){
                    steps {
                        sh "scp -i /home/jenkins/tomcat-demo.pem **/target/*.war ec2-user@${params.tomcat_prod}:/var/lib/tomcat7/webapps"
                    }
                }
            } */
			echo 'Now Deploying ...'
        }
    }
}