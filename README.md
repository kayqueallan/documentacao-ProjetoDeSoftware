# 📘 BookTrack 
🚀 Bem-vindo(a) à documentação do Projeto BookTrack!  
Este repositório concentra toda a documentação técnica de arquitetura, design e modelagem do software BookTrack. Aqui estão reunidos diversos diagramas UML e documentos visuais que explicam a estrutura, o funcionamento e as interações do sistema, oferecendo uma compreensão detalhada e organizada para desenvolvedores, analistas e demais interessados no projeto.

---

# 📖 Sobre o Sistema

O **BookTrack** é um sistema para gerenciar bibliotecas físicas e digitais, oferecendo organização e praticidade para leitores e bibliotecários.  

Para **usuários**, o sistema permite:  
- **Empréstimos e reservas de livros** – localizar, reservar e acompanhar prazos de devolução.  
- **Leitura e avaliação de ebooks** – ler online e registrar comentários sobre os livros.  
- **Histórico de leitura** – consultar reservas, empréstimos e devoluções anteriores.  

Para **bibliotecários**, o sistema oferece:  
- **Gestão do acervo** – cadastrar, editar e remover livros.  
- **Controle de usuários** – monitorar atividades e gerenciar permissões.  
- **Relatórios e ocorrências** – controle de multas, reservas e estatísticas de uso.  

**Benefícios principais:**  
- Automatiza processos internos, reduzindo erros manuais.  
- Facilita o acesso aos livros e ebooks.  
- Melhora a organização e o controle da biblioteca.  
- Integração com sistema de pagamentos para multas.  

Em resumo, o BookTrack combina **funcionalidade, acessibilidade e eficiência**, tornando a gestão da biblioteca mais moderna e prática.


---

# 📚 Índice
  
- [Diagrama de Arquitetura](#diagrama-arquitetura)  
- [Diagrama de Casos de Uso](#diagrama-casos-de-uso)  
- [Diagrama de Classes](#diagrama-classes)
- [Diagrama de Componentes](#diagrama-componentes)
- [Diagramas de Comunicação](#diagramas-comunicacao)  
  - [UC-05 – Realizar Reserva](#uc-05-reserva)  
  - [UC-06 – Realizar Empréstimo](#uc-06-emprestimo)  
  - [UC-07 – Registrar Devolução](#uc-07-devolucao)  
  - [UC-10 – Pagar Multa](#uc-10-multa)  
- [Diagramas de Estado](#diagramas-estado)  
  - [Ciclo de Vida do Livro](#ciclo-vida-livro)  
  - [Estado do Empréstimo](#estado-emprestimo)  
  - [Estado da Multa](#estado-multa)  
- [Diagrama de Implantação](#diagrama-implantacao)  
- [Diagrama de Modelo de Dados](#diagrama-modelo-dados)  
- [Diagramas de Sequência](#diagramas-sequencia)  
  - [UC-05 – Realizar Reserva](#uc-05-sequencia-reserva)  
  - [UC-06 – Realizar Empréstimo](#uc-06-sequencia-emprestimo)  
  - [UC-07 – Registrar Devolução](#uc-07-sequencia-devolucao)  
  - [UC-10 – Pagar Multa](#uc-10-sequencia-multa)  

---

<h2 id="diagrama-arquitetura">🏗️ Diagrama de Arquitetura (C4 / Container)</h2>
**Objetivo:** Apresentar a visão de alto nível do sistema, mostrando como os contêineres principais se comunicam.  

**Componentes principais:**
- **Frontend** – Interface de usuário web e mobile.  
- **Backend** – Processa a lógica de negócio, valida dados e integra com o banco de dados e sistemas externos.  
- **Banco de Dados** – Armazena usuários, livros, empréstimos, reservas e multas.  
- **Sistema de Pagamentos Externo** – Processa pagamentos de multas e taxas.

**Diagrama:**  
![Diagrama de Arquitetura](ImagesPlantUML/Diagrama%20de%20Arquitetura.png)

---

<h2 id="diagrama-casos-de-uso">🎯 Diagrama de Casos de Uso</h2>
**Objetivo:** Mostrar os atores e as funcionalidades que eles podem executar no sistema, permitindo visualizar **quem faz o quê**.

**Atores principais:**
- **Leitor** – Reservar livros, realizar empréstimos, devolver livros e pagar multas.  
- **Bibliotecário** – Gerenciar acervo, aprovar reservas, registrar devoluções e aplicar multas.  
- **Sistema de Pagamentos** – Processar pagamentos de multas e taxas.

**Diagrama:**  
![Diagrama de Casos de Uso](ImagesPlantUML/Diagrama%20de%20Casos%20de%20Uso.png)

---

<h2 id="diagrama-classes">🧱 Diagrama de Classes</h2>
**Objetivo:** Representar a **estrutura lógica** do sistema, incluindo entidades, atributos, métodos e relacionamentos.

**Principais classes:**
- **Livro** – Título, autor, categoria e status (disponível, reservado, emprestado).  
- **Usuário** – Nome, matrícula, tipo (leitor ou bibliotecário) e histórico de empréstimos.  
- **Empréstimo** – Data de retirada, devolução e multas aplicadas.  
- **Multa** – Valor, status do pagamento e data de vencimento.

**Diagrama:**  
![Diagrama de Classes](ImagesPlantUML/Diagrama%20de%20Classes.png)

---

<h2 id="diagrama-componentes">🧩 Diagrama de Componentes</h2>
**Objetivo:** Exibir a organização dos principais módulos do sistema e como eles se comunicam — incluindo frontend, backend, serviços, banco de dados e integrações externas.**

**Componentes principais:**
- **Frontend Web/Mobile**  
- **API Gateway (REST/HTTP)**  
- **Serviços (Usuários, Livros, Empréstimos/Reservas, Multas)**  
- **Banco de Dados PostgreSQL**  
- **Sistema de Pagamentos Externo**

**Diagrama:**  
![Diagrama de Componentes](ImagesPlantUML/Diagrama%20de%20Componentes.png)

---

<h2 id="diagramas-comunicacao">🔗 Diagramas de Comunicação</h2>

## UC-05 – Realizar Reserva
**Descrição:** O leitor solicita a reserva de um livro, o sistema valida a disponibilidade e registra a reserva.  
<a id="uc-05-reserva"></a>
![UC-05 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
**Descrição:** O leitor retira um livro, o sistema verifica reservas e atualiza o status do livro e do empréstimo.  
<a id="uc-06-emprestimo"></a>
![UC-06 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-06%20-%20Realizar%20Empréstimo.png)

## UC-07 – Registrar Devolução
**Descrição:** O leitor devolve o livro, o sistema atualiza o status e calcula multas se houver atraso.  
<a id="uc-07-devolucao"></a>
![UC-07 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-07%20-%20Registrar%20Devolução.png)

## UC-10 – Pagar Multa
**Descrição:** O leitor efetua o pagamento da multa, o sistema confirma a transação com o sistema externo.  
<a id="uc-10-multa"></a>
![UC-10 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-10%20-%20Pagar%20Multa.png)

---

<h2 id="diagramas-estado">⏳ Diagramas de Estado</h2>

## Ciclo de Vida do Livro
**Descrição:** Mostra as possíveis transições de estado de um livro (disponível, reservado, emprestado, em manutenção).  
<a id="ciclo-vida-livro"></a>
![Ciclo de Vida do Livro](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Ciclo%20de%20Vida%20do%20Livro.png)

## Estado do Empréstimo
**Descrição:** Mostra as mudanças de status do empréstimo (pendente, ativo, concluído, atrasado).  
<a id="estado-emprestimo"></a>
![Estado do Empréstimo](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Emprestimo.png)

## Estado da Multa
**Descrição:** Mostra os estados possíveis de uma multa (aberta, paga, em disputa).  
<a id="estado-multa"></a>
![Estado da Multa](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Multa.png)

---

<h2 id="diagrama-implantacao">💽 Diagrama de Implantação</h2>
**Descrição:** Representa os nós físicos onde os componentes do sistema estão implantados.  

![Diagrama de Implementação](ImagesPlantUML/Diagrama%20de%20Implementa%C3%A7%C3%A3o.png)

---

<h2 id="diagrama-modelo-dados">🗃️ Modelo de Dados (DER)</h2>
**Descrição:** Exibe tabelas do banco de dados e seus relacionamentos, permitindo entender a modelagem de dados do sistema.  

![Diagrama de Modelagem de Dados](ImagesPlantUML/Diagrama%20de%20Modelagem%20De%20Dados.png)

---

<h2 id="diagramas-sequencia">🕒 Diagramas de Sequência</h2>

## UC-05 – Realizar Reserva
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-05.  
<a id="uc-05-sequencia-reserva"></a>
![Sequência UC-05](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-06.  
<a id="uc-06-sequencia-emprestimo"></a>
![Sequência UC-06](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-06%20-%20Realizar%20Empréstimo.png)

## UC-07 – Registrar Devolução
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-07.  
<a id="uc-07-sequencia-devolucao"></a>
![Sequência UC-07](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-07%20-%20Registrar%20Devolução.png)

## UC-10 – Pagar Multa
**Descrição:** Mostra o fluxo temporal das mensagens entre os componentes para o caso de uso UC-10.  
<a id="uc-10-sequencia-multa"></a>
![Sequência UC-10](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-10%20-%20Pagar%20Multa.png)




