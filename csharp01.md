
# 📘 Apuntes de C# .NET – Primeros Pasos

## 1. Escribir las primeras líneas de código
En C# usamos la clase **Console** para interactuar con la terminal.  
El método más común es `WriteLine()`, que imprime un valor seguido de un salto de línea.

```csharp
Console.WriteLine("Hola, mundo!");
```

### Diferencia entre `Console.Write` y `Console.WriteLine`
- `Write` imprime sin salto de línea.  
- `WriteLine` imprime y agrega un salto de línea.

```csharp
Console.Write("Hola");
Console.Write(" mundo");
Console.WriteLine("!");
// Salida: Hola mundo!
```

---

## 2. Comentarios en el código
Los comentarios en C# se escriben con **doble diagonal (`//`)**.

```csharp
// Este es un comentario
Console.WriteLine("Ejecutando código...");
```

---

## 3. Valores literales
Un **valor literal** es un dato escrito directamente en el código y que no cambia.

```csharp
Console.WriteLine(123);        // Entero
Console.WriteLine("Roberto");  // Cadena de texto
Console.WriteLine('A');        // Carácter
```

⚠️ Importante:  
- `'a'` → válido (un solo carácter).  
- `"hola"` → válido (cadena de caracteres).  
- `'hola'` → error (demasiados caracteres para un `char`).  

---

## 4. Tipos numéricos
### Enteros
```csharp
Console.WriteLine(42);  // Imprime 42
```

### Punto flotante
C# admite:
- `float`
- `double`
- `decimal` (más preciso para cálculos financieros).

```csharp
Console.WriteLine(3.14f);   // float
Console.WriteLine(2.718);   // double
Console.WriteLine(2.625m);  // decimal
```

---

## 5. Declaración de variables
Una **variable** es un contenedor para almacenar valores que pueden cambiar durante la ejecución.

```csharp
string nombre = "Ana";
int edad = 25;
bool esActivo = true;
```

### Reglas para nombres de variables
- Deben iniciar con letra o `_`.  
- No pueden contener caracteres especiales como `#` o `$`.  
- Son **case-sensitive** (`Nombre` ≠ `nombre`).  
- No pueden ser palabras reservadas (`string string;` ❌).  

---

## 6. Operaciones con cadenas de texto
### Concatenación
```csharp
string nombre = "Bob";
int edad = 30;
Console.WriteLine(nombre + " tiene " + edad + " años.");
```

### Interpolación
```csharp
string nombre = "Bob";
int edad = 30;
Console.WriteLine($"{nombre} tiene {edad} años.");
```

---

## 7. Operaciones matemáticas
```csharp
int suma = 7 + 5;       // 12
int resta = 7 - 5;      // 2
int producto = 7 * 5;   // 35
int cociente = 7 / 5;   // 1 (división entera)

Console.WriteLine($"Suma: {suma}, Resta: {resta}, Multiplicación: {producto}, División: {cociente}");
```

### División con decimales
```csharp
decimal resultado = 7.0m / 5;
Console.WriteLine($"Cociente decimal: {resultado}");
```

---

## 8. Orden de operaciones
C# respeta la jerarquía matemática (paréntesis, multiplicación/división, suma/resta).

```csharp
int v1 = 3 + 4 * 5;     // 23
int v2 = (3 + 4) * 5;   // 35
```

---

## 9. Incremento y decremento
```csharp
int valor = 1;

valor++;  // Incrementa en 1
Console.WriteLine(valor); // 2

valor--;  // Decrementa en 1
Console.WriteLine(valor); // 1
```

### Uso con `+=` y `-=`
```csharp
int x = 5;
x += 3;  // 8
x -= 2;  // 6
```

---

## 10. Ejercicio: Conversión Celsius ↔ Fahrenheit
```csharp
int fahrenheit = 94;
decimal celsius = (fahrenheit - 32m) * (5m / 9m);

Console.WriteLine($"La temperatura es {celsius} °C");
```

---

## 11. Ejercicio: Promedio de calificaciones
```csharp
int tareas = 5;
int s1 = 93, s2 = 87, s3 = 98, s4 = 95, s5 = 100;

decimal promedio = (s1 + s2 + s3 + s4 + s5) / (decimal)tareas;

Console.WriteLine($"Promedio: {promedio}");
```

---

## 12. Formato de salida en consola
Puedes usar `	` (tabulación) y `
` (salto de línea).

```csharp
Console.WriteLine("Alumno		Nota");
Console.WriteLine("Sophia		95");
Console.WriteLine("Nicolás		88");
```
