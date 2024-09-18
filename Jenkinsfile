import java.util.Date
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
                    def fecha_nacimiento =  new Date(1981, 7, 16)
                    println ("fecha_nacimiento: "+fecha_nacimiento) 
                    println ("fecha: "+new Date()) 
                    def anyo_actual = new Date().getYear()
                    
                    println ("anyo_actual: "+anyo_actual) 
                    def anyo_fecha_nacieminto = fecha_nacimiento.getYear()
                    println ("anyo_fecha_nacieminto: "+anyo_fecha_nacieminto) 
                    edad = anyo_actual - anyo_fecha_nacieminto
                    
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
