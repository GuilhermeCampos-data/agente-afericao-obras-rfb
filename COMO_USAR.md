# Guia Rápido: Assistente Especialista em Aferição de Obras (RFB)

Este ambiente está configurado com um agente de Inteligência Artificial blindado, programado para responder **exclusivamente** com base nas Instruções Normativas oficiais anexadas localmente (**IN RFB 2.021/2021**, **IN RFB 2.061/2021** e **IN RFB 2.110/2022**), sem buscas externas e sem alucinações.

## 1. Como iniciar o Assistente
1. Abra o Terminal na pasta `Assessoria_Obras`.
2. Digite `agy` e aperte **Enter**.

## 2. Exemplos de Perguntas Práticas
- *"Simule a aferição de uma reforma residencial de Pessoa Física com área de 120m² versus contrato de empreitada de R$ 80.000,00 com material não discriminado."*
- *"Quais são os pisos mínimos de RMT para serviços de pavimentação asfáltica e drenagem segundo a IN 2.021/2021?"*
- *"Quais obras estão dispensadas de inscrição no CNO segundo a IN 2.061/2021?"*

## 3. Como atualizar a base (CTN, CLT ou Leis Externas)
Sempre que uma regra fizer referência a outra lei (ex: Código Tributário Nacional ou CLT), o agente vai **parar a análise** e pedir o texto exato do artigo faltante.
1. Abra o arquivo `.agents/skills/afericao-obras-rfb/references/correlacoes_externas.md`.
2. Cole o texto do artigo solicitado em formato simples (`### Art. X - Lei Y`).
3. Salve o arquivo e peça para o agente continuar a análise.
