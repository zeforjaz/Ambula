# Twilio - WhatsApp | Ambula

Projecto de automacao de mensagens WhatsApp na jornada do cliente Ambula.

## Contexto

Substituir chamadas telefonicas manuais (Valdemir/Roseanne) por mensagens automaticas WhatsApp em cada etapa do transporte, tanto para o contacto principal (paciente) como para o contacto secundario (familiar que solicitou).

## Templates (8 mensagens)

| # | Template | Gatilho | Destinatario |
|---|----------|---------|----------|
| 1 | Pedido Recebido + Pagamento | Novo pedido no Airtable | Principal + Secundario |
| 2 | Transporte Confirmado | Pagamento recebido | Principal + Secundario |
| 2B | Alerta de Cancelamento | 24h antes se nao pago | Principal + Secundario |
| 3 | Ambulancia a Caminho | Tripulante inicia viagem | Principal + Secundario |
| 4 | Paciente Recolhido | Tripulante confirma recolha | Secundario apenas |
| 5 | Transporte Concluido | Tripulante confirma entrega | Principal + Secundario |
| 6 | Feedback (3 botoes quick reply) | 2h apos conclusao | Principal + Secundario |
| 7 | Lembrete Pagamento | Manual / dividas antigas | Principal + Secundario |

## Stack

- **Twilio** WhatsApp Business API (conta Ambula LDA activa)
- **Airtable** como fonte de dados e gatilhos
- **Make/n8n** para automacao (Airtable -> Twilio)

## Ficheiros

- `mockup-conversa-exemplo.html` - Mockup visual da conversa WhatsApp

## Custo Estimado

~8 EUR/mes para 182 transportes actuais. Escala linear.
