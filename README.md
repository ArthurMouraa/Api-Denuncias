=======
# 🐾 S.O.S Fauna

O S.O.S Fauna é uma plataforma dedicada ao combate aos maus-tratos contra animais. Esta é a versão inicial do projeto (v1), que segue em constante evolução para oferecer melhorias contínuas.

### 🛠️ Banco de dados - Diagrama Entidade Relacionamento

```mermaid
erDiagram
    ORGAOS {
        VARCHAR id PK
        VARCHAR nome
        VARCHAR cnpj
        TEXT descricao
        VARCHAR telefone
        VARCHAR rede_social
        VARCHAR rua
        INT numero
        VARCHAR bairro
        VARCHAR cidade
        VARCHAR cep
        LONGBLOB foto_perfil
        BOOLEAN acesso
        DATETIME data_criacao
    }
    USUARIOS {
        VARCHAR id PK
        VARCHAR cpf
        VARCHAR nome
        DATETIME dt_nascimento
        VARCHAR telefone
        BLOB foto_perfil
        DATETIME dataCriacao
        BOOLEAN acesso
        VARCHAR email
        VARCHAR public_id
    }
    DENUNCIAS {
        VARCHAR id PK
        VARCHAR animal
        VARCHAR denunciado
        TEXT descricao
        DATE data_ocorrido
        TIME hora_ocorrido
        VARCHAR bairro
        VARCHAR numero
        VARCHAR rua
        VARCHAR cep
        DATETIME data_criacao
        ENUM status_denuncia
        VARCHAR usuario_id FK
        VARCHAR orgaos_id FK
    }
    ANIMAIS_ADOCAO {
        INT id PK
        VARCHAR nome
        VARCHAR especie
        INT idade
        ENUM sexo
        LONGBLOB foto
        DATETIME data_criacao
        ENUM status_adocao
        VARCHAR orgaos_id FK
    }

    USUARIOS ||--o{ DENUNCIAS : realiza
    ORGAOS ||--o{ DENUNCIAS : completa
    ORGAOS ||--o{ ANIMAIS_ADOCAO : realiza

```

## 🌟 Colaboradores

### 💻 Backend

#### Arthur Moura  
[🔗 Linkedin](https://www.linkedin.com/in/arthur-moura-20462524b/) | [🐙 Github](https://github.com/ArthurMouraa)

#### Luiz Filipe  
[🔗 Linkedin](https://www.linkedin.com/in/luiz-felipe-35265b1a8/) | [🐙 Github](https://github.com/fluizz00)

#### Maycon Gabriel  
[🔗 Linkedin](https://www.linkedin.com/in/maycon-gabriel-388421214/) | [🐙 Github](https://github.com/May154)

#### Armando Alves  
[🔗 Linkedin](https://www.linkedin.com/in/armando-alves-878356151/) | [🐙 Github](https://github.com/ArmandoMartins1)

#### Tallys Labanca  
[🔗 Linkedin](https://www.linkedin.com/in/tallys-labanca/) | [🐙 Github](https://github.com/helelys)





