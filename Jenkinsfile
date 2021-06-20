pipeline {
  agent any
  stages {
 
    stage('Checkout Source') {
      steps {
        //checkout scm
       }
    } 
      stage("Build image") {
            steps {
                 steps {
                echo 'Building..'
                       }
            }
        }
     stage('Test') {
            steps {
                echo 'Testing..'
                sh 'kubectl get pods'
                sh 'kubectl get services wordpress'
            }
        }
    
    stage('Deploy App') {
      steps {
        script {
           
          //kubernetesDeploy(configs: "hellowhale.yml", kubeconfigId: "kubeconfig")
          //kubernetesDeploy([kubeconfigId: 'kubeconfig' , configs: 'hellowhale.yml'])
           
          //kubernetesDeploy(credentialsType: 'KubeConfig', kubeConfig: [path: 'kubeconfig.yaml'], configs: '**/hellowhale.yml', enableConfigSubstitution: false )
           
          
            sh 'kubectl apply -k ./'
          
           
        }
      }
    }
 
  }
 
}
