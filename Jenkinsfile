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
            withCredentials([string(credentialsId:'mytoken', variable: 'ZXlKaGJHY2lPaUpTVXpJMU5pSXNJbXRwWkNJNklqbFlhekZCV0d4S1pVRlhiMjVrWnpoMGRVNVdPVXQ2UWpWaGVtdzVRVUZVZUZOS1kzVlVkSHBhT1RBaWZRLmV5SnBjM01pT2lKcmRXSmxjbTVsZEdWekwzTmxjblpwWTJWaFkyTnZkVzUwSWl3aWEzVmlaWEp1WlhSbGN5NXBieTl6WlhKMmFXTmxZV05qYjNWdWRDOXVZVzFsYzNCaFkyVWlPaUprWldaaGRXeDBJaXdpYTNWaVpYSnVaWFJsY3k1cGJ5OXpaWEoyYVdObFlXTmpiM1Z1ZEM5elpXTnlaWFF1Ym1GdFpTSTZJbXBsYm10cGJuTXRkRzlyWlc0dGMyMXpjWE1pTENKcmRXSmxjbTVsZEdWekxtbHZMM05sY25acFkyVmhZMk52ZFc1MEwzTmxjblpwWTJVdFlXTmpiM1Z1ZEM1dVlXMWxJam9pYW1WdWEybHVjeUlzSW10MVltVnlibVYwWlhNdWFXOHZjMlZ5ZG1salpXRmpZMjkxYm5RdmMyVnlkbWxqWlMxaFkyTnZkVzUwTG5WcFpDSTZJbUptTVRFeU5qSmhMVFJrWm1RdE5EUm1OUzFoWTJJeExUZ3dNamN4TURWaFpqSTBOQ0lzSW5OMVlpSTZJbk41YzNSbGJUcHpaWEoyYVdObFlXTmpiM1Z1ZERwa1pXWmhkV3gwT21wbGJtdHBibk1pZlEuTWxqZjNld3lDeUh1SjVNMUkzU1FybTJNR2REaW1zaWkzbDItaW9ROWpNSUxldWNENVdJYzZTNU9YSTVoZ01JM1VVTmFTQ2lYZW1NbG5PMlJ0TFVkNkRMTWd4SkQ5Sl9rRm5mdWlkVjAtZDhsUlpoMGhnVGR4WWdsZlljamVUNFJHUGxQU3JNbWtMRl9EekZwdUVmRDEwTmJaeTlGVjhUVExNTHZIY21Iekk1VElFa0dWQ1RoYUJhdzVzNkpwem1uYTBYQldpWC1VSEJhZjdSVHMzVzZPc3k1dE9oQTkyX25ndHRHanllcE1YRXB3OEVCaDRqSW00S1RNUmJxSGZBbDR1S3NXV2E4ejczNVZwajRXQmdxc0FqdGl1NXN0aUVZc0R1YmhOMEQ3UGs0R2l6SlJKVG1LS3cyWUE1ZFhYUHloa1RVTjB0a0tRZjkwZU1xNWZTdWd3')]{
            sh 'cd /etc/kubernetes'
            //sh 'kubectl --token ZXlKaGJHY2lPaUpTVXpJMU5pSXNJbXRwWkNJNklqbFlhekZCV0d4S1pVRlhiMjVrWnpoMGRVNVdPVXQ2UWpWaGVtdzVRVUZVZUZOS1kzVlVkSHBhT1RBaWZRLmV5SnBjM01pT2lKcmRXSmxjbTVsZEdWekwzTmxjblpwWTJWaFkyTnZkVzUwSWl3aWEzVmlaWEp1WlhSbGN5NXBieTl6WlhKMmFXTmxZV05qYjNWdWRDOXVZVzFsYzNCaFkyVWlPaUprWldaaGRXeDBJaXdpYTNWaVpYSnVaWFJsY3k1cGJ5OXpaWEoyYVdObFlXTmpiM1Z1ZEM5elpXTnlaWFF1Ym1GdFpTSTZJbXBsYm10cGJuTXRkRzlyWlc0dGMyMXpjWE1pTENKcmRXSmxjbTVsZEdWekxtbHZMM05sY25acFkyVmhZMk52ZFc1MEwzTmxjblpwWTJVdFlXTmpiM1Z1ZEM1dVlXMWxJam9pYW1WdWEybHVjeUlzSW10MVltVnlibVYwWlhNdWFXOHZjMlZ5ZG1salpXRmpZMjkxYm5RdmMyVnlkbWxqWlMxaFkyTnZkVzUwTG5WcFpDSTZJbUptTVRFeU5qSmhMVFJrWm1RdE5EUm1OUzFoWTJJeExUZ3dNamN4TURWaFpqSTBOQ0lzSW5OMVlpSTZJbk41YzNSbGJUcHpaWEoyYVdObFlXTmpiM1Z1ZERwa1pXWmhkV3gwT21wbGJtdHBibk1pZlEuTWxqZjNld3lDeUh1SjVNMUkzU1FybTJNR2REaW1zaWkzbDItaW9ROWpNSUxldWNENVdJYzZTNU9YSTVoZ01JM1VVTmFTQ2lYZW1NbG5PMlJ0TFVkNkRMTWd4SkQ5Sl9rRm5mdWlkVjAtZDhsUlpoMGhnVGR4WWdsZlljamVUNFJHUGxQU3JNbWtMRl9EekZwdUVmRDEwTmJaeTlGVjhUVExNTHZIY21Iekk1VElFa0dWQ1RoYUJhdzVzNkpwem1uYTBYQldpWC1VSEJhZjdSVHMzVzZPc3k1dE9oQTkyX25ndHRHanllcE1YRXB3OEVCaDRqSW00S1RNUmJxSGZBbDR1S3NXV2E4ejczNVZwajRXQmdxc0FqdGl1NXN0aUVZc0R1YmhOMEQ3UGs0R2l6SlJKVG1LS3cyWUE1ZFhYUHloa1RVTjB0a0tRZjkwZU1xNWZTdWd3 apply -k ./'
            sh kubectl apply -f ./'
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
