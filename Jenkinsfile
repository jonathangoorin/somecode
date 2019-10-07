node("linux"){  
//yo
    timestamps{
        stage("Checkout"){
            checkout changelog: false, 
                    poll: false, 
                    scm: [$class: 'GitSCM', 
                            branches: [[name: '${sha1}']], 
                            doGenerateSubmoduleConfigurations: false, 
                            extensions: [[$class: 'CheckoutOption', timeout: 90]], 
                            submoduleCfg: [], 
                            userRemoteConfigs: [[
                                credentialsId: 'jonathangooringithub', 
                                url: 'https://github.com/jonathangoorin/somecode.git'
                                ]]
                        ]
        sh "touch txt.txt"
    }
    }
}