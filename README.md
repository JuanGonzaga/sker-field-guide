# Sker · Guia de campo

Site estático em português para consultar 21 armas, comparar dano e entender Miracles, perks, Super Charger e drops de Sker Ritual. Sem framework, dependências ou instalação. Funciona no celular e compartilha os filtros pelo endereço.

## Publicar no GitHub Pages

1. Crie um repositório público, por exemplo `sker-field-guide`, na sua conta GitHub.
2. Envie **o conteúdo desta pasta** para a raiz do repositório, na branch `main` (incluindo todos os arquivos). Não envie apenas o ZIP.
3. No repositório, abra **Settings → Pages → Build and deployment → Source → Deploy from a branch → main → /(root)**.
4. Clique em Save. O Pages publicará o site automaticamente.
5. Aguarde o deploy. O endereço esperado é `https://SEU-USUARIO.github.io/sker-field-guide/`.

Alternativa sem Actions: escolha **Deploy from a branch → main → /(root)** em Settings → Pages. O site não precisa de build.

## Desenvolvimento

Abra `index.html` no navegador. Todos os dados usados pelo app vêm de `data.js`; não há requisição à wiki nem necessidade de servidor. Para atualização, edite esse arquivo. `weapons.json` guarda os mesmos dados em JSON para reutilização; mantenha os dois sincronizados.

Cada arma: `[nome, modo, carregador ou null, dano base no corpo, [headshot Base, I, II, III, IV, V]]`. Corpo e crítico são calculados com progressão 2× e crítico 2×. Headshots preservam valores arredondados da fonte.

`app.js` contém também os catálogos de Miracles (seleção de 14), perks e drops. A comparação não calcula DPS nem combina automaticamente os bônus.

## Fontes e limitações

Dados da Sker Ritual Wiki / Fandom: [Weapons](https://sker.fandom.com/wiki/Weapons), [Miracles](https://sker.fandom.com/wiki/Miracles), [Perks](https://sker.fandom.com/wiki/Perks), [Mechanics](https://sker.fandom.com/wiki/Mechanics). Consulta: 24/10/2026, a partir de conteúdo indexado meses antes. Não são dados extraídos do patch atual. Números de Perks e Machines divergem; confirmar no jogo.

Classes S–D medem dano por impacto relativo ao maior dano do catálogo no mesmo nível: S ≥ 50%, A ≥ 25%, B ≥ 10%, C ≥ 5%, D < 5%. Fases são uma convenção de melhoria, não disponibilidade. A God Killer exige desbloqueios de endgame. Escopetas exibem dano por pellet, não total por disparo. Beginner tem progressão própria e não é coberto pela tabela.

Conteúdo da comunidade adaptado sob CC BY-SA, conforme a licença da fonte. Tradução e organização são adaptações; consulte o histórico das páginas originais para autoria. Projeto não oficial, sem afiliação com Wales Interactive. Código original deste projeto: MIT (LICENSE). Dados e textos derivados da wiki mantêm a licença da fonte.
