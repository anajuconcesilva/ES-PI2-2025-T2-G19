- Feito pela aluna: Sofia de Sousa
       - RA: 25005435

Para executar o código precisa executar script SQL


create database ProjetoNotaDez;

drop database ProjetoNotaDez;

use ProjetoNotadez;

CREATE TABLE Docente (
    ID_Docente INT PRIMARY KEY AUTO_INCREMENT,
    Nome_Docente VARCHAR(100) NOT NULL,
    Email VARCHAR(100) UNIQUE NOT NULL,
    Telefone_Celular VARCHAR(20),
    Senha VARCHAR(100) NOT NULL
);

CREATE TABLE Instituicao (
  ID INT AUTO_INCREMENT PRIMARY KEY,
  Nome VARCHAR(150) NOT NULL,
  Endereco VARCHAR(255)
);

CREATE TABLE Curso (
    ID_Curso INT PRIMARY KEY AUTO_INCREMENT,
    Nome_Curso VARCHAR(100) NOT NULL,
    Periodo VARCHAR(30),
    Codigo INT UNIQUE NOT NULL,
    ID_Instituicao INT,
    FOREIGN KEY (ID_Instituicao) REFERENCES Instituicao(ID)
);

CREATE TABLE Disciplina (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome_Disciplina VARCHAR(100) NOT NULL,
    Sigla_Disciplina VARCHAR(20),
    Codigo_Disciplina VARCHAR(20),
    Periodo_Curso INT,
    ID_Curso INT,
    FOREIGN KEY (ID_Curso) REFERENCES Curso(ID_Curso)
);
    
CREATE TABLE Aluno (
	ID INT auto_increment PRIMARY KEY,
    RA varchar(50) UNIQUE NOT NULL,
    Nome_Aluno VARCHAR(100) NOT NULL
);

select * from Docente;

select * from Curso;

select * from Aluno;

select * from Instituicao;

select * from Disciplina;
