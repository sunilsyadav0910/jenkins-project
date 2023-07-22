pipeline {
    agent any

      environment { 
         
           ENV_URL = "jenkins.global.com"
       }

    stages {
        stage("AWS Demo") {
            steps { 
                 echo " This is global value of ${ENV_URL} "
                 echo "I am Stage One Step"                    
                 echo " I am in step 2"
                  } 
        }  
        
       stage("stage 2") { 
             
          environment { 
             ENV_URL = "jenkins.stage2.com"
           }
          steps { 
        
              echo "I am in stage 2"
              sh ''' echo "this is local value of ${ENV_URL}" 

                    env  '''
           } 
         }             


    }
 }

