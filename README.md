# 📦 Sistema de Contagem de Estoque (Mobile-First)

Sistema web autocontido em um único arquivo (`index.html`) projetado especificamente para operadores realizarem a conferência física e contagem de estoque em lojas e depósitos. 

O sistema integra o envio direto do relatório formatado para o **WhatsApp fixo (+55 11 98278-5102)**.

---

## 🚀 Demonstração e Acesso Online

- **Aplicação Online (GitHub Pages):** [https://vitornsc077.github.io/software-contagem-estoque/](https://vitornsc077.github.io/software-contagem-estoque/)
- **Arquivo Local:** Basta abrir o `index.html` em qualquer navegador (celular, tablet ou computador). Não requer instalação de servidor nem dependências externas.

---

## ✨ Principais Recursos

- **📱 Abordagem Mobile-First Ergonômica:**
  - Botões touch amplos (`+` e `−`) com tamanho mínimo de 46px para facilitar o toque com o polegar.
  - Campos numéricos com `inputmode="numeric"` para abrir diretamente o teclado numérico em dispositivos móveis.
  - Barra inferior fixa para rápida visualização dos totais e finalização a qualquer momento.

- **🎨 Paleta Laranja Pastel & Alto Contraste:**
  - Desenvolvida com fundo suave (`#fef5ee`) e tipografia escura em tons quentes (`#291811` / `#5c4135`), garantindo conforto visual prolongado e máxima legibilidade.

- **📋 Catálogo Pré-Cadastrado (105 Itens):**
  - **Geladeira (27 produtos):** Hot miola, Ketchup, Mostarda, Milho, Cebola branca, Pimenta jalapeno, Cebola caramelizada, Geleia de bacon, Tomate em cubos, Chedar, Maionese verde, Baconnaise, Sour cream, Pct tomate, Pct alface crespa, Caixa de carne, Pct limão, Pct de Bacon, Requeijão cremoso, Chantilly, Maionese vigor, Pct mussarela, Cebola roxa, Pct alface americana, Toucinho defumado, Farofa de bacon, Leite.
  - **Freezer (23 produtos):** Pacote de batata, Pct de hambúrguer RP, Pct de salsicha, Pão Brioche, Pacote de bacon fechado, Pct pão sem glúten, Disco de alho, Saco cebola crua, Purê, Molho de frango, Caixa de hambúrguer vegetal, Palito de requeijão, Coxinha de queijo, Coxinha de frango, Porção de frango, Pct molho de frango, Saco de molho de costela, Pct Nuggets, Cebola branca, Carne moída, Presunto, Disco de gorgonzola, Disco de bacon.
  - **Prateleira (41 produtos):** Caixa pão Brioche, Caixa pão hot-dog, Hambúrguer do RP, Pacotes de Barquinha, Caixa guardanapo RP, Caixa aberta sacola vinho miola, Caixa aberta sacola RP, Pct tampa bolha, Pct bobina picotada, Pacote de selante, Bobina de impressora, Rolo de linha, Sal de batata Miola, Sal de batata RP, Pct de chá, Pct ovo maltine, Pct chocolate, Pct paçoca, Pct de confete, Granulado de chocolate, Pct de leite em pó, Pct doce de leite, Pct bases de baunilha, Pct batata palha, Caixas de Heineken, Caixa de cotuba, Cotubas 0, Pacote de guaraná, Pacote de guaraná 0, Pacote de coca, Groselha, Molho Chipotle, Ketchup real, Pct copo salão, Pct copo cozinha, Pote de batata, Fardo de água, Pão gergelim, Molho american chicken, Molho GRILL, Cebola crispy.
  - **Bar (14 produtos):** Coca, Coca LT 0, Coca KS 0, Coca KS, Turbaína, Guaraná, Guaraná 0, Pudim, Eisenbahn, Heineken, Água, Água com gás, Garrafa de berry, Garrafa passion.
  - **Adição de Produtos Avulsos:** Botão ao final de cada categoria para incluir produtos não previstos no catálogo.

- **🔍 Foco por Estação de Trabalho & Busca Rápida:**
  - Abas que filtram por ambiente (`❄️ Geladeira`, `🧊 Freezer`, `📦 Prateleira`, `🍹 Bar`) para reduzir sobrecarga de informação.
  - Aba especial **Contados (>0)** para conferir apenas o que já foi registrado.
  - Campo de pesquisa global instantânea com suporte a busca sem acentos e botão de limpar (`×`).

- **💾 Persistência Automática:**
  - Todos os lançamentos e itens customizados são salvos em tempo real no `localStorage` do navegador. Se a página for recarregada ou fechada, nada é perdido.
  - Botão **Zerar** com confirmação de segurança para iniciar nova contagem.

- **🧠 Integração com o Segundo Cérebro (Obsidian Vault):**
  - Conexão e sincronização direta com o seu Segundo Cérebro em `C:\Users\kelly\Documents\Obsidian Vault\Contagens\`.
  - Suporte à **Obsidian Local REST API** (`https://127.0.0.1:27124`) e exportação direta com 1 clique de notas `.md`.
  - Notas formatadas com Frontmatter YAML canônico, tags (`#segundo-cerebro`, `#agentes`, `#estoque`), callouts de síntese e wikilinks para o `[[00 - 🧠 Cérebro Central & Governança/🧠 Cérebro Central - Second Brain Master Hub|🧠 Master Hub]]` e classificações `MEM-ORQ` e `MEM-WEB`.

- **🤖 Hub de Indução de Agentes Autônomos de IA:**
  - **🛒 Agente de Compras & Reposição (AGENT-BUY):** Analisa rupturas imediatas (≤ 2 un) e gera ordens de compra organizadas por fornecedor (Padaria, Açougue/Frigorífico, Hortifrúti, Laticínios e Bebidas).
  - **🛡️ Agente de Auditoria & Prevenção de Perdas (AGENT-AUDIT):** Audita a cadeia de frio, perecibilidade de queijos, carnes moídas, toucinho e molhos caseiros sob a regra PEPS/FIFO.
  - **👨‍🍳 Agente de Operações & Chapa (AGENT-OPS):** Traduz matérias-primas na capacidade real de entrega de hambúrgueres do próximo turno, identificando o insumo gargalo e direcionando o mise en place da chapa.
  - **🧠 Agente Cérebro Central (AGENT-BRAIN):** O nó mestre que calcula o Health Score do estoque (0 a 100) e compila o Despacho Executivo para a gerência.
  - **⚡ Diagnóstico Heurístico em Tempo Real:** Gera métricas e insights acionáveis imediatos na tela a cada contagem.
  - **📜 Prompts Canônicos de Indução (1-Click):** Copia prompts profissionais de sistema estruturados para induzir qualquer LLM (Claude, ChatGPT, Gemini, Antigravity ou agentes n8n).

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

  🍹 *BAR*
  • Coca: *6 un*
  • Heineken: *12 un*
  • Pudim: *4 un*

  ━━━━━━━━━━━━━━━━━━━━━
  📊 *RESUMO GERAL:*
  • Itens Contados: *7 tipos*
  • Total de Unidades: *33 un*
  ━━━━━━━━━━━━━━━━━━━━━
  ✅ _Enviado via sistema móvel de contagem._
  ```

---

## 🛠️ Tecnologias Utilizadas

- **HTML5 Semântico**
- **CSS3 Vanilla Moderno**
- **JavaScript ES6+ Puro** (Sem dependências externas)
- **Google Fonts** (*Plus Jakarta Sans*)

---

## 📄 Licença

Distribuído sob a licença MIT.
