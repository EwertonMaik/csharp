# ❤️ Linguagem de Programação C#

* Usando Visual Studio 2019 / .NET Framework e .NET CORE
* Debugging com Visual Studio
* F9 - Marcar / Desmarcar BreakPoint
* F5 - Iniciar / Continuar o Debug
* F10 - Executar um passo (pula função)
* F11 - Executar um passo (entra na função)
* SHIFT + F11 - Sair método em execução
* SHIFT + F5  - Parar Debug

Este repositório contêm alguns exemplos práticos e projetos em desenvolvimentos da Linguagem C# usando;
Classes, Atributos, Encapsulamento, Construtores, Estruturas IF ElSE - Simples, Composta, Encadeada e Ternário. Estrutura For, Foreach,
Estrutura While, Métodos, Sobrecarga, Métodos, Construtores, Herança, Polimorfismo entre outros recursos.
Uso de this para diferênciar atributos de variáveis locais. Nullable, Vetores, Matrizes, Listas, Modificador Params, Ref e Out.
Enum, Boxing e Unboxing, composição, Upcasting, Downcasting.

# ✔️ Tipo de Dados Referência e Tipo Valor/Struct.
Classe - Vantagem: usa todos recursos OO), Variáveis são ponteiros, precisa ser instânciada new, aceita valor null, suporta herança, y = x (y recebe o ponteiro de x), objetos instânciados do heap, objetos não utilizados são desalocados em um momento próximo pelo Garbage Collector.

Struct - Struct (É mais simples e performático, variáveis são caixa, não é preciso instânciar, mais é possível, não aceita null, não tem suporte a herança, aceita interfaces, y = x (recebe uma cópia de x), objetos instanciados no stack, objetos são desalocados imediatamente quando seu escopo de execução é finalizado ).

# ✔️ Memória - Stack e Heap
Garbage Collector - Processo que gerencia memória de um programa. Monitora objetos dinamicamente no heap, desalocando os que não estão sendo mais usados.

Desalocação por Escopo - O que é alocado dentro de um método é desalocado assim que a execução sair do escopo.
Variáveis locais são desalocadas imediatamente assim que seu escopo local sai de execução.

# ✔️ Valores Padrão tipo de dados Classe, Struct, Arrays
Números = 0;
bool = false;
char = caractere código 0;
objeto = null;

# ✔️ Ordem de Construção de uma Classe

* Atributos privados
* Propriedades autoimplementadas
* Construtores
* Propriedades Customizadas
* Outros Métodos da classe

# ✔️ Modificadores de Acesso para Membro de uma Classe

* 1 - public (própria classe / subclasses no assembly / classes do assembly / subclasses fora do assembly / classes fora do assembly)
* 2 - protected internal (própria classe / subclasses no assembly / classes do assembly / subclasses fora do assembly)
* 3 - internal (própria classe / subclasses no assembly / classes do assembly)
* 4 - protected (própria classe / subclasses no assembly / subclasses fora do assembly)
* 5 - private protected (própria classe / subclasses no assembly)
* 6 - private (própria classe)

# ✔️ Classes e Métodos selead

* Classe - Impede que a Classe possa ser Herdada
sealed class Product {...}
* Método - Impede o método de ser sobreposto novamente.
public sealed override void WithDraw (double amount) {...}

# ✔️ Classes Tratamento de Exceções

* Tratar erros de forma consistente e flexível. Principais são Exception (SystemException / ApplicationException)
* 1 - try (Código que é executado e pode ocorrer um erro)
* 2 - catch (Código que irá capturar e mostrar as mensagens de erro)
* 3 - finally (Código que é executado independente se houver ou não, um erro)
* Classe SystemException (IndexOutofRangeException, NullReferenceException, InvalidCastException, OutOfmemoryException, ArgumentException(ArgumentNullException, ArgumentOutOfRangeException) , ExternalExcption(ComException, SEHException), ArithmeticException(DivideByZeroException, OverflowException) ))

# ✔️ Classes Tratam Arquivos

* File, FileInfo, FileStream, StreamReader, StreamWriter - Pertencem ao NameSpace System.IO
* IOException (DirectoryNotFoundException, DriveNotFoundException, EndOfStreamException, FileLoadException, FileNotFoundException, PathTooLongException, PipeException)
NameSpace System.IO
* Objetos IDisposable não são gerenciados pelo CLR e precisam ser fechados manualmente: Font, FileStream, StreamReader, StreamWriter.
* E como alternativa, o C# possui o bloco using(){}, os objetos instânciados dentro dele é finalizado ao encerrado a execução do bloco. Ele permite ser cascateado também, using () { using () { } }
* Path - nameSpace System.IO, realiza operações com strings que contém informações de arquivos de pastas
* Trabalha com Diretórios : Directory - operações static, não precisa instânciar. DirectoryInfo - operações instância.

# ✔️ Interfaces

* Interface é um tipo que define um conjunto de operações que uma classe ou struct deve implemtar ao receber a determinada interface. Permite Baixo Acoplamento e flexíveis.
* Injeção de dependência, informar o objeto por meio do construtor, para qual ele implementa a determinada interface
* Inversão de Controle : Padrão de desenvolvimento que consiste em retirar da classe a responsabilidade de instânciar suas dependências.
* Injeção de dependência : É uma forma de realizar a inversão de controle: um componente externo instãncia a dependência, que é então injetada no objeto "pai".
* Pode ser implementada pelo Construtor, Objetos de Instãnciação (Builder / Factory), Container / Framework
* Herança (Herda as caracteristicas - Reuso) X Interfaces (Deve cumprir Implementação do contrato). Relação é-um, Generalização / Especialização, Polimorfismo
* O problema de Herança Multipla ou Diamante, que o CLR não permite, pode ser implementada de outra forma usando Interfaces.
* Interface IComparable - Interface para comparar um objeto com outro, menor, maior ou igual - Compara dois objetos retornando um número inteiro

# ✔️ Generics

* Generics, permitem que classes, interfaces e métodos possam ser parametrizados por seu tipo. Oferecem Reuso, Type Safety, Performance, uso comum - Coleções.
* GetHashCode e Equals - Classe Object, usada para comparar Objetos.
