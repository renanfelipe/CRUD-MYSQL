# CRUD-MYSQL
Um Simples CRUD MySQL em Node.JS com uma interface front-end escrita em React.

Esse CRUD foi implementado seguindo o tutorial [CRUD Full Stack com Node, React & MySQL](https://www.youtube.com/watch?v=voXTVTW73E8).

Ele é bem simples, e é apenas um exercício para estudos sobre a utilização do banco de dados MySQL com Node.js.

Para executar é simples:

* Crie um banco de dados MySQL e importe o SQL a seguir para criar a estrutura da tabela:

```sql
CREATE TABLE `usuarios` (
  `id` int(11) NOT NULL,
  `nome` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `fone` varchar(45) NOT NULL,
  `data_nascimento` date NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;


ALTER TABLE `usuarios`
  ADD PRIMARY KEY (`id`);

ALTER TABLE `usuarios`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;
COMMIT;

INSERT INTO `usuarios` (`id`, `nome`, `email`, `fone`, `data_nascimento`) VALUES
(1, 'Test', 'teste@gmail.com', '32323232', '2000-01-01');
```


Depois entre na pasta API, altere o arquivo ```db.js``` com as informações sobre o seu banco de dados e depois rode ```yarn start```.
Em outro terminal entre na pasta frontend e rode ```yarn start```. O site escrito em react rodará em http://localhost:3000
