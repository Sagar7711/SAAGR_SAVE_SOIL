pipeline{
      
	     agent{
		   
		    label{
			
			      label'built-in'
				  customWorkspace '/mnt/slave-3'
				  
				  }
				  
				}
				
				stages {
				
			           stage('cloning'){

					          steps{

	                                dir('/mnt/22Q3/'){

									 sh "rm -rf git *"
			                         sh "git clone https://github.com/Sagar7711/SAAGR_SAVE_SOIL.git -b 22Q3"
									 sh "chmod -R 777 /mnt/22Q3/SAAGR_SAVE_SOIL/index.html"
									 sh "cp /mnt/26Mar.pem /mnt/slave-3/"
									 
									 }
									 
									 }
									 
								}
								
				        stage('deploy'){
				
		                steps{

						           sh "scp -i 26Mar.pem /mnt/22Q3/SAAGR_SAVE_SOIL/index.html ec2-user@172.31.34.156:/var/www/html/"
								  
								  
								  }
								   
								  }


							}

		}				
				
				     
