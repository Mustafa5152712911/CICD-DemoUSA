pipeline
{
agent any 
stages{
stage('Build Application'){
steps{
hs 'mvn clean install'
}
}

stage('Deploy Application To Mulesoft CloudHub'){
steps{
hs 'mvn package deploy -DmuleDeploy'
}
}

stage('Perform Regression Testing'){
steps{
hs 'newman run /home/mustafa/Music/newmen/World-time-Zone.postman_collection.json'
}
}

}
}