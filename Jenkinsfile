pipeline {
  agent any
    stages {
        stage('Pull') {
             steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                        userRemoteConfigs: [[credentialsId: '01039517-19db-4e4e-a50c-73a292ef2443',
                            url: 'https://github.com/mohamedthemer/Myapp.git']]])
                }
            }
        }
     stage ('Build') {
	
			steps {
			
			sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml"
	
			}


	}
     }

   }
     
