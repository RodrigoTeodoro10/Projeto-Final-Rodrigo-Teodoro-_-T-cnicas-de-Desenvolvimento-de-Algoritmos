# Projeto Final – Rodrigo Teodoro  
### Disciplina: Técnicas de Desenvolvimento de Algoritmos  

## 📌 Descrição do Projeto
Este projeto consiste no desenvolvimento de um sistema CRUD simples utilizando PHP e MySQL, permitindo o cadastro e gerenciamento de **médicos** e **pacientes**.

O sistema realiza:
- Cadastro
- Listagem

Foram utilizados conceitos fundamentais de algoritmos, lógica e estruturas de programação.

---

## 🛠 Tecnologias Utilizadas
- PHP 8+
- MySQL/MariaDB
- Bootstrap 5
- HTML5 / CSS3

---

## 📁 Estrutura do Projeto
src/
├── conexao.php
├── medicos/
│ ├── cadastrar.php
│ └── listar.php
└── pacientes/
├── cadastrar.php
└── listar.php

database/
└── banco.sql

documentos/
├── pseudocodigo.md
├── algoritmo.md
└── fluxograma.png


---

## ▶ Como Executar o Projeto

1. Instale o **XAMPP** ou **WAMP**  
2. Coloque o projeto em:  
   - XAMPP → `C:\xampp\htdocs\clinica`  
   - WAMP → `C:\wamp64\www\clinica`  

3. Importe o banco de dados:
   - Acesse `http://localhost/phpmyadmin`
   - Crie o banco `clinica`
   - Importe o arquivo `database/banco.sql`

4. No navegador, abra:

http://localhost/clinica/medicos/cadastrar.php

http://localhost/clinica/pacientes/cadastrar.php


---

## 👨‍💻 Autor
**Rodrigo Teodoro**  
Projeto final da disciplina **Técnicas de Desenvolvimento de Algoritmos**.
# Pseudocódigo – CRUD Médicos e Pacientes

INÍCIO

    EXIBIR MENU PRINCIPAL
        1 - Cadastrar Médico
        2 - Cadastrar Paciente

    LER opção

    SE opção = 1 ENTÃO
        LER nome_do_médico
        LER especialidade
        INSERIR dados na tabela MÉDICOS
        EXIBIR "Médico cadastrado"

    SENÃO SE opção = 2 ENTÃO
        LER nome_do_paciente
        LER telefone
        INSERIR dados na tabela PACIENTES
        EXIBIR "Paciente cadastrado"

    SENÃO
        EXIBIR "Opção inválida"

FIM

          ┌───────────────┐
          │    INÍCIO     │
          └───────┬───────┘
                  │
       ┌──────────▼───────────┐
       │ Exibir Menu CRUD      │
       │ 1 - Médico            │
       │ 2 - Paciente          │
       └──────────┬───────────┘
                  │
         ┌────────▼───────────┐
         │ Ler opção do usuário│
         └────────┬───────────┘
                  │
     ┌────────────▼──────────────┐
     │ Opção = 1 ? (Médico)       │
     └───────┬─────────┬─────────┘
             │SIM       │NÃO
             │          │
 ┌───────────▼───┐    ┌─▼─────────────────┐
 │ Ler Nome       │    │ Opção = 2 ?       │
 │ Ler Especialidade│   │ (Paciente)       │
 └───────────┬────┘    └───────┬──────────┘
             │                 │
   ┌─────────▼────────┐   ┌────▼────────────┐
   │ Inserir no BD     │   │ Ler Nome        │
   │ tabela Médicos    │   │ Ler Telefone    │
   └─────────┬────────┘   └────┬────────────┘
             │                 │
   ┌─────────▼──────────┐ ┌────▼─────────────┐
   │ Exibir Sucesso      │ │ Inserir no BD    │
   │ Médico cadastrado   │ │ tabela Pacientes │
   └─────────┬──────────┘ └────┬─────────────┘
             │                 │
             └──────┬──────────┘
                    │
             ┌──────▼───────┐
             │    FIM       │
             └──────────────┘

# Linguagem Algorítmica – CRUD

Algoritmo CRUD_Clinica

Início
    Exibir "1 - Cadastrar Médico"
    Exibir "2 - Cadastrar Paciente"

    Leia opcao

    Se opcao = 1 então
        Leia nome
        Leia especialidade
        Chamar função Inserir_Medico(nome, especialidade)
    FimSe

    Se opcao = 2 então
        Leia nome
        Leia telefone
        Chamar função Inserir_Paciente(nome, telefone)
    FimSe

FimAlgoritmo


