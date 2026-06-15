<div align="center">
  <h1>💻 Oscar | Software Engineer</h1>
  <p>Olá! 👋 Sou o Oscar, um desenvolvedor apaixonado por tecnologia e engenharia de software. Trabalho com <b>Java</b> há mais de 3 anos, criando soluções eficientes e escaláveis. 🚀</p>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring" />
  <img src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL" />
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/GIT-E44C30?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white" alt="IntelliJ" />
  <img src="https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=Jira&logoColor=white" alt="Jira" />
  <img src="https://img.shields.io/badge/Trello-0052CC?style=for-the-badge&logo=trello&logoColor=white" alt="Trello" />
</div>

---

## 💡 Sobre mim  
🔹 Engenheiro de Software especializado em Java ☕  
🔹 Ponto forte em **identificar problemas e resolvê-los** 🔍✅  
🔹 Meu trabalho é focado em soluções entre **Homem e Máquina** 🤝💻  
🔹 Experiência prática com **Java e Spring Framework** (JPA Hibernate, Web Services e Spring Security) ⚙️  
🔹 Experiência com metodologias ágeis: **Scrum e Kanban** 🔄 para maximizar eficiência e qualidade 📈  
🔹 Sempre aprendendo e explorando novas tecnologias 📚  

## 🛠️ Tecnologias e Ferramentas  
✔️ **Back-end:** Java, Spring Boot, Spring Security, Hibernate (JPA)  
✔️ **Banco de Dados:** MySQL, PostgreSQL, MongoDB  
✔️ **Versionamento & Fluxos:** Git, GitHub e GitFlow  
✔️ **Metodologias & Gestão:** Scrum, Kanban, Jira e Trello  

## 🎓 Certificados  
Acesse meus certificados de desenvolvimento e tecnologias clicando [aqui](https://drive.google.com/drive/folders/1740658cwNVprDwaXxE5KKmIv7yADapk5?usp=drive_link).  

## 📫 Contato  
<div align="left">
  <a href="mailto:NEgociante2t@gmail.com">
    <img src="https://img.shields.io/badge/NEgociante2t@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail" />
  </a>
  <a href="https://www.linkedin.com/in/oscar-java-engineer/" target="_blank">
    <img src="https://img.shields.io/badge/OscarRibeiro-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
</div>
---

<div align="center">
  <h2>📊 Estatísticas do GitHub </h2>

  <table border="0" cellpadding="0" cellspacing="0">
    <tr align="center">
      <td width="50%">
        <img src="https://github-readme-stats.vercel.app/api?username=OscarRibeiro07&show_icons=true&theme=dracula&hide_border=true&include_all_commits=true&count_private=true&show=reviews,prs_merged,prs_merged_percentage&locale=pt-br" alt="Estatísticas do Oscar" height="190px"/>
      </td>
      <td width="50%">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=OscarRibeiro07&layout=compact&theme=dracula&hide_border=true&langs_count=7&locale=pt-br" alt="Linguagens do Oscar" height="190px"/>
      </td>
    </tr>
  </table>

  <br />

  <img src="https://github-readme-streak-stats.herokuapp.com/?user=OscarRibeiro07&theme=dracula&hide_border=true&locale=pt_BR" alt="Sequência de Contribuições" />
</div>

---
## 🎯 Foco Atual: Ecossistema MusicNow

O **MusicNow** é uma plataforma distribuída baseada em microsserviços e APIs modulares, totalmente estruturada sob as diretrizes de **Domain-Driven Design (DDD)** e **Arquitetura Hexagonal**. O sistema resolve o ciclo completo de agendamento, contratação e avaliação de eventos musicais de forma isolada e altamente resiliente.

### 🗺️ Contexto Geral do Ecossistema (APIs)
O ecossistema é composto por 5 módulos/APIs com responsabilidades de negócio bem delimitadas:

* **Músico (API):** Gerencia o ciclo de vida, perfil profissional, dados técnicos, repertório e o cadastro do artista.
* **Disponibilidade (API):** Controla a agenda do músico. É o motor que gerencia os slots de data/hora abertos, os bloqueios automáticos e as janelas de tempo livre.
* **Contratante (API):** Administra os perfis de contratantes (PF/PJ), aplicando validações rígidas de integridade e unicidade (como chaves de CPF/CNPJ).
* **Reserva (API):** O orquestrador central do processo de contratação. Cuida das propostas recebidas, da renegociação de cachês e das máquinas de estados/status do evento.
* **Avaliação (API):** Coleta o feedback mútuo pós-evento, processando as notas e atualizando matematicamente as médias de reputação de ambas as partes.

### 🛠️ Diretrizes de Desenvolvimento e Qualidade
Para garantir a evolução segura das APIs, os seguintes padrões são aplicados no repositório:
* **Arquitetura Hexagonal:** Toda lógica de negócio (como a validação de propostas e cálculo de médias) reside estritamente no `Domain (Core)`, isolada de banco de dados (`Adapters Outbound`) ou Web/HTTP (`Adapters Inbound`).
* **Conventional Commits:** Uso obrigatório de commits semânticos para manter o histórico limpo e inteligível (ex: `feat(reserva): implementar logica de renegociacao de valores`).
* **Proteção de Branches:** As branches `main` e `develop` são protegidas. Nenhuma alteração entra no core do ecossistema sem um *Pull Request* aprovado e validação de cobertura de testes.

---


