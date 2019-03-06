node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t moringa:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'smnjeru' -p 'bdonkadonk' "
}
stage('Create image space'){
sh "docker tag moringa:latest smnjeru/moringa:latest"
}
stage('Push Image'){
sh "docker push smnjeru/moringa:latest"
}

stage('Apply changes to the environment'){
sh "ls -l"
}


}
