# Nove domingos — plano de natação

Plano de retorno à natação (1×/semana, domingos) como alternativa cardio à corrida, com baixo impacto lombar. Nadador experiente voltando após 3 anos parado.

A página principal é o **`index.html`** — plano interativo com calculadora de CSS, seletor de sessão e registro das sessões feitas. Os mesmos dados existem em Markdown (`plano.md` e `registros/`) para durabilidade e para uso por outras ferramentas.

## Princípios do plano

1. **Tempo é o teto, volume é consequência.** Sessões regulares ≤ 55 min (calibrado pela sessão 04, que levou 52 min). O volume flutua entre 1.350 e 1.550 m conforme a intensidade.
2. **Todas as séries partem do CSS** (Critical Swim Speed), medido em contrarrelógios de 400 e 200 m: `CSS = (T400 − T200) ÷ 2` por 100 m. Valor atual: **2'38"/100 m** (ajustado em 06 set — a conta do teste dava 2'47", refutada pela sessão 06).
3. **Crawl carrega a carga (~70%), costas dá variedade (~25–30%), peito fica fora** (extrusão L5-S1). Costas sempre com **pé de pato** — máximo de costas medido em 3'19"/100 significa que blocos moderados cairiam abaixo do piso lombar de 3'10"/100.
4. **O portão para subir volume é a contagem de braçadas por 50 m**, não a tabela: o custo articular do ombro é número de braçadas, não metros.
5. **Freio:** desconforto de ombro que dura além do treino → repete o volume anterior. Sintoma lombar → sai da água.

## Estado atual

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
| 11 | — | Prescrita (ver `plano.md` ou `index.html`) |
| 12 | — | Reteste (10 min entre contrarrelógios; costas em domingo separado) |

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
2. Atualize o card correspondente no `index.html` (estrutura executada + resultados, padrão das sessões 04 e 05).
3. `git add -A && git commit -m "Sessão NN" && git push`
