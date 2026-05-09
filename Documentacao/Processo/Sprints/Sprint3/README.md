# AtlasTech - Projeto IPEM
# Documentação - Sprint 3

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
Finalizar o ecossistema do projeto com foco em segurança e governança de dados. O desafio desta etapa é implementar o controle de acesso (Autenticação e Autorização), permitir a rastreabilidade através do histórico de lançamentos e automatizar os alertas de manutenção preventiva (como a troca de óleo prevista no boletim físico), transformando dados brutos em inteligência operacional.

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
