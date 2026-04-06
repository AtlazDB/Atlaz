# AtlasTech - Projeto IPEM
# Documentação - Sprint 1

<p align="center">
      <h2 align="center"> AtlasTech </h2>
</p>

<p align="center">
  | <a href ="#desafio"> Desafio</a>  |
  <a href ="#us"> User Stories</a>  |   
  <a href ="#dor">DoR</a>  |
</p>

> Status da Sprint: Sprint Review

---

## 🏅 Desafio <a id="desafio"></a>
Estabelecer o fluxo funcional de entrada e saída de dados de abastecimento. Isso inclui a criação da interface de lançamento para o técnico e o motor de exportação de relatórios para o administrador, garantindo a integridade mínima das informações coletadas para o sistema IPEM.

---



| Capacidade estimada da Equipe por Sprint:               | 45                                                         |
| ------------------------------------------------------- | ---------------------------------------------------------- |
| Meta da Sprint:                                         | User Stories de rank 1 e rank 2 (Total de 33 Story Points) |
| Previsão da Sprint (extras, sem compromisso de entrega) | —                                                          |


| Rank | Prioridade | User Story                                                                                         | Estimativa | Sprint |
| ---- | ---------- | -------------------------------------------------------------------------------------------------- | ---------- | ------ |
| 1    | Alta       | Como técnico, quero registrar um abastecimento para digitalizar as informações da planilha física. | 13         | 1      |
| 2    | Alta       | Como administrador, quero exportar os dados mensais para facilitar o input manual no sistema SGI.  | 20         | 1      |


---
## 📋 User Stories & DoD <a id="us"></a>

Nesta seção, detalhamos as histórias de usuário e seus respectivos **DoD (Definition of Done)**, que são os critérios específicos para considerar cada funcionalidade concluída.

### **US01 - Registro de Jornada e Abastecimento**
> **Como técnico, quero registrar um abastecimento para digitalizar as informações da planilha física.**

* **Prioridade:** Alta
* **Estimativa:** 13h
* **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Interface em **Vue.js** com os campos obrigatórios do SGI: Motivo, Requisitante, Destino, Hodômetro (Saída/Chegada) e Horários.
    * Campos específicos para Abastecimento (Opcionais): Litros, Valor Total e Nº da Nota Fiscal.
    * Regra de Negócio: Cálculo automático de "KM Rodados" e validação para impedir Hodômetro de chegada menor que o de saída.
    * Integração: Persistência no **Docker** via API Java/Spring Boot conectando os dados ao Prefixo da viatura.
    * Feedback visual ao usuário e opção de anexar foto da NF (se houver).

---

### **US02 - Exportação SGI**
> **Como administrador, quero exportar os dados mensais para facilitar o input manual no sistema SGI.**

* **Prioridade:** Alta
* **Estimativa:** 20h
* **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Interface administrativa contendo botão de exportação de dados.
    * Geração de relatório em formato compatível (CSV ou Excel) com os campos exigidos pelo SGI.
    * Implementação de filtro para garantir a exportação correta do período mensal.
    * Garantia de que o arquivo gerado pode ser baixado e aberto sem erros de formatação.

---

## 🏃‍ DoR - Definition of Ready (Sprint 1) <a id="dor"></a>
Estes critérios garantem que o time tem todos os insumos necessários para iniciar o desenvolvimento desta Sprint:

* **Clareza**: User Stories escritas com objetivos de negócio e critérios de aceitação básicos definidos.
* **Modelagem**: Estrutura das tabelas de `abastecimento` e `viaturas` configuradas no banco de dados.
* **Integração**: Ambiente Java/Spring Boot e Container Docker devidamente configurados.
* **Design**: Protótipo de baixa ou média fidelidade da tela de lançamento validado no **Figma**.
* **Requisitos SGI**: Definição clara do layout de colunas necessário para a exportação de dados.

---

## 🏆 Critérios de Conclusão da Sprint
Para o fechamento da Sprint 1, a equipe deve atender aos seguintes requisitos gerais:
* Pull Requests revisados e aprovados seguindo o fluxo do **GitHub Flow**.
* Integração contínua: Código consolidado na branch `main` sem quebras de build.
* Documentação técnica: README da sprint atualizado com o status final das entregas.
  
  
---
# BurndownChart

<img width="1391" height="682" alt="image" src="https://github.com/user-attachments/assets/9dfabdff-f071-4d19-a968-6689f892cfd2" />

--- 

# 🎥 Demonstração da aplicação

> Clique na imagem abaixo para assistir ao vídeo no YouTube.

[![Vídeo da aplicação](https://img.youtube.com/vi/MP2xFfE2Bcs/maxresdefault.jpg)](https://www.youtube.com/watch?v=MP2xFfE2Bcs)

