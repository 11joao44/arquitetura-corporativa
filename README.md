# 📘 Desafio – Arquitetura da Informação na UnivagPro

## 🏫 Contexto da Empresa

A **UnivagPro** é uma empresa fictícia que oferece cursos profissionalizantes presenciais nas áreas de administração, informática e saúde. Com um número crescente de alunos e colaboradores, a empresa passou a depender fortemente de seus sistemas internos para gerenciar informações acadêmicas, financeiras e administrativas, como:

- Frequência de alunos
- Notas e históricos escolares
- Pagamentos e mensalidades
- Informações cadastrais e contratuais

No entanto, a UnivagPro enfrenta desafios críticos:
- Ausência de rotinas formais de **backup e recuperação**;
- Inexistência de um **plano estruturado de recuperação de desastres**;
- **Segurança da informação fragilizada**, com riscos de vazamentos e acessos indevidos.

---

## 👨‍💼 Papel Estratégico

Como **CTO (Chief Technology Officer)** da UnivagPro, minha missão é alinhar a tecnologia à estratégia da empresa, assegurando que as informações sejam protegidas, os sistemas sejam escaláveis e os serviços funcionem de forma integrada. Para isso, proponho uma abordagem baseada na **Arquitetura Corporativa**, conforme o modelo abaixo.

---

## 🧩 Componentes da Arquitetura Corporativa

### 🔐 1. Arquitetura de Informação

Responsável por identificar **onde e como informações críticas** da empresa — como registros de alunos e fornecedores — serão **armazenadas, mantidas e protegidas**. Engloba três áreas fundamentais:

---

#### 🔁 Backup e Recuperação

**Diretrizes a seguir:**

- Adotar **backup incremental diário em nuvem**, salvando apenas os arquivos modificados desde o último backup.
- Realizar **backup completo semanalmente aos sábados em HDs externos** armazenados em local seguro.
- No **início de cada mês**, executar testes de **restauração completa** para verificar a integridade dos backups.
- Em caso de falha no processo de restauração, realizar **recuperação parcial** priorizando arquivos e sistemas de uso diário.
- Aplicar o plano de **BCP (Business Continuity Plan)** e comunicar imediatamente os responsáveis e usuários sobre o ocorrido.

---

#### ⚠️ Recuperação de Desastres

**Diretrizes a seguir:**

- Acionar o **DRP (Disaster Recovery Plan)** em situações críticas, sinalizando o **status de alerta vermelho**.
- Identificar a natureza da ameaça (ex: falha elétrica, ataque cibernético, incêndio, etc.) e avaliar o impacto em cada setor e sistema.
- Priorizar a **restauração dos serviços essenciais** com base nos backups mais recentes.
- Comunicar de forma clara e objetiva todos os usuários sobre a situação.
- Realizar uma **análise pós-incidente** para identificar falhas, responsabilidades e melhorias futuras.

---

#### 🔐 Segurança da Informação

**Diretrizes a seguir:**

- Adotar o modelo dos **5 pilares da segurança da informação (CIA + AA)**:  
  - **C**onfidencialidade  
  - **I**ntegridade  
  - **D**isponibilidade  
  - **A**utenticidade  
  - **I**rretratabilidade
- Exigir **senhas fortes** com troca periódica e **autenticação em dois fatores** em todos os sistemas internos.
- Aplicar o **princípio do menor privilégio**, concedendo a cada colaborador apenas o acesso necessário às suas funções.
- Realizar **revisão imediata de acessos** em casos de desligamento ou mudança de cargo.
- Promover **treinamentos recorrentes** sobre boas práticas de segurança da informação.
- Monitorar e registrar todos os acessos a dados sensíveis.
- Exigir que **todo novo dispositivo seja equipado com o antivírus oficial da empresa** antes de se conectar à rede interna.
- Analisar a **origem e autenticidade de toda informação** recebida ou enviada, especialmente as que envolvam dados de terceiros.

---

### 🖥️ 2. Arquitetura de Infraestrutura

Inclui os equipamentos de **hardware, software e telecomunicações** que dão suporte às operações da UnivagPro.

A infraestrutura da empresa é orientada pelos seguintes atributos:
- **Flexibilidade e escalabilidade**: uso de servidores virtualizados com possibilidade de migração para a nuvem.
- **Confiabilidade e disponibilidade**: mecanismos de redundância e UPS (no-breaks) para manter os serviços ativos.
- **Desempenho**: monitoramento contínuo dos recursos para garantir responsividade e estabilidade.

---

### 🧩 3. Arquitetura de Aplicação

Determina como os sistemas e softwares da empresa **se integram e se comunicam entre si**.

A UnivagPro adota os seguintes princípios:
- **Serviços Web**: sistemas acessíveis por navegador, integrando portais de alunos, professores e financeiro.
- **Sistemas Abertos**: suporte à integração com plataformas externas por meio de APIs.

#### 🧠 SOA – Service-Oriented Architecture

A UnivagPro está evoluindo sua arquitetura de aplicação com base no modelo **SOA**, estruturando seus sistemas em **serviços independentes e reutilizáveis**, como:
- Serviço de matrícula
- Serviço de consulta de notas
- Serviço de emissão de certificados
- Serviço de pagamento de mensalidades

Esses serviços são acessados por diferentes interfaces (portais, apps, relatórios), promovendo:
- **Reutilização de funcionalidades**
- **Redução de retrabalho**
- **Facilidade de manutenção e escalabilidade**

---

## ✅ Conclusão

A implementação dessas diretrizes e camadas arquiteturais garante que a UnivagPro esteja preparada para proteger seus ativos informacionais, manter a continuidade dos serviços e evoluir de forma sustentável, integrando tecnologia à sua missão educacional.

## 🧾 Considerações Finais

As diretrizes apresentadas no documento cumpriu integralmente os requisitos propostos no desafio, abordando as três áreas fundamentais da Arquitetura da Informação: **backup e recuperação**, **recuperação de desastres** e **segurança da informação**. Para cada uma delas, foi definidas políticas práticas que contemplam tanto **ações de prevenção** quanto **rotinas de suporte em caso de falhas ou incidentes**.
