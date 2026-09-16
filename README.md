# 📦 Sistema de Contagem de Estoque (Mobile-First)

Sistema web autocontido em um único arquivo (`index.html`) projetado especificamente para operadores realizarem a conferência física e contagem de estoque em lojas e depósitos. 

O sistema integra o envio direto do relatório formatado para o **WhatsApp** e o salvamento sincronizado de notas no **Obsidian** via plugin **Local REST API**.

---

## 🚀 Demonstração e Acesso Online

- **Aplicação Online (GitHub Pages):** [https://vitornsc077.github.io/software-contagem-estoque/](https://vitornsc077.github.io/software-contagem-estoque/)
- **Arquivo Local:** Basta abrir o `index.html` em qualquer navegador (celular, tablet ou computador). Não requer instalação de servidor nem dependências externas.

---

## ✨ Principais Recursos

- **📱 Abordagem Mobile-First Ergonômica:**
  - Botões touch amplos (`+` e `−`) com tamanho mínimo de 44px a 48px para facilitar o toque com o polegar.
  - Campos numéricos com `inputmode="numeric"` para abrir diretamente o teclado numérico em dispositivos móveis.
  - Barra inferior fixa para rápida visualização dos totais e finalização a qualquer momento.

- **☀️ Paleta Clara de Alto Contraste:**
  - Desenvolvida com fundo claro (`#f4f6f9` / `#ffffff`) e tipografia escura (`#0f172a` / `#334155`), garantindo máxima legibilidade mesmo sob luz forte ou reflexos comuns em áreas operacionais.

- **📋 Catálogo Pré-Cadastrado (74 Itens):**
  - **Geladeira (22 produtos):** Hot miola, Ketchup, Mostarda, Milho, Cebola branca, Pimenta jalapeno, Cebola caramelizada, Geleia de bacon, Tomate em cubos, Chedar, Maionese verde, Baconnaise, Sour cream, Pct tomate, Pct alface crespa, Caixa de carne, Pct limão, Pct de Bacon, Requeijão cremoso, Chantilly, Maionese vigor, Pct mussarela.
  - **Freezer (16 produtos):** Pacote de batata, Pct de hambúrguer RP, Pct de salsicha, Pão Brioche, Pacote de bacon fechado, Pct pão sem glúten, Disco de alho, Saco cebola crua, Purê, Molho de frango, Caixa de hambúrguer vegetal, Palito de requeijão, Coxinha de queijo, Coxinha de frango, Porção de frango, Pct molho de frango.
  - **Prateleira (36 produtos):** Caixa pão Brioche, Caixa pão hot-dog, Hambúrguer do RP, Pacotes de Barquinha, Caixa guardanapo RP, Caixa aberta sacola vinho miola, Caixa aberta sacola RP, Pct tampa bolha, Pct bobina picotada, Pacote de selante, Bobina de impressora, Rolo de linha, Sal de batata Miola, Sal de batata RP, Pct de chá, Pct ovo maltine, Pct chocolate, Pct paçoca, Pct de confete, Granulado de chocolate, Pct de leite em pó, Pct doce de leite, Pct bases de baunilha, Pct batata palha, Caixas de Heineken, Caixa de cotuba, Cotubas 0, Pacote de guaraná, Pacote de guaraná 0, Pacote de coca, Groselha, Molho Chipotle, Ketchup real, Pct copo salão, Pct copo cozinha, Pote de batata.
  - **Adição de Produtos Avulsos:** Botão ao final de cada categoria para incluir produtos não previstos no catálogo.

- **🔍 Busca Rápida e Filtros Inteligentes:**
  - Campo de pesquisa global instantânea com botão de limpar (`×`).
  - Abas de categoria com contadores dinâmicos de progresso (ex: `14/22 contados`).
  - Aba especial **Contados (>0)** para revisar rapidamente apenas os itens que tiveram quantidades lançadas.

- **💾 Persistência Automática:**
  - Todos os lançamentos e itens customizados são salvos em tempo real no `localStorage` do navegador. Se a página for recarregada ou fechada, nada é perdido.
  - Botão **Nova Contagem** com confirmação de segurança para zerar os dados ao iniciar uma nova rodada.

---

## 📲 Integração com WhatsApp

- **Destino Fixo:** O número `+55 11 98278-5102` (`5511982785102`) está configurado no sistema e não pode ser editado acidentalmente pelo operador.
- **Link Gerado Automaticamente:** `https://wa.me/5511982785102?text=...`
- **Exemplo de Mensagem Formatada:**
  ```text
  📋 *RELATÓRIO DE CONTAGEM DE ESTOQUE*
  🗓 *Data:* 16/09/2026 às 01:45
  ━━━━━━━━━━━━━━━━━━━━━

  ❄️ *GELADEIRA*
  • Hot miola: *2 un*
  • Ketchup: *3 un*

  🧊 *FREEZER*
  • Pacote de batata: *5 un*

  📦 *PRATELEIRA*
  • Caixa pão Brioche: *1 un*

  ━━━━━━━━━━━━━━━━━━━━━
  📊 *TOTAL GERAL:*
  • Tipos de Itens Contados: *4*
  • Volume Total: *11 unidades*
  ━━━━━━━━━━━━━━━━━━━━━
  ✅ _Contagem conferida e registrada via sistema móvel._
  ```

---

## 🟣 Integração com o Obsidian (Local REST API)

O sistema conta com um painel de configurações acessível pelo ícone de engrenagem no cabeçalho:
- **URL do Servidor:** Padrão `https://127.0.0.1:27124` (ou `http://127.0.0.1:27123` para conexões não criptografadas).
- **Chave de API:** Campo tipo senha para colar a chave gerada nas configurações do plugin *Local REST API* no Obsidian.
- **Pasta de Destino no Vault:** Padrão `Contagens/` (ex: cria a nota `Contagens/Contagem - 2026-09-16 01-45.md`).
- **Botão Testar Conexão:** Valida se o Obsidian está aberto e respondendo antes do envio final.
- **Resiliência:** Caso o Obsidian esteja desligado ou haja falha na rede, o operador recebe um aviso amigável e o envio para o WhatsApp **continua normalmente sem interrupções**.

> **⚠️ Dica sobre Certificado SSL Local:**
> Por padrão, o plugin do Obsidian usa HTTPS com certificado autoassinado. Na primeira vez em um novo navegador/celular, acesse a URL `https://127.0.0.1:27124` e aceite o aviso de segurança ("Avançado > Continuar"), ou configure o plugin no Obsidian para permitir conexões HTTP na porta 27123.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 Semântico**
- **CSS3 Vanilla Moderno** (sem frameworks externos pesados)
- **JavaScript ES6+ Puro** (Modular, sem dependências externas)
- **Google Fonts** (*Plus Jakarta Sans*)

---

## 📄 Licença

Distribuído sob a licença MIT. Consulte `LICENSE` para obter mais informações.
