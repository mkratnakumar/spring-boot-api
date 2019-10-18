pipeline{
    agent any
    stages{
        stage('Git Checkout'){
            steps{
                git credentialsId: '4007c218-5ab1-428c-96f9-227a4762439a', url: 'https://github.com/mkratnakumar/spring-boot-api.git'
            }
        }
        
        stage('Dev Deploy'){
            steps{
                sh "ansible-playbook -i dev.invenory mongodb.yml"
            }
        }
        
    }
}
