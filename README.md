# DigitaHinos ViolaCaipira

Visualizador/compositor MIDI com **viola caipira** animada (10 cordas = 5 ordens de cordas duplas), derivado do Violão Bounce: biblioteca de hinos, escolha de voz, tom automático, acompanhamento (Fingerstyle básico/profissional ou Acompanhamento em batida/dedilhado), mão esquerda animada, compositor de tablatura, exportação WAV/MIDI/JSON/PDF e modo Pro.

## Viola caipira
- 5 ordens, cada uma com 2 cordas: **5ª, 4ª e 3ª em oitava** (a corda fina soa uma oitava acima), **2ª e 1ª em uníssono**. O som toca as duas cordas de cada ordem.
- Afinações (seletor no app e no editor), da 5ª à 1ª ordem (nota da corda grave do par):
  - **Cebolão em Mi** (padrão): Si Mi Sol♯ Si Mi
  - **Cebolão em Ré**: Lá Ré Fá♯ Lá Ré
  - **Rio Abaixo**: Sol Ré Sol Si Ré
  - **Boiadeira**: Sol Ré Fá♯ Lá Ré
- A pauta é escrita uma oitava acima do som real. A tablatura tem 5 linhas (uma por ordem).
- Formas de acorde geradas automaticamente para a afinação escolhida (nos cebolões, pestana inteira numa casa); a mão escolhe a forma mais próxima da melodia.
- Baixo contínuo nas 3 ordens graves; melodia nas 2 agudas. Mão direita p-i-m-a.
- Trocar a afinação refaz acordes, digitação e o editor (as notas mantêm a altura).

## Publicação
- GitHub Pages: suba os arquivos. A cada versão nova, mude `CACHE_NAME` em `sw.js` (agora `viola-bounce-v1`).
- APK: workflow `.github/workflows/build-apk.yml` (Capacitor), appId `io.github.capuchowpdesign.violabounce`.
- Modo Pro: `pro-config.js` usa `app: 'viola'`; a planilha/Apps Script precisa aceitar esse nome de app.

## PDF da tablatura (exclusivo Pro)
Botão **📄 PDF** no player: baixa a tablatura da versão que está tocando (voz, tom, afinação e estilo escolhidos). No modo grátis o botão (🔒) só abre a tela do Pro; não há amostra.

## Harmonia "Cantoral (livro)"
Em **Harmonia** há a opção *Cantoral (livro)*, que usa as cifras do livro (`hinos/cifras.json`, hino a hino: compasso, tempo, raiz e tipo do acorde). As formas de acorde continuam sendo geradas para a afinação escolhida. Hinos sem cifra no arquivo seguem com a harmonia automática.

## Estilo "Acompanhamento"
Em **Estilo** há: *Fingerstyle · básico*, *Fingerstyle · profissional (dedilhado)* e **Acompanhamento**.
No Acompanhamento a viola toca só as cifras e o **soprano toca ao fundo** (flauta, violino, harmônio ou violão; campo *Soprano ao fundo*).
- **Ritmo:** *Batida* (golpes ↓ ↑) ou *Dedilhado* (P = baixo do acorde; I = 3ª ordem; M = 2ª ordem; A = 1ª ordem).
- **Contagem:** os movimentos seguem a contagem do compasso do hino.
  - *Simples*: um movimento por tempo. Ex.: 6/8 = batida ↓↓↑↓↓↑ e dedilhado P I M A M I; 4/4 = P I M A; 3/4 = P IMA IMA.
  - *Subdividida*: "1 e 2 e 3 e…", o dobro de movimentos. Ex.: 6/8 = P I M A M I P I M A M I.
  - *Mista*: primeira metade do compasso simples e segunda subdividida. Ex.: 4/4 = ↓ ↓ ↑↓↑↓ ↓↑↓↑.

## Correções
- Notas que sumiam na virada do verso para o coro (hinos 6, 41, 61 e outros 30): a numeração das casas de repetição no arquivo começava no 2, e o app pulava o último compasso do verso.
- Cordas soltas: sempre que uma ordem solta dá a mesma nota e não está em uso por outra nota, o app usa a corda solta em vez de apertar a casa.
