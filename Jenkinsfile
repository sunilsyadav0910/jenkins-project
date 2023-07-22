pipeline {
    agent any

    environment { 
         URL="jenkins.global"
    }

    stages {
        stage("AWS Demo") {
            steps { 
                 echo " This is global value of ${URL} "
                 echo "I am Stage One Step"                    
                 echo " I am in step 2"
                  } 
        }  
        
       stage("stage 2") { 
             steps { 
        
              echo "I am in stage 2"
              sh ''' echo "this is local value of ${URL}" 

                    env  '''
           } 
         }             


    }
 }

