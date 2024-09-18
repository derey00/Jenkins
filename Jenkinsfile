import java.text.SimpleDateFormat;
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
                    fecha_nacimiento = '01/01/1981'
                    
                    def fecha = new SimpleDateFormat("dd/MM/yyyy").parse(fecha_nacimiento)
                    fechaNa = fecha.getYear().toInteger()
                    println ("fechaNa: "+fechaNa)
                    
                    
                    def anyo_actual = new Date().getYear().toInteger()
                    println ("anyo_actual: "+anyo_actual) 
                    
                    
                    
                    edad = anyo_actual - fechaNa
                    println ("edad: "+edad) 
                }

            }
        }
        
       stage("GenerarTxt")
        {
            steps
            {
                script
                {
                    
                    writeFile(file: "C:\\Elena\\edad.txt", text:"la edad es:"+edad)
                }
            }
        }  
    }
}
