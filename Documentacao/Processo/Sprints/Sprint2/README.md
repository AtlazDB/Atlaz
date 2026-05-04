# AtlasTech - Projeto IPEM
# Documentação - Sprint 2

<p align="center">
      <h2 align="center"> AtlasTech </h2>
</p>

<p align="center">
  | <a href ="#desafio"> Desafio</a>  |
  <a href ="#us"> User Stories</a>  |   
  <a href ="#dor">DoR</a>  |
</p>

> Status da Sprint: Em Andamento ⚙️

---

## 🏅 Desafio <a id="desafio"></a>
Expandir o ecossistema do sistema garantindo a gestão da frota e dos usuários. O foco é permitir o controle administrativo completo (Viaturas e Técnicos), implementar as travas de segurança de quilometragem para evitar erros humanos e fornecer a primeira visão analítica de consumo médio para os gestores.

---

## 📋 User Stories & DoD <a id="us"></a>

Nesta seção, detalhamos as histórias de usuário e seus respectivos **DoD (Definition of Done)** específicos.

### **US03 - Gestão de Viaturas**
> **Como administrador, quero cadastrar viaturas para manter a frota atualizada no sistema.**

* **Prioridade:** Alta | **Estimativa:** 13h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Interface funcional para Cadastro/Edição/Listagem (CRUD) de veículos.
    * Campos obrigatórios conforme Boletim de Tráfego: Marca, Modelo, Ano, Placa, Prefixo e Tipo de Combustível.
    * Persistência dos dados no **Supabase** garantindo que o Prefixo seja único.

### **US04 - Gestão de Técnicos**
> **Como administrador, quero cadastrar técnicos para que eles possam acessar o sistema e realizar apontamentos.**

* **Prioridade:** Alta | **Estimativa:** 8h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Interface para cadastro de funcionários com Nome e Número da Carteira Funcional (conforme Boletim).
    * Vinculação do usuário ao perfil de "Técnico" para acesso restrito à tela de apontamento.
    * Lista de técnicos ativos disponível para seleção no formulário de jornada.

### **US05 - Validação de Integridade (KM)**
> **Como administrador, quero validar a quilometragem inserida para garantir a integridade dos dados.**

* **Prioridade:** Alta | **Estimativa:** 13h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Regra de Backend: Bloqueio de inserção se o KM de Saída for menor que o último KM de Chegada registrado para aquela viatura.
    * Regra de Frontend: Exibição de alerta impeditivo caso o usuário tente finalizar com KM incoerente.
    * Log de erros para tentativas de inserção inválidas.

### **US06 - Dashboard de Consumo Médio**
> **Como administrador, quero visualizar um Dashboard de consumo para monitorar a eficiência da frota.**

* **Prioridade:** Média | **Estimativa:** 20h | **Status:** ⚙️
* **DoD (Critérios de Sucesso):**
    * Gráficos em tempo real utilizando os dados de Abastecimento (Litros) e KM Rodados.
    * Cálculo automático da média de consumo ($km/l$) por veículo e por período.
    * Filtros por Prefixo da Viatura e intervalo de datas (mês corrente).

---

## 🏆 Critérios de Conclusão da Sprint
Para o fechamento da Sprint 2, a equipe deve garantir:
* Pull Requests aprovados por membros da TechForce seguindo o **GitHub Flow**.
* Código funcional integrado à branch `main`.
* Documentação do README da Sprint atualizada com evidências dos novos cadastros e do Dashboard.

---
# BurndownChart

<img width="1188" height="575" alt="image" src="https://github.com/user-attachments/assets/03a60854-bd60-4af5-8044-cd25d258cf94" />


--- 

# 🎥 Demonstração da aplicação

> Clique na imagem abaixo para assistir ao vídeo no YouTube.

[![Vídeo da aplicação](https://img.youtube.com/vi/rNZketvz7Ho/maxresdefault.jpg)](https://www.youtube.com/watch?v=rNZketvz7Ho)


--- 
## Tasks realizadas nessa sprint 🛠️

### `[Back-End]`

| Chave     | Task                                                                  | Responsável     | SP  | Status      |
| --------- | --------------------------------------------------------------------- | --------------- | --- | ----------- |
| TT - T1   | Refatorar nomes de classes, metodos e atributos do BackEnd para EN-US | João            | 3   | ✅ Concluído |
| US03 - T2 | Criar DTO para Response de viatura                                    | Samuel          | 1   | ✅ Concluído |
| US03 - T4 | Adicionar tipo de combustivel na tabela viatura                       | Gabriel Rocha   | 1   | ✅ Concluído |
| US03 - T5 | Atualizar Request e Response de veiculo                               | Gabriel Rocha   | 1   | ✅ Concluído |
| US03 - T7 | Criar Migration atualizando os status de usuario e viatura            | João            | 1   | ✅ Concluído |
| US05 - T1 | Atualizar tabela viatura para receber KM atual                        | Gabriel Nunes   | 2   | ✅ Concluído |
| US06 - T2 | Endpoint GET /api/dashboard/resumo                                    | Leandro         | 5   | ✅ Concluído |
| US06 - T3 | DTO Response abastecimento                                            | Gabriel Rocha   | 2   | ✅ Concluído |
| US06 - T4 | FIX - Corrigir exibição de dados no dashboard                         | Leandro         | 1   | ✅ Concluído |


### `[Front-End]`

| Chave     | Task                                              | Responsável     | SP  | Status      |
| --------- | ------------------------------------------------- | --------------- | --- | ----------- |
| US01 - T1 | Refatorar Telas de abastecimento                  | Maria           | 1   | ✅ Concluído |
| US02 - T2 | Refatorar Formulário principal                    | Maria           | 1   | ✅ Concluído |
| US03 - T1 | Tela de Viaturas cadastradas                      | Leonardo        | 2   | ✅ Concluído |
| US03 - T3 | Tela para cadastro de viaturas                    | Ryan            | 1   | ✅ Concluído |
| US03 - T6 | Integração das telas de viaturas com a API                                | Leandro         | 1   | ✅ Concluído |
| US04 - T1 | Adaptar a tela principal com login                | Maria           | 5   | ✅ Concluído |
| US04 - T2 | Tela de cadastro/exibição de tecnicos cadastrados | Gabriel Rocha   | 5   | ✅ Concluído |
| US04 - T3 | Integração das telas de tecnico com API                                | Leandro         | 3   | ✅ Concluído |
| US05 - T2 | Integração dos métodos de validação com API                           | Leandro         | 3   | ✅ Concluído |
| US06 - T1 | Tela Dashboard do administrador                   | Gabriel Valente | 5   | ✅ Concluído |
