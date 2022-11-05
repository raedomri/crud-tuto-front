pipeline{
    agent any
    
    stages{
        stage("git pull"){
            steps{


                git branch: 'master',
                credentialsId: 'da9bc35b-d402-40d7-8098-e96a284e3c9b',
                url: 'https://github.com/raedomri/crud-tuto-front.git'

                }

            }
        stage('build'){
            steps
            { 
                scripts  
             {
                 sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml"
                
            }
        }
        }
            
    }
}
