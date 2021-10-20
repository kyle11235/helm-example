- helm

        - config

                - check setup me up
                helm repo add helm_dev_virtual http://182.92.214.141:8081/artifactory/helm_dev_virtual --username kyle --password xxx

        - test
        
                - resolve (must resolve from virtual)
                
                        helm repo update

                        helm search repo helm_dev_virtual/nginx-ingress
                        helm pull helm_dev_virtual/nginx-ingress

                        helm search repo helm_dev_virtual/prometheus
                        helm pull helm_dev_virtual/prometheus-community/prometheus

                - deploy

                        - deploy from UI

                        - check setup me up
                        curl -H 'X-JFrog-Art-Api:xxx' -T <PATH_TO_FILE> "http://182.92.214.141:8081/artifactory/helm_dev_virtual/<TARGET_FILE_PATH>"
