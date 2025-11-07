---
layout: post
title: "Como usar o DB Fiddle para rodar bancos de dados online"
author: Lux
date: 2025-10-31
categories: [Banco de Dados, Tutoriais, SQL]
tags: [DB Fiddle, SQL, Ferramentas Online]
description: Aprenda a usar o DB Fiddle para criar, testar e compartilhar consultas SQL de forma prática e sem precisar instalar nada.
image: /assets/img/dbfiddle-banner.png
---

![Capa do tutorial: DB Fiddle](https://raw.githubusercontent.com/yourusername/yourrepo/main/assets/img/dbfiddle-banner.png)

# 💻 Tutorial — Como usar o DB Fiddle para rodar bancos de dados online

**Autor:** Lux  
**Tema principal:** Uso prático do DB Fiddle (db-fiddle.com / dbfiddle.uk) para executar, testar e compartilhar consultas SQL sem precisar instalar um SGBD local.  
**Relação com a disciplina:** Ferramentas de apoio para gerenciamento de banco de dados e prática de SQL.

---

## 🎯 Objetivo
Aprender a criar um esquema simples, inserir dados, executar consultas e compartilhar o resultado usando o DB Fiddle. Ao final, você terá um *fiddle* público (link) que pode ser usado em trabalhos e comunicação com colegas/professores.

---

## 🚀 Por que usar o DB Fiddle?
✅ Não precisa instalar nada.  
✅ Suporta MySQL, PostgreSQL, SQLite, SQL Server, Oracle e outros.  
✅ Ideal para testar queries, compartilhar dúvidas e demonstrar exercícios em aula.

---

## 🧩 Passo a passo

### 1️⃣ Acesse o site
Entre em [db-fiddle.com](https://www.db-fiddle.com) ou [dbfiddle.uk](https://dbfiddle.uk). Você verá duas áreas principais: **Schema / Setup** (criação do banco) e **Query** (execução das consultas).

### 2️⃣ Escolha o SGBD
No menu suspenso, selecione o tipo de banco e a versão (exemplo: MySQL 8.0, PostgreSQL 15). Isso garante que as queries rodem igual às da sua disciplina.

### 3️⃣ Crie seu schema (tabelas e inserts)
```sql
CREATE TABLE aluno (
  id INT PRIMARY KEY,
  nome VARCHAR(100),
  curso VARCHAR(80)
);

INSERT INTO aluno VALUES (1, 'Mariana', 'ADS'), (2, 'João', 'Engenharia');
```

### 4️⃣ Escreva e execute suas queries
```sql
SELECT id, nome, curso FROM aluno WHERE curso = 'ADS';
```
Clique em **Run** e veja o resultado em formato de tabela.

### 5️⃣ Compartilhe seu trabalho
Use o botão **Share** para gerar um link único. Assim, qualquer pessoa pode abrir seu banco e ver os resultados.

---

## 🧠 Exemplos práticos

**Exemplo 1 — Consulta simples:**
```sql
CREATE TABLE livro (
  isbn VARCHAR(20) PRIMARY KEY,
  titulo TEXT,
  autor VARCHAR(100)
);

INSERT INTO livro VALUES ('978-0-123456-47-2', 'Algoritmos', 'Cormen');

SELECT * FROM livro;
```

**Exemplo 2 — JOIN entre tabelas:**
```sql
CREATE TABLE autor (id INT PRIMARY KEY, nome VARCHAR(80));
CREATE TABLE livro (id INT PRIMARY KEY, titulo VARCHAR(120), autor_id INT REFERENCES autor(id));

INSERT INTO autor VALUES (1, 'Ana'), (2, 'Carlos');
INSERT INTO livro VALUES (10, 'Redes', 1), (11, 'Sistemas', 2);

SELECT l.titulo, a.nome FROM livro l JOIN autor a ON l.autor_id = a.id;
```

---

## ⚙️ Erros comuns e soluções
- **Tabela vazia?** Verifique se o *setup* foi executado.  
- **Erro de sintaxe?** Confirme o dialeto SQL correto.  
- **Problemas com chaves estrangeiras?** Coloque `CREATE TABLE` e `INSERT` juntos no mesmo bloco.

---

## 🧾 Boas práticas
- Adicione comentários (`--`) explicando o que cada parte faz.  
- Use nomes claros: `aluno_id`, `livro_id`, etc.  
- Sempre envie o link do *fiddle* junto com seu exercício.

---

## 🔗 Recursos adicionais
- [DB Fiddle Oficial](https://www.db-fiddle.com)  
- [SQLBolt — Exercícios interativos de SQL](https://sqlbolt.com)  
- [W3Schools SQL Reference](https://www.w3schools.com/sql/)

---

## 🏁 Conclusão
O DB Fiddle é uma ferramenta poderosa e gratuita para praticar SQL. Em poucos minutos, você cria bancos, testa consultas e compartilha tudo com facilidade. Ideal para estudantes, professores e profissionais de banco de dados.

> 💡 **Dica extra:** Use esse tutorial como post fixo no seu portfólio para mostrar domínio em SQL e ferramentas de prática online!

