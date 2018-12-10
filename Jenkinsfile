stage("Checkout") {
    checkout scm
}

stage ("ATH") {
    node {
       runATH metadataFile: "essentials.yml"
    }
}