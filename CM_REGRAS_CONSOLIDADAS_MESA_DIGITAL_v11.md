# CORAÇÕES E MENTES — Regras operacionais do playtest de 48 cartas

Versão 11 · 20/10/2026 · Alinhamento à Bíblia v0.6.

Este documento descreve a implementação local. Não modifica a Bíblia, a planilha ou o CSV canônicos. Para regras, prevalece a Bíblia v0.6; para dados, a aba Cartas_48 da planilha V3.5 e seu CSV V4 conferido.

## 1. Componentes e objetivo

- 48 cartas físicas, com face azul e face vermelha: 96 faces.
- Dois ícones diferentes por face, entre os oito canônicos. Cada ícone ocorre 12 vezes em cada cor.
- 12 combos de cada cor, com quatro integrantes possíveis em cada combo. Toda face pertence a exatamente um combo.
- Tabuleiro normal de quatro linhas e seis colunas: 24 casas. Vence o maior total quando todas estiverem ocupadas; totais iguais empatam.

A face visível determina a posse da carta no tabuleiro. Só seus ícones e seu combo contam; o verso não pontua nem fornece apoios.

## 2. Preparação

Distribuir quatro cartas abertas por jogador, alternando Azul e Vermelho. Sortear quem fará a primeira jogada. Revelar as duas cartas do topo do monte: A e B.

Quem não começa escolhe qual das duas ficará na sua cor; a outra fica na cor de quem começa. Colocar A em L2C3 e B em L3C4. Essa escolha não é jogada nem conversão. A nova carta do topo é a carta pública. O jogador sorteado começa.

Na revanche, quem perdeu começa e o adversário escolhe a abertura. Em empate, fazer novo sorteio.

## 3. Turno e carta pública

Cada turno coloca exatamente uma carta, na cor de quem joga, em qualquer casa livre. São três modalidades:

1. Colocar da mão e repor com a carta pública.
2. Colocar a carta pública diretamente, sem alterar a mão.
3. Colocar da mão e converter uma carta adversária vizinha, sem reposição.

Converter é opcional. A pública nunca converte. Com a mão vazia, o jogador continua usando a pública. Suas duas representações na interface são a mesma carta física. Não há descarte, movimento de peças ou conversão sem colocação.

Ninguém converte na própria primeira jogada: os turnos 1 e 2 da partida aceitam apenas colocação normal.

## 4. Adjacência e conversão

Adjacência inclui lados e cantos, nas oito direções, respeitando as bordas do tabuleiro. Não é exigida para colocar; é exigida entre cada apoio e o alvo.

Para converter um alvo adversário com ícones X e Y:

1. Colocar uma carta da mão numa casa livre vizinha ao alvo.
2. A carta nova deve mostrar X ou Y.
3. Outra carta aliada, que já estava no tabuleiro e é vizinha ao alvo, deve mostrar o outro ícone.

Se a nova carta mostrar os dois ícones, continua sendo necessário um apoio antigo com qualquer um deles. Uma carta não cobre sozinha os dois ícones.

Se o alvo estiver num combo ativo, são necessários três apoios aliados diferentes, todos vizinhos ao alvo e todos com algum ícone dele. Entre esses apoios, a nova carta e uma antiga continuam cobrindo os dois ícones, respectivamente.

Virar apenas um alvo. Os apoios ficam no lugar. Não há reposição, propagação automática nem dispensa de ícones por completar outro combo. Recalcular pontos e proteção imediatamente.

## 5. Combos de três e quatro

Para cada combo e cor, considerar somente seus integrantes atualmente visíveis nessa cor. Encontrar os componentes conectados pelas oito direções, usando exclusivamente peças desse combo como caminho.

- Três integrantes conectados: combo ativo, +3 pontos e proteção nas três cartas.
- Quatro conectados: um único combo ativo, +4 pontos e proteção nas quatro cartas.
- Três conectados e um isolado: +3; somente o trio tem proteção.
- Dois pares desconectados: nenhum combo ativo, nenhum bônus ou proteção de combo.

Não somar os diferentes subconjuntos de três de um combo de quatro. Cartas externas não servem de ponte. Colocação e conversão podem ativar combos.

Depois de converter uma peça de um combo de quatro, as três restantes mantêm +3 e proteção se continuarem conectadas. Se a conversão separar as três, o combo deixa de estar ativo. Uma quarta carta incorporada posteriormente ganha a mesma proteção, sem depender da ordem das jogadas.

## 6. Pontuação

- Grupo conectado de três ou mais cartas da mesma cor: 1 ponto por carta.
- Para cada ícone, cadeia conectada de três ou mais cartas dessa cor com esse ícone: +1 por carta da cadeia.
- Uma carta pode somar pelos dois ícones, até +2. Caminhos múltiplos não repetem o ponto do mesmo ícone na mesma carta. Cartas sem o ícone não fazem ponte.
- Combo ativo: +3 ou +4, conforme o tamanho do componente conectado.

Total = grupos + ícones + combos. O placar é recalculado a cada jogada e não acumula pontos históricos. Mãos e monte não pontuam. Resolver a eventual conversão da última jogada antes de encerrar nas 24 casas.

## 7. Leitura das cartas

A miniatura mantém título, cor, ícones e os dois combos. Vinhetas e versos podem ser exibidos pelas opções existentes. A barra de título abre a ampliação; Virar consulta a outra face.

A ampliação apresenta título, vinheta, dois ícones, defesa do valor, contraponto e os dois combos no rodapé. Os textos são independentes e literais:

- Face azul: defesa em seta azul para a direita; contraponto em seta vermelha para a esquerda.
- Face vermelha: defesa em seta vermelha para a esquerda; contraponto em seta azul para a direita.

O sentido das setas é desenhado pela interface. Os textos não ganham símbolos ou alterações editoriais. Os caminhos de vinheta vêm do CSV, mesmo quando conservam um título antigo no nome do arquivo.

## 8. Computador e modos de uso

Iniciante mantém a avaliação imediata e variação entre alternativas legais. Experiente avalia a diferença de pontos e respostas adversárias. Ambos usam o mesmo motor de legalidade e pontuação e reconhecem os componentes de combo. Nenhum recebe a ordem oculta do monte.

A observação da IA contém somente tabuleiro, mãos abertas, carta pública, quantidade de cartas restantes e, durante a abertura, as duas cartas reveladas. O trabalho ocorre em Worker, sem bloquear a interface.

O modo jogador não exibe IDs ou códigos de combo. O laboratório mantém sementes, parâmetros, cálculo detalhado, históricos, exportação e demonstração. Salvamento, desfazer e consulta são ferramentas de playtest; não são novas jogadas de mesa.

## 9. Tutorial e compatibilidade

O tutorial existente conserva cinco rodadas guiadas em 4 × 4 e prossegue na mesma partida até ocupar 16 casas. Usa os dados atuais de 48 cartas, com uma ordem preparada para ensinar. Seu salvamento é separado da partida normal. Os textos didáticos do roteiro permanecem coerentes com as cartas efetivamente usadas.

As novas partidas usam exclusivamente 48 cartas. Novos salvamentos registram versão do baralho e das regras. Arquivos de 40 cartas são históricos: validam-se suas jogadas com os motores anteriores e abrem-se somente para consulta e reprodução. Não podem receber novas jogadas ou ser convertidos silenciosamente para 48 cartas. A pontuação original da primeira versão, com um único bônus de ícone por carta, também é preservada na reprodução.

O salvamento anterior de 40 no navegador não é sobrescrito. A tela inicial oferece sua consulta quando presente. Um arquivo histórico exportado mantém seu formato original, cursor e estado reproduzido. Tutoriais anteriores permanecem guardados na chave antiga; o tutorial atual usa uma chave própria.

## 10. Limites e publicação

Não estão incluídos cartas cinzas, fusões ou cartas da futura V2.0, revisão editorial, alterações de arte, multiplayer remoto ou novas regras de pontuação.

A atualização é local e aguarda conferência do autor. Gerar arquivos em publish não envia conteúdo ao GitHub nem altera o site público. A publicação deve incluir a pasta assets, pois o HTML do site utiliza imagens externas. Os arquivos ABRIR_JOGO permanecem independentes, com imagens incorporadas, para uso sem internet.
