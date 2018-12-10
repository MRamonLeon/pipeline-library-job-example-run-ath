node {
    stage("Checkout") {
    checkout scm
    }

    stage ("ATH") {
        node {
        runATH metadataFile: pwd() + "essentials.yml"
        }
    }
}