# Checklist de lançamento

Tudo é gerado na pasta de trabalho (`~/translations/dragon-quest-8-3ds-ptbr`), que NÃO vai para o GitHub.

1. Validar: `python3 analise/dq8.py validar dialogos` e `validar sistema` (0 problemas) e
   `python3 analise/marcar_glossario.py --simular` (0 a marcar).
2. Montar as duas versões:
   - Completa: `python3 analise/dq8.py montar teste/layeredfs_X`
   - Purista: `python3 analise/dq8.py montar teste/layeredfs_X_en --nomes-en todos --sem-imagens`
3. Testar as duas no Azahar (copiar para `load/mods/`): título, novo jogo, primeira cena, menu, uma batalha, salvar e
   carregar.
4. Atualizar a versão no título do README, no LEIA-ME e no nome do zip.
5. Montar o zip `DQ8_3DS_PTBR_vX.zip`: pasta `DQ8_3DS_PTBR_vX/` com LEIA-ME.txt, LICENSE.txt,
   `LayeredFS-Completa/000400000018F100/` e `LayeredFS-Purista/000400000018F100/`.
6. Commit, tag `vX` e Release com o zip anexado (conta 0xdhx0, remoto `git@github-0xdhx0:...`). Pre-release enquanto
   for beta.
