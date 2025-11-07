---
layout: post
title: "Como Usar o DB Fiddle para Rodar Bancos de Dados Online"
author: Lux
date: 2025-10-31
categories: [Banco de Dados, Tutoriais, Ferramentas]
description: "Aprenda passo a passo a utilizar o DB Fiddle para testar e executar seus scripts SQL de forma online, rápida e prática."
---

# 🧠 Tutorial — Como Usar o DB Fiddle para Rodar Bancos de Dados Online

## 👤 Autor
Lux

## 🎯 Tema Principal
Uso da plataforma **DB Fiddle** para criar, testar e executar comandos SQL diretamente no navegador.

## 🧩 Relação com os Conteúdos da Disciplina
Este tutorial se relaciona ao conteúdo de **Gerenciamento de Banco de Dados Relacional**, permitindo compreender na prática a execução de **comandos SQL** sem precisar instalar softwares locais, como MySQL ou PostgreSQL.

---

## 🚀 Passo a Passo

### 1️⃣ Acesse o site do DB Fiddle
Entre no site oficial: [https://www.db-fiddle.com](https://www.db-fiddle.com)

Você verá uma tela dividida em duas partes:
- À esquerda: onde você escreve os **comandos SQL de criação de tabelas e inserção de dados**.
- À direita: onde aparecem os **resultados das consultas (queries)**.

---

### 2️⃣ Escolha o SGBD
No canto superior esquerdo, selecione o tipo de banco de dados que deseja usar:
- MySQL
- PostgreSQL
- SQLite
- Oracle
- SQL Server

💡 *Dica:* escolha o mesmo sistema que você está estudando ou utilizando no projeto.

---

### 3️⃣ Crie seu banco de dados
Digite os comandos SQL no painel esquerdo.  
Por exemplo:

```sql
CREATE TABLE Alunos (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100),
    curso VARCHAR(50)
);

INSERT INTO Alunos (nome, curso) VALUES
('João Silva', 'Engenharia'),
('Maria Souza', 'Sistemas de Informação');
