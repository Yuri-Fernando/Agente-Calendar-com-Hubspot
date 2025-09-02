# Agente-Calendar-com-Hubspot

Como integrei HubSpot com n8n para automatizar follow-ups de clientes — tudo de forma FREE 🚀

📌 Visão Geral
Este projeto mostra como conectar HubSpot, Supabase, Google Calendar e WhatsApp usando n8n para criar um AI Agent que:
Cria e atualiza contatos no HubSpot
Agenda, cancela e reagenda reuniões no Google Calendar
Responde e interage via WhatsApp
Automatiza follow-ups personalizados (via GPT)
Ativa/desativa funções via comando
Integra com banco Supabase para armazenar dados
Controla follow-ups e confirmações 24h antes de reuniões

👉 Tudo isso de forma gratuita com n8n e APIs públicas.

⚙️ Fluxo de Funcionamento

Usuário → AI Agent → Tool Agendamento → HubSpot Create Engagement → Enviar Confirmação Inicial
    ↳ Wait 24h → Enviar Confirmação via WhatsApp

🚀 Funcionalidades
Banco de Dados: usa Supabase para armazenar interações e dados dos clientes.
Agendamento: cria, cancela e reagenda compromissos no Google Calendar.

HubSpot:
Criação/atualização automática de contatos.
Criação de Engagements (tasks/meetings) para follow-up.
Atualização de status do lead em tempo real.
WhatsApp: envio de confirmações e lembretes automáticos.
AI Agent (GPT): personalização de mensagens de follow-up.
Ativação/Desativação: controle do agente por comando direto.

💡 Benefícios
Automação de tarefas repetitivas
Follow-ups consistentes e personalizados
Integração CRM + comunicação sem custo com softwares caros
Experiência fluida para leads e equipe de vendas

🛠️ O que falta terminar:
Replicar agendamento do Calendar diretamente no HubSpot
Finalizar aviso automático de agenda 24h antes da reunião
Melhorar follow-up final pós-reunião

📋 Como funciona o agendamento no HubSpot
Criar/atualizar contato no HubSpot
Node: HubSpot → Create or Update a Contact
Criar engajamento (Engagement)
Node: HubSpot → Create Engagement

Configuração:
engagement type → MEETING
timestamp → data/hora da reunião
associations → contato/deal correto
Enviar confirmação automática
Node Wait (ou Cron) → start - 24h
Depois → HTTP Request (WhatsApp)

Pós-reunião
Checar status no HubSpot
Marcar como done/completed
Disparar pesquisa de satisfação ou follow-up final

🔮 Próximos Passos
Finalizar replicação completa do agendamento HubSpot ↔ Calendar
Criar dashboard para monitoramento dos follow-ups em tempo real
Adicionar camada de métricas (quantidade de reuniões, taxa de conversão etc.)
