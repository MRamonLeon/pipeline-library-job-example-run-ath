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
        environment {
            RUN_ATH_LOCAL_PLUGINS_STASH_NAME = false
        } 
        runATH metadataFile: checkoutDir + "/essentials.yml"
        }
    }
}