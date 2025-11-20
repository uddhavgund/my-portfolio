pipeline{
  agent any

  stages{
    stage('Clone'){
      steps{
        checkout scm
      }
    }
    stage('Deploy to EC2'){
      steps{
        sh '''
        cp -r * /var/www/html/
        '''
      }
    }
  }
}
   
