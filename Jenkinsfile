node{
    stage("compile"){
   checkout([$class: 'GitSCM', branches: [[name: "*/${BRANCH_NAME}"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/gradle/gradle-build-scan-quickstart.git']]])
}
    stage("build"){
        
       // sh 'mvn install'
        
}
    stage("deployment"){
}
    stage("checkout"){
}
     stage("smoke test"){

          //sh './sample.sh'
          //echo "Build id is ${BUILD_ID}"
          //echo "Job name is ${JOB_NAME}"
          //echo "Node name is ${NODE_NAME}"
        // sh './gradlew build --scan'
     } 

}
