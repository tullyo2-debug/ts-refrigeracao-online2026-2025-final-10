# TS Refrigeração — versão pronta para Vercel

Esta versão usa Vite + Supabase e já contém a melhoria completa do módulo de Ordens de Serviço.

## Variáveis de ambiente no Vercel

Use:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`

Os valores também estão no `.env.production` desta entrega para facilitar o deploy. A chave usada é a **publishable**, não `service_role`.

## Deploy

1. Importe este projeto no Vercel.
2. Framework: **Vite**.
3. Build Command: `npm run build`.
4. Output Directory: `dist`.
5. Install Command: `npm install`.
6. Faça o deploy.

## Ordem de Serviço

Inclui cliente, equipamento, agendamento, técnico, serviços, peças, valores, desconto, total, status, prioridade, diagnóstico, execução, observações, fotos por URL, assinatura, histórico, finalização e integração financeira.

## Banco

A versão pressupõe o banco Supabase já configurado com as tabelas e gatilhos da TS Refrigeração. O fechamento da OS usa `status = Concluída` e registra a conclusão; os recebimentos continuam em `pagamentos`, separados do faturamento da OS.
