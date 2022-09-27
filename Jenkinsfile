pipeline{
      
	     agent{
		   
		    label{
			
			      label'built-in'
				  customWorkspace '/mnt/slave-2'
				  
				  }
				  
				}
				
				stages {
				
			           stage('cloning'){

					          steps{

	                                dir('/mnt/22Q2/'){

									 sh "rm -rf git *"
			                         sh "git clone https://github.com/Sagar7711/SAAGR_SAVE_SOIL.git -b 22Q2"
									 sh "chmod -R 777 /mnt/22Q1/SAAGR_SAVE_SOIL/index.html"
									 sh "cp /mnt/26Mar.pem /mnt/slave-2/"
									 
									 }
									 
									 }
									 
								}
								
				        stage('deploy'){
				
		                steps{

						           sh "scp -i 26Mar.pem /mnt/22Q2/SAAGR_SAVE_SOIL/index.html ec2-user@172.31.32.110:/var/www/html/"
								  
								  
								  }
								   
								  }


							}

		}				
				
				     
