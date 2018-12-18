// This is a pipeline

static isPullRequestFromFork(env) {
    return env?.getProperty('CHANGE_FORK') ? true : false
}

//def isPullRequestFromFork(jenkins.env)

 def runPipeline() {
     
     jenkins.stage("Cleanup") {
            mvn clean install
     }
     jenkins.echo ${scm.GIT_BRANCH}
     jenkins.echo ${scm.GIT_URL}
     
   jenkins.echo ${jenkins.env}

if (isPullRequestFromFork) {
jenkins.echo "True"
}
   
 }
