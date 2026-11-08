# Domingos — plano de natação

Plano de natação 1×/semana (domingos), hoje o cardio principal, com baixo impacto lombar. Nadador experiente que voltou após 3 anos parado. Dois ciclos: **ciclo 1** (sessões 04–12, ago–nov 2026, concluído) e **ciclo 2** (sessões 13–20, nov 2026–jan 2027, em curso).

A página principal é o **`index.html`** — plano interativo com calculadora de CSS, abas por ciclo (ciclo 2 abre primeiro; ciclo 1 fica em aba separada), seletor de sessão e registro das sessões feitas. Os mesmos dados existem em Markdown (`plano.md` e `registros/`) para durabilidade e para uso por outras ferramentas.

## Princípios do plano

1. **Tempo é o teto, volume é consequência.** Sessões regulares ≤ 55 min (calibrado pela sessão 04, que levou 52 min). Volume flutua conforme a intensidade: 1.350–1.550 m no ciclo 1, 1.500–1.700 m no ciclo 2.
2. **Todas as séries partem do CSS** (Critical Swim Speed), medido em contrarrelógios de 400 e 200 m: `CSS = (T400 − T200) ÷ 2` por 100 m. Valor atual: **2'45"/100 m** (reteste de 8 nov: 400 em 10'05", 200 em 4'30" → 2'47", igual a agosto; o ajuste de setembro para 2'38" superestimava o limiar).
3. **Crawl carrega a carga; peito fica fora** (extrusão L5-S1). **Costas** no ciclo 1 era ~25–30% do volume; no ciclo 2 fica só no aquecimento e na volta à calma (100 + 100 m). **Sempre com pé de pato** (curto, não longo): o máximo de costas medido em 3'19"/100 significa que blocos moderados cairiam abaixo do piso lombar de 3'10"/100 — sem sustentação da perna o quadril afunda e a lombar arqueia. Única exceção: o 200 máximo de teste (05, 13), com critério de abortar.
4. **O portão para subir volume é a contagem de braçadas por 50 m**, não a tabela: o custo articular do ombro é número de braçadas, não metros.
5. **Pausa fixa, pace variável** (ciclo 2). Se o alvo não se sustenta com a pausa prescrita, desacelera 2"/100; nunca alonga a pausa — no ciclo 1 as pausas esticadas transformaram séries de limiar em tiros.
6. **Freio:** desconforto de ombro que dura além do treino → repete o volume anterior. Sintoma lombar → sai da água.

## Ciclo 2 — por quê e o quê

O reteste de 8 nov mostrou que as 10 semanas do ciclo 1 melhoraram velocidade e capacidade anaeróbia (400 e 200 caíram 25" cada; D′ de ~24 → ~39 m) mas não o limiar (CSS 2'47" nas duas medições). O ciclo 2 tem um estímulo só — crawl perto do CSS, pausa curta, blocos cada vez mais longos — e um critério de sucesso: **na sessão 20, o 400 melhorar mais que o 200.**

| Sessão | Bloco principal | Vol | Status |
|---|---|---|---|
| 13 | Teste de costas (200 máx, sem pé de pato) + 4×100 @ 2'48" c/ 15" | 1.300 | prevista |
| 14 | 4×200 @ 5'36" (CSS+3") c/ 20" | 1.500 | prevista |
| 15 | 3×300 @ 8'27" (CSS+4") c/ 20" | 1.600 | prevista |
| 16 | 2×400 @ 11'16" (CSS+4") c/ 30" | 1.500 | prevista |
| 17 | 1.000 contínuo @ 2'50", negative split 2'52" → 2'48" — checagem | 1.700 | prevista |
| 18 | 5×200 @ 5'34" (CSS+2") c/ 15" | 1.700 | prevista |
| 19 | 2×500 @ 14'10" (CSS+5") c/ 30" | 1.700 | prevista |
| 20 | Reteste 400/200, protocolo idêntico à 12 | 1.450 | prevista |

Sem domingos pulados, 13 = 15 nov 2026 e 20 = 3 jan 2027. Feriados deslocam a numeração, não o conteúdo.

## Ciclo 1 — concluído

| Sessão | Data | Status |
|---|---|---|
| 04 | 22 ago 2026 | ✅ Teste de crawl — CSS 2'47" provisório |
| 05 | 29 ago 2026 | ✅ Teste de costas — 3'19"/100, razão 1,35–1,40× |
| 06 | 6 set 2026 | ✅ 5×100 a 2'36"–2'43" → CSS ajustado para 2'38" |
| R | fim set 2026 | ✅ Retorno pós-ombro (2 semanas paradas) — 6×100 a ~2'34" |
| 07 | out 2026 | ✅ 3×200 a 5'19" → 5'15" → 5'08" (pausas longas) |
| 08 | out 2026 | ✅ 800 em 11'50" + 11'00" — checagem inconclusiva |
| 09 | 18 out 2026 | ✅ 8×75 a 1'55"–2'00" (alvo 2'00") |
| 10 | 25 out 2026 | ✅ 4×150 a 3'50"–4'00" (alvo 4'01") |
| 11 | 1 nov 2026 | ✅ 10×50 a 1'05"–1'10" (alvo 1'18") |
| 12 | 8 nov 2026 | ✅ Reteste: 400 em 10'05", 200 em 4'30" → CSS 2'47" (D′ ~24 → ~39 m) |

## Como publicar no GitHub Pages

```bash
# 1. Crie um repositório vazio em github.com (ex.: natacao-domingos), sem README

# 2. Neste diretório:
git remote add origin https://github.com/SEU_USUARIO/natacao-domingos.git
git branch -M main
git push -u origin main

# 3. No GitHub: Settings → Pages → Source: "Deploy from a branch"
#    Branch: main, pasta / (root) → Save

# A página fica em https://SEU_USUARIO.github.io/natacao-domingos/
```

O e-mail do commit inicial é um placeholder. Para trocar:

```bash
git config user.name "Seu Nome"
git config user.email "seu@email.com"
git commit --amend --reset-author --no-edit
```

## Como registrar uma sessão feita

1. Copie `registros/_modelo.md` para `registros/AAAA-MM-DD-sessao-NN.md` e preencha.
2. Atualize o card correspondente no `index.html` (estrutura executada + resultados, padrão das sessões 04 e 05) e acrescente a classe `done` ao `<article class="sess ...">` — o seletor abre automaticamente na primeira sessão sem `done`.
3. Atualize a linha da sessão nas tabelas acima e, se o reteste mudar o CSS, o campo "CSS ajustado" no `index.html`.
4. `git add -A && git commit -m "Sessão NN" && git push`
