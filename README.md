# 🚀 Desafio de Projeto: Modelagem e Transformação de Dados com DAX no Power BI

## 📄 Descrição do Projeto
Este projeto foi desenvolvido como parte de um desafio de modelagem de dados proposto pela DIO e NTTDATA, com o objetivo de criar um modelo analítico no Power BI utilizando o **esquema estrela** (star schema). A partir de uma tabela de dados financeiros (`Financial Sample`), foram criadas tabelas de dimensões e uma tabela de fatos para facilitar a análise e visualização de dados.

---

## 📂 Estrutura do Projeto
O projeto foi estruturado a partir de uma tabela principal (`Financial Sample`), da qual foram derivadas as seguintes tabelas:

- **Financials_origem**: Tabela de backup (oculta) para referência.
- **D_Produtos**: Contém colunas como `ID_produto`, `Produto`, média de unidades vendidas, média e mediana do valor de vendas, e valores máximos e mínimos de venda.
- **D_Produtos_Detalhes**: Inclui `ID_produtos`, `Discount Band`, `Sale Price`, `Units Sold`, e `Manufacturing Price`.
- **D_Descontos**: Composta por `ID_produto`, `Discount`, e `Discount Band`.
- **D_Detalhes**: Agrega informações adicionais sobre vendas que não foram contempladas nas demais tabelas de dimensão.
- **D_Calendário**: Criada utilizando DAX (`CALENDAR`) para facilitar a análise temporal dos dados.
- **F_Vendas**: Tabela de fatos contendo colunas como `SK_ID`, `ID_Produto`, `Produto`, `Units Sold`, `Sales Price`, `Discount Band`, `Segment`, `Country`, `Salers`, `Profit`, e `Date`.

---

## 🛠️ Processo de Construção

1. **Criação das Tabelas**  
   As tabelas de dimensão e a tabela de fatos foram derivadas da tabela `Financial Sample`, organizando os dados de forma a otimizar a análise. Cada tabela foi estruturada com colunas específicas para facilitar consultas e relacionamentos.

2. **Funções DAX**

 ![image](https://github.com/user-attachments/assets/959f7951-c25d-412e-b9f2-75746c4d21b9)
 
   Várias funções DAX foram utilizadas para transformar e manipular os dados, incluindo:
   - `CALENDAR` para gerar a tabela de calendário, que possibilita análise por data.
   - Cálculos agregados como médias, medianas, e valores máximos e mínimos em **D_Produtos**.

4. **Reorganização das Colunas**  
   As colunas foram reorganizadas para facilitar a visualização e análise dos dados na tabela de fatos **F_Vendas**.

5. **Construção de Colunas Calculadas**  
   Colunas adicionais foram criadas para enriquecer o modelo de dados, incluindo um índice de produtos gerado com base em condições específicas.

![image](https://github.com/user-attachments/assets/628bf7a0-b9a5-4695-a112-ccc3ed74e935)
![image](https://github.com/user-attachments/assets/db324d86-6fe5-425d-89bd-1713cc345bc1)


---

## 🌟 Esquema Estrela (Star Schema)

O modelo de dados segue o **esquema estrela**, com a tabela de fatos (**F_Vendas**) centralizando as informações principais e se relacionando com as tabelas de dimensão. Esse modelo permite consultas rápidas e eficientes, facilitando a geração de relatórios e dashboards.

>  ![image](https://github.com/user-attachments/assets/f98f5f3e-6201-4251-a075-37ad204510b9)


---

## 🛠️ Tecnologias Utilizadas

- **Power BI**: Ferramenta para criação de relatórios e dashboards.
- **DAX (Data Analysis Expressions)**: Linguagem para criação de colunas calculadas e manipulação de dados no Power BI.

---

## 📊 Como Executar o Projeto

1. Abra o arquivo `.pbix` no Power BI Desktop.
2. Explore as tabelas de dimensão e a tabela de fatos.
---

## 📌 Considerações Finais

Este projeto oferece uma estrutura de dados sólida para análise financeira. O uso de DAX possibilitou uma transformação eficaz dos dados, com tabelas de dimensão bem definidas e um modelo de dados otimizado. O repositório GitHub serve como referência para outros profissionais e recrutadores, permitindo uma visão do processo de construção e organização dos dados.

---

<div align="center">
    Feito com ❤️ por Matheus Guerra
</div>
