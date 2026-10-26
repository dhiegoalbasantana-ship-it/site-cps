# Projeto Landing Page - Fisioterapia & Osteopatia (Integrado com Supabase)

Site de alta conversão adaptável com formulário inteligente que salva os leads no **Supabase** e dispara direto para o **WhatsApp**.

---

## ⚡ Como testar agora mesmo
1. Abra a pasta `landing-osteopatia` e dê 2 cliques no `index.html`.
2. O site já funciona imediatamente mesmo sem Supabase configurado (o formulário direciona direto para o WhatsApp com os dados preenchidos).

---

## 🗄️ Como conectar seu Supabase Grátis (Opcional, mas agrega muito valor)
1. Crie uma conta no [supabase.com](https://supabase.com) com seu novo e-mail.
2. Crie um novo projeto (ex: `osteopatia-leads`).
3. Vá em **SQL Editor** no menu esquerdo e cole o conteúdo do arquivo `supabase_setup.sql`. Clique em **Run**.
4. Vá em **Project Settings** -> **API** e copie:
   - **Project URL**
   - **anon public key**
5. Abra o `index.html`, vá até o final e substitua no objeto `CLIENT_SETUP`:
   ```javascript
   supabaseUrl: "https://SEU_PROJETO.supabase.co",
   supabaseAnonKey: "SUA_CHAVE_ANON"
   ```
Pronto! Toda vez que um paciente solicitar agendamento pelo site:
1. O lead é salvo no banco de dados Supabase com data e hora.
2. O WhatsApp do profissional abre automaticamente já com o texto pronto!

---

## 🔄 Como migrar para outro cliente em 1 minuto:
Se o Dr. Israel não fechar e você for apresentar para outro fisioterapeuta:
No `index.html`, aperte `Ctrl + H`:
- Troque `Dr. Israel Silva` pelo nome do novo cliente.
- Troque `5511999999999` pelo WhatsApp dele.
- Troque `Centro de Postura e Saúde` pelo nome do novo consultório.
- Troque a foto na pasta `assets` se quiser colocar a foto do novo cliente.
