<h1 align="center"> :mortar_board:Pruebas unitarias - Testing 2024-1 Wednesday 2 at 4pm </h1>

## Índice
1. [Objetivo del proyecto](#Objetivo-del-proyecto)
2. [Explicación breve de las pruebas unitarias](#Explicación-breve-de-las-pruebas-unitarias)
   - [Función 1](##Función-1-ConcatenateStrings)
4. [Bibliografía](#Bibliografía)

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



<h1 align="center">:blue_book:Bibliografía</h1>
Las bases que se utilizaron para desarrollar el proyecto están en el siguiente [Github](https://github.com/yBetancurr4002/UnitTestingXUnit.)

