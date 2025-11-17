# 📘 BookTrack – Documentação Completa

Bem-vindo(a) à documentação oficial do **BookTrack**, sistema para gerenciamento de bibliotecas físicas e digitais.  
Aqui você encontrará todos os diagramas UML organizados, com explicações detalhadas sobre cada componente, ator e interação.

> **Imagens:** pasta `/ImagesPlantUML/`  

---

# 🏗️ Diagrama de Arquitetura (C4 / Container)

**Objetivo:** Apresentar a visão de alto nível do sistema, mostrando como os contêineres principais se comunicam.  
Ajuda a entender a arquitetura do BookTrack e o fluxo de dados entre os módulos principais.

**Componentes principais:**
- **Frontend** – Interface de usuário web e mobile.  
- **Backend** – Processa a lógica de negócio, valida dados e integra com o banco de dados e sistemas externos.  
- **Banco de Dados** – Armazena usuários, livros, empréstimos, reservas e multas.  
- **Sistema de Pagamentos Externo** – Processa pagamentos de multas e taxas.

**Diagrama:**  
![Diagrama de Arquitetura](ImagesPlantUML/Diagrama%20de%20Arquitetura.png)

---

# 🎯 Diagrama de Casos de Uso

**Objetivo:** Mostrar os atores e as funcionalidades que eles podem executar no sistema, permitindo visualizar **quem faz o quê**.

**Atores principais:**
- **Leitor** – Reservar livros, realizar empréstimos, devolver livros e pagar multas.  
- **Bibliotecário** – Gerenciar acervo, aprovar reservas, registrar devoluções e aplicar multas.  
- **Sistema de Pagamentos** – Processar pagamentos de multas e taxas.

**Diagrama:**  
![Diagrama de Casos de Uso](ImagesPlantUML/Diagrama%20de%20Casos%20de%20Uso.png)

---

# 🧱 Diagrama de Classes

**Objetivo:** Representar a **estrutura lógica** do sistema, incluindo entidades, atributos, métodos e relacionamentos.

**Principais classes:**
- **Livro** – Título, autor, categoria e status (disponível, reservado, emprestado).  
- **Usuário** – Nome, matrícula, tipo (leitor ou bibliotecário) e histórico de empréstimos.  
- **Empréstimo** – Data de retirada, devolução e multas aplicadas.  
- **Multa** – Valor, status do pagamento e data de vencimento.

**Diagrama:**  
![Diagrama de Classes](ImagesPlantUML/Diagrama%20de%20Classes.png)

---

# 🔗 Diagramas de Comunicação

**Objetivo:** Mostrar as **interações entre objetos** durante cada caso de uso, detalhando a troca de mensagens.

## UC-05 – Realizar Reserva
**Descrição:** O leitor solicita a reserva de um livro, o sistema valida a disponibilidade e registra a reserva.  
![UC-05 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunica%C3%A7%C3%A3o%20%E2%80%93%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
**Descrição:** O leitor retira um livro, o sistema verifica reservas e atualiza o status do livro e do empréstimo.  
![UC-06 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunica%C3%A7%C3%A3o%20%E2%80%93%20UC-06%20-%20Realizar%20Empr%C3%A9stimo.png)

## UC-07 – Registrar Devolução
**Descrição:** O leitor devolve o livro, o sistema atualiza o status e calcula multas se houver atraso.  
![UC-07 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunica%C3%A7%C3%A3o%20%E2%80%93%20UC-07%20-%20Registrar%20Devolu%C3%A7%C3%A3o.png)

## UC-10 – Pagar Multa
**Descrição:** O leitor efetua o pagamento da multa, o sistema confirma a transação com o sistema externo.  
![UC-10 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunica%C3%A7%C3%A3o%20%E2%80%93%20UC-10%20-%20Pagar%20Multa.png)

---

# ⏳ Diagramas de Estado

**Objetivo:** Mostrar como os objetos mudam de estado ao longo do tempo.

- **Ciclo de Vida do Livro** – Disponível, reservado, emprestado, em manutenção.  
  ![Ciclo de Vida do Livro](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Ciclo%20de%20Vida%20do%20Livro.png)

- **Estado do Empréstimo** – Pendente, ativo, concluído, atrasado.  
  ![Estado do Empréstimo](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Emprestimo.png)

- **Estado da Multa** – Aberta, paga, em disputa.  
  ![Estado da Multa](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Multa.png)

---

# 💽 Diagrama de Implementação

**Objetivo:** Representar os nós físicos onde os componentes do sistema estão implantados (servidores, clientes e bancos de dados).  

**Diagrama:**  
![Diagrama de Implementação](ImagesPlantUML/Diagrama%20de%20Implementa%C3%A7%C3%A3o.png)

---

# 🗃️ Modelo de Dados (DER)

**Objetivo:** Exibir tabelas do banco de dados e seus relacionamentos, permitindo entender a modelagem de dados do sistema.

**Diagrama:**  
![Diagrama de Modelagem de Dados](ImagesPlantUML/Diagrama%20de%20Modelagem%20De%20Dados.png)

---

# 🕒 Diagramas de Sequência

**Objetivo:** Mostrar o fluxo temporal das mensagens entre componentes durante cada caso de uso.

## UC-05 – Realizar Reserva
![Sequência UC-05](ImagesPlantUML/Diagrama%20de%20Sequ%C3%AAncia%20%E2%80%93%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
![Sequência UC-06](ImagesPlantUML/Diagrama%20de%20Sequ%C3%AAncia%20%E2%80%93%20UC-06%20-%20Realizar%20Empr%C3%A9stimo.png)

## UC-07 – Registrar Devolução
![Sequência UC-07](ImagesPlantUML/Diagrama%20de%20Sequ%C3%AAncia%20%E2%80%93%20UC-07%20-%20Registrar%20Devolu%C3%A7%C3%A3o.png)

## UC-10 – Pagar Multa
![Sequência UC-10](ImagesPlantUML/Diagrama%20de%20Sequ%C3%AAncia%20%E2%80%93%20UC-10%20-%20Pagar%20Multa.png)

---

# 📌 Observações e Dicas

- A pasta `ImagesPlantUML` deve estar no **mesmo nível** do arquivo `README.md`.  
- Os nomes das imagens foram codificados com `%20` e UTF-8, mas podem ser renomeados para simplificar.  
- Esta documentação é útil para desenvolvedores, testadores e stakeholders.  

---

# 📞 Suporte

Posso gerar:  

- ✔ PDF da documentação completa  
- ✔ README estilizado com sumário automático  
- ✔ README com badges profissionais  
- ✔ Versão com nomes de imagens sem espaços e acentos  
- ✔ Organização completa do repositório
