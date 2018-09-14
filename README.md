# TP-Groovy

Ejercicio Nº1
a) 500
b) 11500

Explicación

a)

b) gerente.calcularSueldo() //Utiliza el método del padre EmpleadoJerarquico ya qué en Gerente no está sobreescrito

Float calcularSueldo() // Método de EmpleadoJerarquico
{
return super.sueldoBasico() + //Usa el método de su padre (por la palabra reservada super)
this.bonoPorCategoria()       //utiliza el método de EmpleadoJerarquico ya que no está sobreescrito en Gerente
}

Float sueldoBasico() // Método de Empleado
{

return this.montoBasico() - this.aportes() // Ambas hacen referencia a los métodos de Gerente, ya que Gerente los sobreescribe

}

Por lo que la suma nos quedaría:
super.SueldoBasico()                                   +    this.bonoPorCategoria()         =
return this.montoBasico() -   return this.aportes()    +    this.bonoPorCategoria()         =
        10000             -      (10000*0.05)          +           2000                     = 1150
