pipeline{
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')

    }
    satges {
        stage ('Example') 
        {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography:${params.BIOGRAPHY}"
                echo "Toogle:${params.TOGGLE}"
                echo "Choice is:${params.CHOICE}"
                echo "Password is:${params.PASSWORD}"

            }

        }
    }
}
