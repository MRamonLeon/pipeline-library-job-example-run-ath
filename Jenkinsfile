#!/usr/bin/env groovy 
node {
    def checkoutDir = pwd(tmp:true) + "/dir"
    stage("Checkout") {
        dir(checkoutDir) {
            checkout scm
        }
    }

    stage ("ATH") {
        node {
      
        runATH metadataFile: checkoutDir + "/essentials.yml"
        }
    }
}