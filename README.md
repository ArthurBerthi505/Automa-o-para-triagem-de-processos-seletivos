🎯 O Desafio:
Analisar dezenas de currículos manualmente para validar requisitos mínimos (como 2 anos de experiência e uso de Python para automação) consome muito tempo.

🛠️ A Solução:
Desenvolvi um pipeline de triagem utilizando n8n para orquestrar o fluxo, integrando LLMs e planilhas.

O fluxo funciona assim:
1️⃣ O currículo entra no sistema.
2️⃣ A API do Groq (IA) recebe um prompt altamente estruturado para atuar como Recruiter, analisando o texto do CV e extraindo o tempo de experiência real e as habilidades em Python.
3️⃣ O n8n avalia a resposta da IA e toma a decisão:
✅ Aprovados: Seguem no processo.
❌ Reprovados: O fluxo adiciona o candidato e o motivo da reprovação em um Google Sheets via API (para histórico) e encerra o processo (ou envia um e-mail de feedback).
