<p align="center">
      <img src="./imagens/logo.png" alt="Logo" width="80" height="80">
  </a>



  <h3 align="center">ATIVIDADE BANCO DE DADOS</h3>

  <p align="center">
      AVALIAÇÃO IFSULDEMINAS - 1º SEMESTRE - DESENVOLVIMENTO DE SISTEMAS</p>

Aluno: Carlos André Alves Bezerra



## Questões:

a)	Qual seria o código em SQL para criar a tabela “passageiros”?

```sh
CREATE TABLE passageiros (RG INT, Nome VARCHAR(50), Idade INT);
```

b) Qual seria o código em SQL para criar a tabela “voos”?

```sh
CREATE TABLE voos (NumeroVoo CHAR(3), Data DATE, Lugar INT);
```

c) Qual seria o código em SQL para criar a tabela “reservas”?

```sh
CREATE TABLE reservas (RG INT, NumeroVoo CHAR(3), Valor DECIMAL);
```

d) Qual seria o código em SQL para inserir os dados acima na tabela passageiros?

```sh
INSERT INTO passageiros (RG, Nome, Idade) VALUES (77890980, "Ana", 56);
INSERT INTO passageiros (RG, Nome, Idade) VALUES (12367849, "Luiz", 26);
INSERT INTO passageiros (RG, Nome, Idade) VALUES (34569874, "Paula", 13);
INSERT INTO passageiros (RG, Nome, Idade) VALUES (34521230, "Mario", 34);
```

e) Qual seria o código em SQL para inserir os dados acima na tabela voos?

```sh
INSERT INTO voos (NumeroVoo, Data, Lugar) VALUES ("A12", "2011-09-01", 45);
INSERT INTO voos (NumeroVoo, Data, Lugar) VALUES ("A45", "2011-10-01", 33);
INSERT INTO voos (NumeroVoo, Data, Lugar) VALUES ("A65", "2011-09-10", 23);
```

f) Qual seria o código em SQL para inserir os dados acima na tabela reservas?

```sh
INSERT INTO reservas (RG, NumeroVoo, Valor) VALUES (77890980, "A12", 100.00);
INSERT INTO reservas (RG, NumeroVoo, Valor) VALUES (12367849, "A12", 100.00);
INSERT INTO reservas (RG, NumeroVoo, Valor) VALUES (34569874, "A12", 100.00);
```

g) Qual seria o código em SQL para alterar na tabela passageiros o campo nome para varchar(60)?

```sh
ALTER TABLE passageiros MODIFY Nome VARCHAR(60);
```

h) Qual seria o código em SQL para apagar os passageiros com idade maior que 30 anos?

```sh
DELETE FROM passageiros WHERE Idade > 30;
```

i) Qual seria o código em SQL para atualizar o valor de todas as reservas para R$500,00?

```sh
UPDATE reservas SET Valor = 500.00;
```

j) Qual seria o código em SQL para excluir a tabela reservas?

```sh
DROP TABLE reservas;
```



<h3>Faça as seguintes Consultas:</h3>



k) Mostre todos os dados da tabela voos.

```sh
SELECT * FROM voos;
```

l) Mostre o nome e idade de todos os passageiros.

```sh
SELECT Nome, Idade FROM passageiros;
```

m) Mostre o número do voo e o valor.

```sh
SELECT NumeroVoo, Valor FROM reservas;
```

n) Mostre o número do voo, data do voo e nome do passageiro.

```sh
SELECT DISTINCT voos.NumeroVoo, voos.Data, passageiros.Nome 
FROM voos, passageiros;
```

o) Mostre o número dos voos, o valor e a data de cada voo.

```sh
SELECT DISTINCT reservas.NumeroVoo, reservas.Valor, voos.Data 
FROM reservas, voos;
```

p) Mostre o número dos voos reservados com valor maior que R$100,00.

```sh
SELECT NumeroVoo FROM reservas WHERE Valor > 100;
```

q) Mostre o nome dos clientes que reservaram o voo A12 com idade menor que 30.

```sh
SELECT DISTINCT Nome 
FROM passageiros, reservas 
WHERE NumeroVoo = "A12" && Idade < 30;

```

r) a) Mostre os voos reservados pelos passageiros ANA ou Mario.

```sh
SELECT DISTINCT NumeroVoo 
FROM passageiros, reservas 
WHERE Nome = ("Ana" || "Mario");
```

s) Mostre o nome dos passageiros que fizeram reserva nos voos A12 ou A89.

```sh
SELECT DISTINCT Nome 
FROM passageiros, reservas 
WHERE NumeroVoo = ("A12" || "A89");
```

t) Mostre o nome dos passageiros, data do voo, lugar e valor do voo.

```sh
SELECT DISTINCT passageiros.Nome, voos.Data, voos.Lugar, reservas.Valor FROM passageiros, reservas, voos;
```



## Contatos

André Alves: [andrealves-tec@hotmail.com](andrealves-tec@hotmail.com)

Linkedin: [https://www.linkedin.com/in/andrealves8/](https://www.linkedin.com/in/andrealves8/)

Github: [https://github.com/andrealves8](https://github.com/andrealves8)


# 
