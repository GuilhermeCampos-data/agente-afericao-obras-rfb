# 🏗️ Agente Especialista em Aferição de Obras (SERO / RFB)

![Status](https://shields.io)
![Tech](https://shields.io)
![Architecture](https://shields.io)

Assistente de Inteligência Artificial especializado em regularização previdenciária e aferição de obras civis (prediais, reformas e não prediais) junto à Receita Federal do Brasil.

## 🎯 O Problema Resolvido
Profissionais de assessoria tributária e engenharia gastam horas cruzando artigos extensos de Instruções Normativas (**IN RFB 2.021/2021**, **IN RFB 2.061/2021** e **IN RFB 2.110/2022**) para definir a modalidade de aferição de menor custo (Área vs. Contrato/Nota Fiscal). Modelos de IA genéricos sofrem de **alucinação jurídica**, misturam normas revogadas e consomem excesso de tokens.

## 🛡️ Arquitetura e Diferenciais Técnicos
- **Base Normativa Estruturada em Markdown:** Legislação fatiada artigo por artigo (`### Art. X`), permitindo leitura cirúrgica via busca localizada (`grep`) e **reduzindo em até 85% o consumo de tokens** por consulta.
- **Guardrails Anti-Alucinação (Zero Busca Externa):** O agente é bloqueado para pesquisas na web e responde exclusivamente com base literal nos arquivos locais anexados.
- **Protocolo *Human-in-the-Loop*:** Caso uma análise exija correlação com normas externas (CTN, CLT, Código Civil), o agente interrompe a conclusão e solicita o anexo do artigo específico em `.md`.
- **Geração Automatizada de Parecer Técnico:** Saída padronizada pronta para revisão e entrega ao cliente final.

## 📂 Estrutura do Projeto
```text
Assessoria_Obras/
├── .agents/skills/afericao-obras-rfb/
│   ├── SKILL.md                  # Regras de negócio, árvore de decisão e guardrails
│   ├── assets/
│   │   └── template_parecer.md   # Modelo estruturado de parecer técnico
│   └── references/               # Base normativa limpa e indexada por artigo
├── COMO_USAR.md                  # Manual operacional para o usuário final
└── README.md                     # Documentação técnica e comercial
```

## 🚀 Exemplo de Caso de Uso
> *"Gere um parecer técnico completo para um cliente Pessoa Física que realizou uma reforma residencial em alvenaria de 110m², possuindo um contrato de empreitada com fornecimento de material discriminado no valor total de R$ 90.000,00."*

O agente realiza o enquadramento legal citando incisos literais, cruza as alíquotas da IN 2.110/2022, aplica os redutores da IN 2.021/2021 e entrega o parecer técnico estruturado.

---
*Desenvolvido por **Guilherme Campos** — Analista de Dados & Especialista em Automação com IA.*
