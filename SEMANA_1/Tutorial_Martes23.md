# Creación de proyecto con clases

## Introducción a las Clases
En C#, una clase es un plano para crear objetos. Define un tipo de dato que agrupa datos y métodos que operan sobre esos datos. Aquí tienes un ejemplo básico de una clase:

```csharp
public class Empleado
{
    // Propiedades
    public string Nombre { get; set; }
    public string Apellido { get; set; }
    public string Cargo { get; set; }
    public DateTime FechaIngreso { get; set; }
    private decimal Salario { get; set; }

    // Constructor
    public Empleado(string pNombre, string pApellido, string pCargo, DateTime pFechaIngreso, decimal pSalario)
    {
        this.Nombre = pNombre;
        this.Apellido = pApellido;
        this.Cargo = pCargo;
        this.FechaIngreso = pFechaIngreso;
        this.Salario = pSalario;
    }

    // Método
    public int CalcularAntiguedad()
    {
        return DateTime.Now.Year - this.FechaIngreso.Year;
    }
    public int SalarioBruto()
    {
        return this.Salario - (this.Salario * 0.03 + this.Salario * 0.0725);
    }
}
```

## Uso de la Clase Banco
Finalmente, veamos cómo usar esta clase en un programa:
```csharp
using AbogadosNotariosLopez.EN;

class Program
{
    static void Main(string[] args)
    {
        Empleado empleado1 = new Empleado();
        empleado1.Nombre = "Juan G";
        
     

        Console.WriteLine($"Nombre del Banco: {miBanco.NombreBanco}");
        Console.WriteLine($"Saldo Final: {miBanco.Saldo:C}");
    }
}
```

## Conceptos Teóricos
- **Clases:** Son plantillas para crear objetos. Contienen campos, propiedades, métodos y eventos.
- **Propiedades:** Permiten el acceso controlado a los campos de una clase. Utilizan los accesores get y set.
- **Métodos:** Son funciones que realizan acciones específicas. Pueden recibir parámetros y devolver valores.
