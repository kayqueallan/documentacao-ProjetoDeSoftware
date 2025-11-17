# 📘 BookTrack  
Documentação de Arquitetura de Software

🚀 Bem-vindo(a) à documentação do Projeto BookTrack!  
Este repositório concentra toda a documentação técnica de arquitetura, design e modelagem do software BookTrack. Aqui estão reunidos diversos diagramas UML e documentos visuais que explicam a estrutura, o funcionamento e as interações do sistema, oferecendo uma compreensão detalhada e organizada para desenvolvedores, analistas e demais interessados no projeto.

---

# 📖 Sobre o Sistema
O BookTrack é um sistema projetado para gerenciar bibliotecas físicas e digitais.  
Ele permite que usuários realizem:

- Empréstimos e reservas de livros  
- Leitura e avaliação de ebooks  
- Acompanhamento do histórico de leitura  

Para bibliotecários, o sistema oferece:

- Controle completo do catálogo de livros  
- Gerenciamento de usuários  
- Registro de ocorrências e geração de relatórios  

O sistema é acessível via **web** e **mobile**.

---

# 📚 Índice
  
- [Diagrama de Arquitetura](#diagrama-de-arquitetura-c4-container)  
- [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)  
- [Diagrama de Classes](#diagrama-de-classes)  
- [Diagramas de Comunicação](#diagramas-de-comunicacao)  
  - [UC-05 – Realizar Reserva](#uc-05-realizar-reserva)  
  - [UC-06 – Realizar Empréstimo](#uc-06-realizar-emprestimo)  
  - [UC-07 – Registrar Devolução](#uc-07-registrar-devolucao)  
  - [UC-10 – Pagar Multa](#uc-10-pagar-multa)  
- [Diagramas de Estados](#diagramas-de-estado)  
  - [Ciclo de Vida do Livro](#ciclo-de-vida-do-livro)  
  - [Estado do Empréstimo](#estado-do-emprestimo)  
  - [Estado da Multa](#estado-da-multa)  
- [Diagrama de Implantação](#diagrama-de-implantacao)  
- [Diagrama de Modelo de Dados](#diagrama-de-modelo-de-dados)  
- [Diagramas de Sequência](#diagramas-de-sequencia)  
  - [UC-05 – Realizar Reserva](#uc-05-sequencia-realizar-reserva)  
  - [UC-06 – Realizar Empréstimo](#uc-06-sequencia-realizar-emprestimo)  
  - [UC-07 – Registrar Devolução](#uc-07-sequencia-registrar-devolucao)  
  - [UC-10 – Pagar Multa](#uc-10-sequencia-pagar-multa)  

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
<a name="diagrama-de-arquitetura-c4-container"></a>
![Diagrama de Arquitetura](ImagesPlantUML/Diagrama%20de%20Arquitetura.png)

---

# 🎯 Diagrama de Casos de Uso
**Objetivo:** Mostrar os atores e as funcionalidades que eles podem executar no sistema, permitindo visualizar **quem faz o quê**.

**Atores principais:**
- **Leitor** – Reservar livros, realizar empréstimos, devolver livros e pagar multas.  
- **Bibliotecário** – Gerenciar acervo, aprovar reservas, registrar devoluções e aplicar multas.  
- **Sistema de Pagamentos** – Processar pagamentos de multas e taxas.

**Diagrama:**  
<a name="diagrama-de-casos-de-uso"></a>
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
<a name="diagrama-de-classes"></a>
![Diagrama de Classes](ImagesPlantUML/Diagrama%20de%20Classes.png)

---

# 🔗 Diagramas de Comunicação

## UC-05 – Realizar Reserva
**Descrição:** O leitor solicita a reserva de um livro, o sistema valida a disponibilidade e registra a reserva.  
<a name="uc-05-realizar-reserva"></a>
![UC-05 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
**Descrição:** O leitor retira um livro, o sistema verifica reservas e atualiza o status do livro e do empréstimo.  
<a name="uc-06-realizar-emprestimo"></a>
![UC-06 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-06%20-%20Realizar%20Empréstimo.png)

## UC-07 – Registrar Devolução
**Descrição:** O leitor devolve o livro, o sistema atualiza o status e calcula multas se houver atraso.  
<a name="uc-07-registrar-devolucao"></a>
![UC-07 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-07%20-%20Registrar%20Devolução.png)

## UC-10 – Pagar Multa
**Descrição:** O leitor efetua o pagamento da multa, o sistema confirma a transação com o sistema externo.  
<a name="uc-10-pagar-multa"></a>
![UC-10 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-10%20-%20Pagar%20Multa.png)

---

# ⏳ Diagramas de Estado

## Ciclo de Vida do Livro
**Descrição:** Mostra as possíveis transições de estado de um livro (disponível, reservado, emprestado, em manutenção).  
<a name="ciclo-de-vida-do-livro"></a>
![Ciclo de Vida do Livro](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Ciclo%20de%20Vida%20do%20Livro.png)

## Estado do Empréstimo
**Descrição:** Mostra as mudanças de status do empréstimo (pendente, ativo, concluído, atrasado).  
<a name="estado-do-emprestimo"></a>
![Estado do Empréstimo](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Emprestimo.png)

## Estado da Multa
**Descrição:** Mostra os estados possíveis de uma multa (aberta, paga, em disputa).  
<a name="estado-da-multa"></a>
![Estado da Multa](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Multa.png)

---

# 💽 Diagrama de Implantação
**Descrição:** Representa os nós físicos onde os componentes do sistema estão implantados.  
<a name="diagrama-de-implantacao"></a>
![Diagrama de Implementação](ImagesPlantUML/Diagrama%20de%20Implementa%C3%A7%C3%A3o.png)

---

# 🗃️ Modelo de Dados (DER)
**Descrição:** Exibe tabelas do banco de dados e seus relacionamentos, permitindo entender a modelagem de dados do sistema.  
<a name="diagrama-de-modelo-de-dados"></a>
![Diagrama de Modelagem de Dados](ImagesPlantUML/Diagrama%20de%20Modelagem%20De%20Dados.png)

---

# 🕒 Diagramas de Sequência

## UC-05 – Realizar Reserva
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-05.  
<a name="uc-05-sequencia-realizar-reserva"></a>
![Sequência UC-05](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-06.  
<a name="uc-06-sequencia-realizar-emprestimo"></a>
![Sequência UC-06](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-06%20-%20Realizar%20Empréstimo.png)

## UC-07 – Registrar Devolução
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-07.  
<a name="uc-07-sequencia-registrar-devolucao"></a>
![Sequência UC-07](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-07%20-%20Registrar%20Devolução.png)

## UC-10 – Pagar Multa
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-10.  
<a name="uc-10-sequencia-pagar-multa"></a>
![Sequência UC-10](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-10%20-%20Pagar%20Multa.png)
