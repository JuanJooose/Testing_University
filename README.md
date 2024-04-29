<h1 align="center"> :mortar_board:Pruebas unitarias - Testing 2024-1 Wednesday 2 at 4pm </h1>

## Índice
- [Objetivo del proyecto](#Objetivo-del-proyecto)
   
- [Explicación breve de las pruebas unitarias](#Explicacion-breve-de-las-pruebas-unitarias)
   
   - [Función 1 ConcatenateStrings](##Funcion-1-ConcatenateStrings)
  
   - [Función 2 ReverseString](##Funcion-2-ReverseString)
 
   - 

- [Bibliografía](#Bibliografía)

<h1 align="center"> :dart:Objetivo del proyecto </h1>

Este proyecto de pruebas se hizo con el fin de adquirir conocimientos acerca de como se hacen las pruebas unitarias en C# con xUnit, donde el proyecto toma 11 funciones que interactuan con strings la cuales entregan diferentes soluciones.

<h1 align="center">:left_right_arrow:Explicación breve de las pruebas unitarias</h1>

## Función 1 ConcatenateStrings

Se elaboró solamente una prueba unitaria ya que la función consistía en unir dos strings, como se sabe, los strings puede gaurdar cualquier carácter, asi que no había un error grande para este caso.
incluso, se hizo otra pureba unitaria, pero se skipea porque no se considera necesaria.

Adjunto código.

```csharp,

/// <summary>
/// // Tests for the first option of menu.
/// </summary>
[Fact]
public void ConcatenateStrings_Test_1_Equal()
{
    // Arrange
    StringOperations StringsFunctions = new StringOperations();
    string input_1 = "xUnit";
    string input_2 = "Tests";
    string expectedResult = "xUnit Tests";

    // Act
    string ResultOfFunction = StringsFunctions.ConcatenateStrings(input_1, input_2);

    // Assert
    Assert.Equal(expectedResult, ResultOfFunction);
}

[Fact(Skip = "This unit tests is not required")]
public void ConcatenateStrings_Test_2_True()
{

    // Arrange
    string input_1 = "";
    string input_2 = "";

    // Assert
    Assert.True(string.IsNullOrEmpty(input_1) ? string.IsNullOrEmpty(input_2) : false);
}


```

## Función 2 ReverseString

En ese caso, se agrego una prueba unitaria en caso de que no fuera null para que la validara. Esta prueba no tiene una gran validez ya que solo es hacer al revés una palabra o frase.

```csharp,

/// <summary>
/// // Tests for the second option of menu.
/// </summary>
[Fact]
public void ReverseString_Test_1_Equal()
{
    // Arrange
    StringOperations StringsFunctions = new StringOperations();
    string input_1 = "Tests";
    string expectedResult = "stseT";

    // Act
    string ResultOfFunction = StringsFunctions.ReverseString(input_1);

    // Assert
    Assert.Equal(expectedResult, ResultOfFunction);
}


[Fact]
public void ReverseString_Test_2_NotNull()
{
    // Arrange
    string input_1 = "";

    // Assert
    Assert.NotNull(input_1);
}

```

## Función 3 - GetStringLength

```csharp,

/// <summary>
/// // Tests for the third option of menu.
/// </summary>

[Fact]
public void GetStringLength_Test_1_Equal()
{
    // Arrange
    StringOperations StringsFunctions = new StringOperations();
    string input_1 = "Tests";
    int expectedResult = 5;

    // Act
    int ResultOfFunction = StringsFunctions.GetStringLength(input_1);

    // Assert
    Assert.Equal(expectedResult, ResultOfFunction);
}

[Fact]
public void GetStringLength_Test_2_Exception()
{
    //Arrange
    StringOperations StringsFunctions = new StringOperations();

    // Assert
    Assert.Throws<ArgumentNullException>(() => StringsFunctions.GetStringLength(null));
}

```


<h1 align="center">:blue_book:Bibliografía</h1>

Las bases que se utilizaron para desarrollar el proyecto están en el siguiente [Github](https://github.com/yBetancurr4002/UnitTestingXUnit)

