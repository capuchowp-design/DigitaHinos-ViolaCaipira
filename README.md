# Viola Bounce

Visualizador/compositor MIDI com **viola caipira** animada (10 cordas = 5 ordens de cordas duplas), derivado do Violão Bounce: biblioteca de hinos, escolha de voz, tom automático, acompanhamento (acordes + baixo, estilo básico ou dedilhado), mão esquerda animada, compositor de tablatura, exportação WAV/MIDI/JSON/PDF e modo Pro.

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
