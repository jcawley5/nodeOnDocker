node {
    checkout scm
    
    sh "echo $PATH"
    sh "docker ps"

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("jcawley5/node-web-app")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
