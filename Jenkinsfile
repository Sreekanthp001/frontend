// @Library('jenkins-shared-library') _

// def configMap = [
//     project : "roboshop",
//     component: "frontend"
// ]

// if( ! env.BRANCH_NAME.equalsIgnoreCase('main') ){ // if not equals to main
//     nodejsEKSPipeline(configMap) // by default it will call, call function inside this pipeline
// }
// else{
//     echo "Please proceed with PROD process"
// }

@Library('jenkins-shared-library') _

def configMap = [
    project    : "roboshop",
    component  : "frontend",
    agentLabel : "AGENT-1" // optional, shared library will fallback to 'any' if offline
]

echo "Running branch: ${env.BRANCH_NAME}"

if (!env.BRANCH_NAME.equalsIgnoreCase('main')) {
    nodejsEKSPipeline(configMap)
} else {
    echo "Please proceed with PROD process"
    // Optionally call prod pipeline here
}
