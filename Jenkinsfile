pipeline {
  agent any
  stages {
 
  
      stage("Build image") {
                 steps {
                echo 'Building..'
                       }
      }
    
    
    stage('Deploy App') {
      steps {
        script {
           
          //kubernetesDeploy(configs: "hellowhale.yml", kubeconfigId: "kubeconfig")
          //kubernetesDeploy([kubeconfigId: 'kubeconfig' , configs: 'hellowhale.yml'])
           
          //kubernetesDeploy(credentialsType: 'KubeConfig', kubeConfig: [path: 'kubeconfig.yaml'], configs: '**/hellowhale.yml', enableConfigSubstitution: false )
           
          node ('master'){
            sh 'cd /etc/kubernetes'
            sh 'kubectl apply -k ./'
          
          }
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
 
  }
 
}
