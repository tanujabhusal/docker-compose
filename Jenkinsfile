pipeline {

      agent {
	  
	  node {
	        
			label "built-in"
			customWorkspace "/mnt/project"
			}
			}
	  
	  stages {
	  
	     stage ("clone") {
	  
	        steps {
	  
	          sh "git clone https://github.com/tanujabhusal/game-of-life.git"
	          
	           }
	 	 }
	 	 
	    stage ("Build") {
	     steps {
	         
	          sh "cd /mnt/project/game-of-life/gameoflife-web/ && mvn install "
			 
	     }   
	    }
	    
	    
			stage ('warfile_3tomcat') {
			   steps {
				sh "docker-compose up -d --scale webserver=3"
							
}	
}
            
}
}


