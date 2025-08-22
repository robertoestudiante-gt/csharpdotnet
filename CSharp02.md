# 📘 Apuntes de C# .NET – Segunda Clase

## 1. Bibliotecas de clases en .NET
- La biblioteca de clases de .NET es una colección organizada de recursos de programación.  
- **Console** es una de ellas.  
- Una **clase** es un contenedor de métodos.  
- Incluso los tipos de datos forman parte de clases.  

### Sintaxis general
```csharp
Clase.Metodo();
```

### Ejemplo con `Random`
```csharp
Random dice = new Random();
int roll = dice.Next(1, 7); // número aleatorio entre 1 y 6
Console.WriteLine(roll);
```

---

## 2. Lógica de decisión – `if`, `else`, `else if`
### Ejemplo básico
```csharp
if (total > 14)
{
    Console.WriteLine("You win!");
}
else
{
    Console.WriteLine("You lose!");
}
```

### Expresiones booleanas
Una **expresión booleana** devuelve `true` o `false`.  
Se pueden usar operadores como `||` (OR) y `&&` (AND).

---

## 3. Tipos de datos
### Primitivos
- `int`
- `double`
- `bool`
- `char`

```csharp
bool esActivo = false;
char letra = 'y';
```

### Arreglos
```csharp
int[] miArray = new int[5];
miArray[2] = 5;
miArray[3] = 6;

// Matriz 2D
int[,] miMatriz = new int[2,2];
miMatriz[0,1] = 2;
```

---

## 4. Enumeraciones
```csharp
enum DiaSemana
{
    Lunes,
    Martes,
    Miércoles,
    Jueves,
    Viernes
}

Console.WriteLine($"El tercer día es {DiaSemana.Miércoles}");
```

---

## 5. Interpolación de cadenas
```csharp
int num1 = 10;
Console.WriteLine($"El número es {num1}");
```

---

## 6. Tipos `struct`
```csharp
struct Punto
{
    public int X;
    public int Y;

    public Punto(int x, int y)
    {
        X = x;
        Y = y;
    }

    public override string ToString()
    {
        return $"({X}, {Y})";
    }
}
```

---

## 7. Tuplas
```csharp
(string nombre, int edad) persona = ("Pedro", 34);
Console.WriteLine(persona.nombre);
```

### Declaración implícita
```csharp
var t = (1, 2, 3, "número");
Console.WriteLine(t.Item1); // 1
```

---

## 8. Estructura `switch`
```csharp
int opcion = 2;

switch (opcion)
{
    case 1:
        Console.WriteLine("Opción 1");
        break;
    case 2:
        Console.WriteLine("Opción 2");
        break;
    default:
        Console.WriteLine("Ninguna coincidencia");
        break;
}
```

---

## 9. Ciclos e iteraciones
### For
```csharp
for (int i = 0; i < 10; i++)
{
    Console.WriteLine("Iteración: " + i);
}
```

### While
```csharp
int contador = 1;
while (contador <= 5)
{
    Console.WriteLine("Iteración: " + contador);
    contador++;
}
```

### Do While
```csharp
int contador = 1;
do
{
    Console.WriteLine("Iteración: " + contador);
    contador++;
} while (contador <= 5);
```

### Foreach
```csharp
int[] numeros = { 1, 2, 3, 4 };

foreach (int num in numeros)
{
    Console.WriteLine("Número: " + num);
}
```

Con listas:
```csharp
List<string> nombres = new List<string> { "John", "Luke", "Matt" };

foreach (string persona in nombres)
{
    Console.WriteLine("Persona: " + persona);
}
```

---

## 10. Manejo de excepciones – `try`, `catch`, `finally`
```csharp
try
{
    int divisor = 0;
    int resultado = 10 / divisor;
}
catch (Exception e)
{
    Console.WriteLine("Error: " + e.Message);
}
finally
{
    Console.WriteLine("Este bloque siempre se ejecuta.");
}
```
