pipeline { 
    agent any
    stages { 
        stage ('Build') {
          steps {
            sh 'npm install'
          }
        }
        stage ('Test') {
            steps {
            sh 'npm test'
            }
        }
        stage ('Deploy') {
        steps {
            sh 'ssh -i "Masterkey.pem" ubuntu@ec2-52-66-244-239.ap-south-1.compute.amazonaws.com "docker pull node:app2 && docker run -d -p 8000:8001 node:app2"'
        }
        }
    }

}
