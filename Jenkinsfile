pipeline
{
    agent any
    stages
    {
       stage("CalcularEdad")
        {
            steps
            {
                script
                {
                    def fecha_nacimiento = '26/05/1981'
                    def anyo_actual = new Date().getYear()

                    edad = anyo_actual - fecha_nacimiento

                    println ("Edad: "+edad)                    
                }
            }
        }
        
       stage("GenerarTxt")
        {
            steps
            {
                script
                {
                    def contenidoFichero = "La edad es: "+edad
                    writeFile(file: "C:\\Elena\\edad.txt", text:contenidoFichero)
                }
            }
        }  
    }
}
