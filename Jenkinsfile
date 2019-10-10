node("linux"){  
//yo


    stage("Clone"){
        timestamps{
            checkout(
                [
                    $class: 'GitSCM', 
                    branches: [[name: '${sha1}']], 
                    doGenerateSubmoduleConfigurations: false, 
                    extensions: [
                        [$class: 'CleanBeforeCheckout'],
                        [$class: 'CheckoutOption', timeout: 90],
                        [$class: 'CloneOption', depth: 0, noTags: true, reference: '', shallow: true]
                        ], 
                    submoduleCfg: [], 
                    userRemoteConfigs: [[
                        credentialsId: 'jonathangithub', 
                        refspec: '+refs/pull/${ghprbPullId}/*:refs/remotes/origin/pr/${ghprbPullId}/*', 
                        url: 'https://github.com/jonathangoorin/somecode.git']]
                ])
                
                echo " pullid => ${ghprbPullId} && sha1 => ${sha1}"
        }
    }
    
}


//some more commits 
//jonathangooringithub