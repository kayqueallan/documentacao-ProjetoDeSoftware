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
  
- [Diagrama de Arquitetura](#diagrama-de-arquitetura-c4--container)  
- [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)  
- [Diagrama de Classes](#diagrama-de-classes)  
- [Diagramas de Comunicação](#diagramas-de-comunicacao)  
  - [UC-05 – Realizar Reserva](#uc-05--realizar-reserva)  
  - [UC-06 – Realizar Empréstimo](#uc-06--realizar-emprestimo)  
  - [UC-07 – Registrar Devolução](#uc-07--registrar-devolucao)  
  - [UC-10 – Pagar Multa](#uc-10--pagar-multa)  
- [Diagramas de Estados](#diagramas-de-estado)  
  - [Ciclo de Vida do Livro](#ciclo-de-vida-do-livro)  
  - [Estado do Empréstimo](#estado-do-emprestimo)  
  - [Estado da Multa](#estado-da-multa)  
- [Diagrama de Implantação](#diagrama-de-implantacao)  
- [Diagrama de Modelo de Dados](#diagrama-de-modelo-de-dados)  
- [Diagramas de Sequência](#diagramas-de-sequencia)  
  - [UC-05 – Realizar Reserva](#uc-05--sequencia-realizar-reserva)  
  - [UC-06 – Realizar Empréstimo](#uc-06--sequencia-realizar-emprestimo)  
  - [UC-07 – Registrar Devolução](#uc-07--sequencia-registrar-devolucao)  
  - [UC-10 – Pagar Multa](#uc-10--sequencia-pagar-multa)  

---

# 🏗️ Diagrama de Arquitetura (C4 / Container)
**Objetivo:** Apresentar a visão de alto nível do sistema, mostrando como os contêineres principais se comunicam.  

**Diagrama:**  
<a name="diagrama-de-arquitetura-c4--container"></a>
![Diagrama de Arquitetura](ImagesPlantUML/Diagrama%20de%20Arquitetura.png)

---

# 🎯 Diagrama de Casos de Uso
**Objetivo:** Mostrar os atores e as funcionalidades que eles podem executar no sistema.  

**Diagrama:**  
<a name="diagrama-de-casos-de-uso"></a>
![Diagrama de Casos de Uso](ImagesPlantUML/Diagrama%20de%20Casos%20de%20Uso.png)

---

# 🧱 Diagrama de Classes
**Objetivo:** Representar a estrutura lógica do sistema, incluindo entidades, atributos, métodos e relacionamentos.  

**Diagrama:**  
<a name="diagrama-de-classes"></a>
![Diagrama de Classes](ImagesPlantUML/Diagrama%20de%20Classes.png)

---

# 🔗 Diagramas de Comunicação

## UC-05 – Realizar Reserva
**Diagrama:**  
<a name="uc-05--realizar-reserva"></a>
![UC-05 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
**Diagrama:**  
<a name="uc-06--realizar-emprestimo"></a>
![UC-06 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-06%20-%20Realizar%20Empréstimo.png)

## UC-07 – Registrar Devolução
**Diagrama:**  
<a name="uc-07--registrar-devolucao"></a>
![UC-07 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-07%20-%20Registrar%20Devolução.png)

## UC-10 – Pagar Multa
**Diagrama:**  
<a name="uc-10--pagar-multa"></a>
![UC-10 – Comunicação](ImagesPlantUML/Diagrama%20de%20Comunicação%20–%20UC-10%20-%20Pagar%20Multa.png)

---

# ⏳ Diagramas de Estado

## Ciclo de Vida do Livro
<a name="ciclo-de-vida-do-livro"></a>
![Ciclo de Vida do Livro](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Ciclo%20de%20Vida%20do%20Livro.png)

## Estado do Empréstimo
<a name="estado-do-emprestimo"></a>
![Estado do Empréstimo](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Emprestimo.png)

## Estado da Multa
<a name="estado-da-multa"></a>
![Estado da Multa](ImagesPlantUML/Diagrama%20de%20Estado%20-%20Multa.png)

---

# 💽 Diagrama de Implementação
<a name="diagrama-de-implantacao"></a>
![Diagrama de Implementação](ImagesPlantUML/Diagrama%20de%20Implementa%C3%A7%C3%A3o.png)

---

# 🗃️ Modelo de Dados (DER)
<a name="diagrama-de-modelo-de-dados"></a>
![Diagrama de Modelagem de Dados](ImagesPlantUML/Diagrama%20de%20Modelagem%20De%20Dados.png)

---

# 🕒 Diagramas de Sequência

## UC-05 – Realizar Reserva
<a name="uc-05--sequencia-realizar-reserva"></a>
![Sequência UC-05](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-05%20-%20Realizar%20Reserva.png)

## UC-06 – Realizar Empréstimo
<a name="uc-06--sequencia-realizar-emprestimo"></a>
![Sequência UC-06](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-06%20-%20Realizar%20Empréstimo.png)

## UC-07 – Registrar Devolução
<a name="uc-07--sequencia-registrar-devolucao"></a>
![Sequência UC-07](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-07%20-%20Registrar%20Devolução.png)

## UC-10 – Pagar Multa
<a name="uc-10--sequencia-pagar-multa"></a>
![Sequência UC-10](ImagesPlantUML/Diagrama%20de%20Sequência%20–%20UC-10%20-%20Pagar%20Multa.png)
