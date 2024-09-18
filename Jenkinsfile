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
                    fecha_nacimiento = new Date(1981)
                    
                    
                    def anyo_actual = new Date().getYear()
                    
                    anyo_fecha_nacimiento = new Date(1981).getYear()
                    
                    edad = anyo_actual - anyo_fecha_nacimiento
                    
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
