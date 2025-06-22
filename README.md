# SudokuJava

Este é um projeto de Sudoku em Java, desenvolvido para rodar no terminal. O usuário pode iniciar um novo jogo, inserir e remover números, visualizar o tabuleiro, verificar o status do jogo, limpar ou finalizar a partida.

## Estrutura do Projeto

```
src/
  main/
    java/
      br/
        com/
          dio/
            Main.java
            model/
              Board.java
              Space.java
              GameStatusEnum.java
            util/
              BoardTemplate.java
```

## Como Compilar

Utilize o Maven para compilar o projeto:

```sh
mvn clean compile
```

Ou, se preferir usar o `javac` diretamente:

```sh
javac -d target/classes $(find src/main/java -name "*.java")
```

## Como Executar

Execute o programa passando as configurações iniciais do tabuleiro como argumentos:

```sh
java -cp out/production/SudokuJava br.com.dio.Main "0,0;4,false" "1,0;7,false" "2,0;9,true" "3,0;5,false" "4,0;8,true" "5,0;6,true" "6,0;2,true" "7,0;3,false" "8,0;1,false" "0,1;1,false" "1,1;3,true" "2,1;5,false" "3,1;4,false" "4,1;7,true" "5,1;2,false" "6,1;8,false" "7,1;9,true" "8,1;6,true" "0,2;2,false" "1,2;6,true" "2,2;8,false" "3,2;9,false" "4,2;1,true" "5,2;3,false" "6,2;7,false" "7,2;4,false" "8,2;5,true" "0,3;5,true" "1,3;1,false" "2,3;3,true" "3,3;7,false" "4,3;6,false" "5,3;4,false" "6,3;9,false" "7,3;8,true" "8,3;2,false" "0,4;8,false" "1,4;9,true" "2,4;7,false" "3,4;1,true" "4,4;2,true" "5,4;5,true" "6,4;3,false" "7,4;6,true" "8,4;4,false" "0,5;6,false" "1,5;4,true" "2,5;2,false" "3,5;3,false" "4,5;9,false" "5,5;8,false" "6,5;1,true" "7,5;5,false" "8,5;7,true" "0,6;7,true" "1,6;5,false" "2,6;4,false" "3,6;2,false" "4,6;3,true" "5,6;9,false" "6,6;6,false" "7,6;1,true" "8,6;8,false" "0,7;9,true" "1,7;8,true" "2,7;1,false" "3,7;6,false" "4,7;4,true" "5,7;7,false" "6,7;5,false" "7,7;2,true" "8,7;3,false" "0,8;3,false" "1,8;2,false" "2,8;6,true" "3,8;8,true" "4,8;5,true" "5,8;1,false" "6,8;4,true" "7,8;7,false" "8,8;9,false"
```

Cada argumento representa uma posição do tabuleiro no formato:

```
linha,coluna;valor,fixed
```

- `linha,coluna`: coordenadas da célula (0 a 8)
- `valor`: número inicial da célula (1 a 9)
- `fixed`: `true` se o valor é fixo (não pode ser alterado), `false` caso contrário

**Exemplo de argumento:**
`"0,0;5,true"` define a célula [0,0] com valor 5 fixo.

## Funcionalidades

- **1 - Iniciar um novo Jogo:** Inicializa o tabuleiro com os valores informados.
- **2 - Colocar um novo número:** Permite inserir um número em uma célula não fixa.
- **3 - Remover um número:** Permite remover um número de uma célula não fixa.
- **4 - Visualizar jogo atual:** Mostra o tabuleiro atual.
- **5 - Verificar status do jogo:** Mostra se o jogo está completo, incompleto ou não iniciado, e se há erros.
- **6 - Limpar jogo:** Remove todos os números inseridos pelo usuário.
- **7 - Finalizar jogo:** Verifica se o jogo foi concluído corretamente.
- **8 - Sair:** Encerra o programa.

## Observações

- É necessário passar todas as 81 posições do tabuleiro como argumentos ao iniciar o programa.
- O projeto utiliza Java 24 (veja a configuração no `pom.xml`).

## Licença

Este projeto é apenas para fins educacionais.
