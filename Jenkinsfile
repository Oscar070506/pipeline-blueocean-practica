pipeline {
  agent any
  stages {
    stage('Incio') {
      steps {
        echo 'INICIO'
        bat(script: 'echo', encoding: 'Empezando pipeline...')
      }
    }

    stage('Sistema') {
      steps {
        echo 'SISTEMA'
        bat(script: 'echo', encoding: '%DATE% %TIME%')
      }
    }

    stage('Aprobacion') {
      steps {
        input(message: '¿Continuar a FIN?', ok: 'Continuar')
      }
    }

    stage('Fin') {
      steps {
        echo 'FIN'
        bat(script: 'echo', encoding: 'FIN: empezando')
        bat(script: 'echo', encoding: 'FIN: fecha y hora -> %DATE% %TIME%')
        bat(script: 'echo', label: 'FIN: terminado')
      }
    }

  }
}