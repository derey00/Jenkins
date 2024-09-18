def numero1=1
def numero2=0

pipeline
{
    agent any
    stages
    {
       stage("Numeros")
        {
            steps
            {
                script
                {
                    println ("El numero 1 es: "+numero1)
                    println ("El numero 2 es: "+numero2)
                }
            }
        }
        
       stage("Suma")
        {
            steps
            {
                script
                {
                    def suma = numero1 + numero2
                    println ("La suma es: "+suma)
                }
            }
        }
        stage("Resta")
        {
            steps
            {
                script
                {
                    def resta = numero1 - numero2
                    println ("La resta es: "+resta)
                }
            }
        }

        stage("Multiplicacion")
        {
            steps
            {
                script
                {
                    def multiplicacion = numero1 * numero2
                    println ("La multiplicacion es: "+multiplicacion)
                }
            }
        }

          stage("Division")
        {
            steps
            {
                script
                {
                    

                    
                    if (numero2 == 0)
                    {
                        println ("Error division entre 0, cambie el numero2")
                    }
                    else{
                        def division = numero1 / numero2
                        println ("La division es: "+division)
                    }
                }
            }
        }

  
    }
}