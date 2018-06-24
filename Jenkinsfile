pipeline {
  agent any
  stages {
    stage('Download Packer') {
      steps {
        sh '''wget https://releases.hashicorp.com/packer/1.2.4/packer_1.2.4_linux_amd64.zip
unzip packer_1.2.4_linux_amd64.zip
'''
      }
    }
    stage('Packer Valdiate') {
      steps {
        sh './packer validate packer.json'
      }
    }
    stage('Packer Build') {
      steps {
        sh './packer build packer.json'
      }
    }
  }
}