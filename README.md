# 💻 Oscar | Software Engineer  

Olá! 👋 Sou o Oscar, um desenvolvedor apaixonado por tecnologia e engenharia de software. Trabalho com **Java** há mais de 2 anos, criando soluções eficientes e escaláveis. 🚀  
 ![](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white) ![](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white) ![](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white) ![](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white) ![](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=Jira&logoColor=white) ![](https://img.shields.io/badge/Trello-0052CC?style=for-the-badge&logo=trello&logoColor=white) ![](https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white) ![](https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white) 

## 💡 Sobre mim  
🔹 Engenheiro de Software especializado em Java ☕  
🔹 Ponto forte em **identificar problemas e resolvê-los** 🔍✅  
🔹 Meu trabalho é focado em soluções entre **Homem e Maquina** 🤝💻  
🔹 Experiência prática com **Java e Spring Framework** (JPA Hibernate, Web Services e Spring Security) ⚙️  
🔹 Experiência com metodologias ágeis: **Scrum e Kanban** 🔄 para maximizar eficiência e qualidade 📈  
🔹 Sempre aprendendo e explorando novas tecnologias 📚  

## 🛠️ Tecnologias e Ferramentas  
✔️ **Java, Spring Boot, Spring Security, Hibernate (JPA)**  
✔️ **Banco de Dados: MySQL, PostgreSQL**  
✔️ **Versionamento: Git, GitHub e GitFlow**  
✔️ **Metodologias Ágeis: Scrum, KANBAN** 
✔️ **Gerenciamento de projetos: Jira e Trello**  

# Foco atual :
# 🎵 MusicNow Ecosystem

O **MusicNow** é uma plataforma distribuída baseada em microsserviços/APIs modulares estruturada sobre as diretrizes de **Domain-Driven Design (DDD)** e **Arquitetura Hexagonal**. O sistema resolve o problema de agendamento, contratação e avaliação de eventos musicais de forma resiliente e isolada.

---

## 🗺️ Contexto Geral do Ecossistema (APIs)

O ecossistema é composto por 5 módulos/APIs com responsabilidades atômicas e bem delimitadas:

1. **MÚSICO (API):** Gerencia o ciclo de vida, o perfil profissional, dados técnicos, repertório e o cadastro do artista na plataforma.
2. **DISPONIBILIDADE (API):** Controla a agenda do músico. É o motor que gerencia os slots de data/hora abertos, os bloqueios automáticos e as janelas de tempo livre do artista.
3. **CONTRATANTE (API):** Administra os perfis de contratantes (pessoas físicas ou jurídicas), aplicando validações rígidas de integridade (como chaves secundárias exclusivas de CPF/CNPJ).
4. **RESERVA (API):** O orquestrador central do processo de contratação. Cuida das propostas recebidas, da renegociação de cachês e das mudanças de status do evento.
5. **AVALIAÇÃO (API):** Coleta o feedback mútuo pós-evento, processando as notas e atualizando matematicamente as médias de reputação de ambas as partes.

---

## 🔄 Fluxo Estrutural de Negócio (End-to-End)

O fluxo de dados e a comunicação entre as APIs seguem uma sequência lógica e linear para garantir que nenhuma invariante de domínio seja violada:
### Detalhamento das Etapas do Fluxo:

* **Passo 1: Ativação do Músico**
  O músico realiza o seu cadastro na **API Músico**. Seu perfil torna-se elegível para listagem na plataforma.
  
* **Passo 2: Definição de Slot Temporais**
  O músico acessa a **API Disponibilidade** e abre blocos de datas onde está livre para realizar shows.

* **Passo 3: Intenção de Compra**
  O contratante (autenticado pela **API Contratante**) seleciona o artista e envia uma proposta contendo data, local e valor inicial através da **API Reserva**.

* **Passo 4: Barreira de Validação Automática**
  A **API Reserva** consulta imediatamente a **API Disponibilidade** para confirmar se o músico possui agenda aberta para aquela data específica, impedindo conflitos de agendamento antes mesmo de notificar o artista.

* **Passo 5: Ciclo de Negociação Dinâmica**
  O músico é notificado e analisa a proposta. No domínio da **API Reserva**, ele pode:
  * *Aceitar* a reserva diretamente.
  * *Recusar* a proposta.
  * *Renegociar* os valores (abrindo uma contraproposta de cachê para o contratante avaliar).

* **Passo 6: Conclusão e Reputação**
  Após o término do evento, o fluxo é encerrado na **API Avaliação**. O músico avalia o contratante e o contratante avalia o músico. O sistema dispara de forma assíncrona o cálculo das médias aritméticas, atualizando o score público de ambos os perfis no ecossistema.

---

## 🛠️ Diretrizes de Desenvolvimento e Qualidade

Para manter este fluxo protegido à medida que as APIs evoluem, todo desenvolvedor deve seguir rigorosamente estes padrões no Git e GitHub:

* **Arquitetura Hexagonal:** A lógica de validação das propostas ou o cálculo de médias da API de Avaliação devem morar estritamente no `Domain (Core)`, totalmente isolados de banco de dados (`Adapters Outbound`) ou Web/HTTP (`Adapters Inbound`).
* **Conventional Commits:** Todo commit referente às regras dessas APIs deve ser semântico (ex: `feat(reserva): implementar logica de renegociacao de valores`).
* **Proteção de Branches:** As branches `main` e `develop` são protegidas. Nenhuma alteração nas regras de domínio do ecossistema pode ser empurrada diretamente sem um *Pull Request* e validação de cobertura de testes.
---
# Minhas info:

## 🎓 Certificados  
Acesse meus certificados de desenvolvimento e tecnologias [aqui](https://drive.google.com/drive/folders/1740658cwNVprDwaXxE5KKmIv7yADapk5?usp=drive_link).  

## 📫 Contato  
![NEgociante2t@gmail.com](https://img.shields.io/badge/NEgociante2t@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white) [![🔗 LinkedIn: [https://www.linkedin.com/in/oscar-java-engineer/]  ](https://img.shields.io/badge/OscarRibeiro-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/oscar-java-engineer/)

