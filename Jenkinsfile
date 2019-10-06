node("linux"){  
//yo
    timestamps{
        stage("Checkout"){
            checkout changelog: false, 
                    poll: false, 
                    scm: [$class: 'GitSCM', 
                            branches: [[name: '*/master']], 
                            doGenerateSubmoduleConfigurations: false, 
                            extensions: [[$class: 'CheckoutOption', timeout: 90]], 
                            submoduleCfg: [], 
                            userRemoteConfigs: [[
                                credentialsId: 'jonathangithub', 
                                url: 'https://github.com/jonathangoorin/somecode.git'
                                ]]
                        ]
    }
    }
}