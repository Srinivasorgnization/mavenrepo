pipeline{

agent any

triggers {
// poll repo every 2 minute for changes
pollSCM('* * * * *')
}

stages{

stage('git'){
steps{
checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '190257ce-7bf2-4b8f-b8a9-905bac4a9f99', url: 'https://github.com/Srinivasorgnization/mavenrepo.git']]])

}
}    // stage 1  close

stage('build'){
steps{
sh 'mvn package'
}
}




} //stages close
} //pipeline close
