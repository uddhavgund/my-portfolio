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
        sudo cp -r * /var/www/html/
        '''
      }
    }
  }
}
   
