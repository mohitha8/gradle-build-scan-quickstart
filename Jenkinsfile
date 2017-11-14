
properties([
  parameters([
    string(name: 'param1', description: 'Possible options: a b c d', defaultValue: ''),
    string(name: 'param2', description: 'Possible options: e f g h', defaultValue: 'defaultValue'),
    string(name: 'param3', description: 'Possible options: k l m n', defaultValue: ''),
    string(name: 'param4', description: 'Possible options: 1 2 3 4', defaultValue: ''),
  ])
])

node{
    env.custom_var       = "custom_value"
  def paramname = "paramValue";
    echo "custom variable value is ${paramname}"
   echo "param1 vallue is ${param1}"
  echo "param2 value is ${param2}"
    stage("compile"){
   checkout([$class: 'GitSCM', branches: [[name: "*/${BRANCH_NAME}"]], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/mohitha8/gradle-build-scan-quickstart.git']]])
}
    stage("build"){
        
       // sh 'mvn install'
      build 'shpipeline' $paramname
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
