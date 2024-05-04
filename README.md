# Projeto Indivdual  Módulo 2 - Curso do Senac ~ Resilia ~ CNSeg - Análise de dados.

## Banco de Dados para o Sistema RESILIADATA

- **Este repositório contém a modelagem e implementação de um banco de dados para o sistema RESILIADATA, que visa auxiliar na avaliação das tecnologias utilizadas pelas empresas parceiras e seus colaboradores.**

### Descrição do Projeto

- O sistema RESILIADATA requer um banco de dados robusto para armazenar informações essenciais sobre empresas parceiras, tecnologias utilizadas e colaboradores associados. A modelagem do banco de dados inclui quatro entidades principais: Empresa, Tecnologia e Colaborador, com seus respectivos campos e relacionamentos.

**Objetivo:**

- O modelo de banco de dados proposto foi desenvolvido com o objetivo de simplificar o gerenciamento de empresas parceiras, suas áreas de atuação, tecnologias adotadas, colaboradores e também registrar as principais técnologias utilizadas pelas empresas parceiras. Essa estrutura robusta oferece uma organização eficiente para armazenar e acessar informações cruciais para empresas envolvidas em parcerias estratégicas.

**Entidades:**

* **Empresa:**
    * Representa as empresas parceiras que colaboram com a sua organização.
    * Campos:
        * `ID_Empresa`: INT - Número inteiro (chave primária)
        * `nome`: VARCHAR 
        * `CNPJ`: VARCHAR
        * `Endereço`: VARCHAR
        * `Telefone`: VARCHAR
        * `Email`: VARCHAR
        * `Area_atuacao`: VARCHAR

* **Tecnologia:**
    * Representa as tecnologias utilizadas pelas empresas parceiras.
    * Campos:
        * `ID_Tecnologia`:INT (chave primária)
        * `Nome`: VARCHAR
        * `Area`: VARCHAR
        * `Descricao`: VARCHAR
          
* **RegistroTecnologia:**
    * Registra quais técnologias as empresas parceiras parceiras estão útilizando em uma tabela separada.
    * Campos:
        * `ID_RegistroTec`: Número inteiro (chave primária)
        * `ID_Tecnologia`: Número inteiro (chave estrangeira para a tabela `Tecnologia`)
        * `ID_Empresa`: Número inteiro (chave estrangeira para a tabela `Empresa`)
     
* **Colaborador:**
    * Representa os colaboradores das empresas parceiras que trabalham em conjunto com a sua organização.
    * Campos:
        * `ID_Colaborador`: Número inteiro (chave primária)
        * `Nome`: String (255 caracteres)
        * `Cargo`: VARCHAR
        * `Setor`: VARCHAR
        * `Email`: String (100 caracteres) - Validar formato email
        * `Empresa Parceira_Área_ID`: Número inteiro (chave estrangeira para a tabela `Empresa-Parceira_Área`)
      
