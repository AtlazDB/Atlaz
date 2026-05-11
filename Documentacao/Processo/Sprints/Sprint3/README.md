# AtlasTech - Projeto IPEM
# Documentação - Sprint 3

<p align="center">
      <h2 align="center"> AtlasTech </h2>
</p>

<p align="center">
  | <a href ="#desafio"> Desafio</a>  |
  <a href ="#us"> User Stories</a>  |   
</p>

> Status da Sprint: Em Andamento ⚙️

---

## 🏅 Desafio <a id="desafio"></a>
Finalizar o ecossistema do projeto com foco em segurança e governança de dados. O desafio desta etapa é implementar o controle de acesso (Autenticação e Autorização), permitir a rastreabilidade através do histórico de lançamentos e automatizar os alertas de manutenção preventiva (como a troca de óleo prevista no boletim físico), transformando dados brutos em inteligência operacional.

---


| Capacidade estimada da Equipe por Sprint:               | 35                                                         |
| ------------------------------------------------------- | ---------------------------------------------------------- |
| Meta da Sprint:                                         | User Stories de rank 1 e rank 2 (Total de 33 Story Points) |
| Previsão da Sprint (extras, sem compromisso de entrega) | —                                                          |


| Rank | ID   | Prioridade | User Story                                                                                                      | Estimativa | Sprint |
| ---- | ---- | ---------- | --------------------------------------------------------------------------------------------------------------- | ---------- | ------ |
| 1    | US07 | Média      | Como administrador, quero visualizar o histórico de abastecimentos para conferência de dados.                   | 8          | 3      |
| 2    | US08 | Média      | Como administrador, quero editar os registros de abastecimentos e ocorrencias                                   | 8          | 3      |
| 3    | US09 | Baixa      | Como administrador, quero filtrar os gastos por tipo de veículo (Utilitário vs Passeio) para análise de custos. | 8          | 3      |
| 4    | US10 | Baixa      | Como administrador, quero receber notificações referente a manutenções preventivas de viaturas.                 | 5          | 3      |




---

## 📋 User Stories & DoD <a id="us"></a>

Nesta seção, detalhamos as histórias de usuário e seus respectivos **DoD (Definition of Done)** específicos.

### **US07 - Histórico de Conferência**
> **Como técnico, quero visualizar o histórico registros para conferência de dados.**

* **Prioridade:** Média | **Estimativa:** 8h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Interface de "Meus Lançamentos" restrita aos dados inseridos pelo usuário logado.
    * Funcionalidade de ordenação por data e filtro de viatura.
    * Visualização detalhada de cada registro (Km, litros, valor e nota fiscal).

### **US08 - Autogestão do Técnico**
> **Como administrador, quero visualizar e editar os registros de abastecimento/deslocamento.**

* **Prioridade:** Média | **Estimativa:** 13h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Tela de listagem com todos os apontamentos realizados.
    * Funcionalidade de ordenação por data e filtro de tecnico e viatura.
    * Visualização detalhada de cada registro (Km, litros, valor e nota fiscal).

### **US09 - Análise por Categoria de Frota**
> **Como administrador, quero filtrar os gastos por veículo e tecnico para análise de custos.**

* **Prioridade:** Baixa | **Estimativa:** 13h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Inclusão de filtros cruzados que permitem extrair relatórios específicos de um único colaborador ou prefixo de viatura, facilitando a auditoria de deslocamentos e gastos.
    * Ajuste nos seletores de data para permitir extrações de intervalos específicos (Início/Fim).
    * Relatório de exportação refletindo o filtro.

### **US10 - Alertas de Manutenção Preventiva**
> **Como administrador, quero receber notificações referente a manutenções preventivas de viaturas.**

* **Prioridade:** Baixa | **Estimativa:** 13h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Implementação dos campos de "Última Troca de Óleo" e "Próxima Troca (Km)" conforme Boletim de Tráfego.
    * Sistema de alerta visual (ícone ou cor diferenciada) quando a quilometragem atual estiver a menos de 500km da revisão prevista.
    * Notificação automática na tela principal do administrador ao identificar veículos com manutenção vencida.

---

## 🏆 Critérios de Conclusão da Sprint
Para o fechamento da Sprint 3, a equipe deve garantir:
* Segurança: Técnicos impedidos de acessar rotas administrativas via URL ou interface.
* Integração: Todos os filtros de histórico e Dashboard funcionando com dados reais do Supabase.
* Pull Requests aprovados e código consolidado na branch `main`.
* README da Sprint atualizado com as evidências de segurança e alertas funcionais.

--- 

# Tasks🛠️

### `[Back-End]`

| Chave      | Task                                                                                                                                                     | Responsável   | SP  | Status       | Prazo de Entrega | Data de Entrega                                                                                   |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- | --- | ------------ | ---------------- | ------------------------------------------------------------------------------------------------- |
| US09 - T6  | Método GET que recebe duas datas (data_inicio, data_fim) e devolve a quantidade de registros no intervalo                                                | Leandro       | 3   | Não Iniciada | 17/05            |                                                                                                   |
| US09 - T1  | Método GET que recebe um id de viatura e devolve o consumo médio dela                                                                                    | Samuel        | 3   | Não iniciada | 17/05            |                                                                                                   |
| US09  - T2 | Cadastro de CNH e exibição de viaturas de acordo com tipo de habilitação do tecnico                                                                      | Gabriel Rocha | 5   | Concluída✅   | 17/05            | [09/05](https://github.com/AtlazDB/Atlaz-BackEnd/commit/19ce1e5ea6094bb9be1c2994cbf6873339864e88) |
| US08 - T3  | Não permitir inativação de tecnico/viatura durante ocorrencia                                                                                            | João          | 2   | Não iniciada | 17/05            |                                                                                                   |
| US07- T1   | Histórico de ocorrencias para visualização dos tecnicos                                                                                                  | Gabriel Nunes | 3   | Não iniciada | 17/05            |                                                                                                   |
| US10 - T2  | Migration para cadastro de km para troca de oleo, atualizar post e criar get para enviar para tabela de mais info de viaturas (default = após 10 mil km) | Leandro       | 3   | Não iniciada | 17/05            |                                                                                                   |



### `[Front-End]`

| Chave     | Task                                                              | Responsável     | SP  | Status       | Prazo de Entrega | Data de Entrega |
| --------- | ----------------------------------------------------------------- | --------------- | --- | ------------ | ---------------- | --------------- |
| US08 - T1 | Melhorias na pagina de Registros (Campos para filtrar e exibição) | Leonardo        | 3   | Não iniciada | 17/05            |                 |
| US09 - T3 | Remover opção em campo/em uso do cadastro de tecnico/viatura      | Leonardo        | 1   | Não iniciada | 17/05            |                 |
| US07 - T2 | Histórico de ocorrencias para visualização dos tecnicos           | Maria           | 3   | Não iniciada | 17/05            |                 |
| US07 - T3 | Refatoração nas telas de cadastro                                 | Maria           | 2   | Não iniciada | 17/05            |                 |
| US10 - T3 | Responsividade nas telas de administrador                         | Maria           | 2   | Não iniciada | 17/05            |                 |
| US09 - T4 | Refatoração da tela de Dashboard                                  | Gabriel Valente | 3   | Não iniciada | 17/05            |                 |
| US10 -T1  | Tela de mais informações de veículo                               | Ryan            | 2   | Não iniciada | 17/05            |                 |
