def primerNumero = 8
def segundoNumero = 4
def multiplicacio = ""
def potencia = ""
pipeline
{
    agent any
    stages
    {
        stage ("Definicion de numeros")
        {
            steps
            {
                println "Primer numero " + primerNumero + ", segundo numero " + segundoNumero
            }
        }
        stage ("Multiplicación")
        {
            steps
            {
                script {
                    def mult = primerNumero * segundoNumero
                    multiplicacio = "Multiplicación "  + mult + ""
                    println multiplicacio
                }
               
            }
        }
        stage ("Potencia")
        {
            steps
            {
                script {
                    def suma = primerNumero + segundoNumero
                    def pot = suma * suma
                    potencia = "Potencia de la suma de dos numeros "  + pot
                    println potencia
                }
               
            }
        }
        stage ("Creacion de fichero")
        {
            steps
            {
                script {
                    writeFile(file: "calculos.txt", text: multiplicacio + "\n" + potencia)
                }
               
            }
        }
    }
}
