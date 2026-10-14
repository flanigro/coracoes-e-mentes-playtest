# CORAÇÕES E MENTES — Regras consolidadas para mesa e digital

**Versão 10 · 14/10/2026 · Playtest de 40 cartas, com a expansão de 48 prevista (seção 13) · Alinhada à Bíblia v0.5 e ao manual v8.2**

*Mudanças da v9 para a v10:*
- **Regra:** no alvo em combo completo, as três cartas aliadas adjacentes precisam ter, cada uma, ao menos um símbolo em comum com o alvo (seção 7, item 7). Na v9, a terceira podia ter quaisquer símbolos.
- **Redação da cobertura:** a seção 7 passa a descrever a cobertura como na Bíblia (a carta nova cobre um símbolo; uma carta que já estava no tabuleiro cobre o outro). O resultado mecânico é o mesmo da v9.
- **Digital:** explicação obrigatória da conversão (seção 7); números de carta, códigos de combo e ferramentas de laboratório fora do modo jogador (seções 9 e 11); geometria do tutorial prevista (seção 11).

Este documento reúne as regras operacionais do baralho de mesa e do aplicativo, conforme as decisões do autor. **É regra canônica que nenhum jogador converte em sua primeira jogada.** Todo combo exige suas três cartas conectadas, com o mesmo nome de combo e a mesma cor. Não existe variante dessa regra. As demais decisões operacionais de interface são identificadas abaixo.

Os nomes, textos, pares de faces, oito símbolos e associações de combos não são alterados por este documento. A Bíblia v0.5 e a planilha de produção continuam sendo as referências editoriais. O baralho deste playtest é o de 40 cartas, em `CM_DATA_MERGE_FULL_v2_40.csv`. A expansão de 48 cartas está prevista e descrita na seção 13, mas ainda não está ativa no aplicativo.

## 1. Componentes e objetivo

- 40 cartas físicas, cada uma com uma face azul e uma vermelha.
- Exatamente dois símbolos por face, entre os oito símbolos do jogo.
- 10 combos azuis e 10 vermelhos; cada combo tem três cartas específicas.
- Tabuleiro com 4 linhas e 6 colunas: 24 casas, uma carta por casa.
- Dois jogadores, um azul e um vermelho. Vence quem tiver mais pontos quando todas as casas estiverem ocupadas. Pontuações iguais resultam em empate.

A cor da face voltada para cima determina a qual jogador a carta pertence no tabuleiro. A origem da carta não fixa sua posse: uma conversão muda sua cor e os símbolos visíveis.

## 2. Informações visíveis

As cartas das duas mãos ficam expostas, com a face da cor de seu dono visível para ambos os jogadores. O verso não precisa ficar simultaneamente exposto. Os dois combos, azul e vermelho, permanecem visíveis em todas as cartas, inclusive quando a face correspondente estiver no verso.

No tabuleiro, são usados os símbolos da face atualmente visível. Os símbolos do verso não servem de apoio à conversão nem pontuam enquanto aquela face não estiver voltada para cima.

No digital, a exibição inicial recolhe o verso das cartas nas duas mãos. **Mostrar/Ocultar ícones adversário** permite expandir ou recolher a segunda face de ambas as mãos, sem mudar o estado da partida. O olho amplia a carta e permite consultar a outra face. Esses recursos de consulta não criam novos símbolos ou novas ações de jogo.

## 3. Preparação e escolha da abertura

1. Definam quem controla Azul e Vermelho.
2. Embaralhem as 40 cartas e distribuam quatro para cada jogador. O aplicativo distribui alternadamente, começando por Azul; isso é uma escolha operacional do protótipo.
3. Sorteiem quem fará a primeira jogada. Após uma partida concluída, quem perdeu faz a primeira jogada da próxima. Se houve empate, façam novo sorteio.
4. Revelem as **duas cartas do topo** do monte restante. No playtest, são chamadas de **A** e **B**. A origem das duas cartas não muda o jogo; o topo foi escolhido por simplicidade, no impresso e no digital.
5. **O adversário de quem fará a primeira jogada escolhe qual dessas duas cartas terá sua própria cor.** A outra terá a cor do primeiro jogador. Essa escolha compensa a vantagem de começar.
6. Coloquem A em L2C3 e B em L3C4, nas cores escolhidas. Essas são as posições padrão desta versão.
7. A nova carta do topo do monte passa a ser a carta pública. O jogador definido no sorteio, ou o perdedor da partida anterior, faz a primeira jogada.

**Exemplo:** se Azul fará a primeira jogada, Vermelho escolhe se A ou B ficará vermelha. A outra fica azul. Depois, Azul joga.

Escolher as cores das duas cartas iniciais não conta como jogada e não é uma conversão.

No aplicativo, a cor do humano é escolhida antes do sorteio. Se for a vez do computador escolher a abertura, ele escolhe A/B. Quando a escolha cabe ao humano, a janela sobre o tabuleiro permite alternar A/B e só confirma ao apertar **OK**. A mão do humano continua visível acima do tabuleiro.

## 4. Carta pública e mãos

A carta pública é a carta do topo do monte, disponível ao jogador da vez. Ela pode ser colocada diretamente, na cor de quem joga, ou repor uma carta da mão usada numa colocação normal.

- **Colocar da mão:** a carta pública entra na mão para repor a carta jogada, enquanto houver monte.
- **Colocar a carta pública:** retira-se o topo do monte e a mão permanece igual.
- **Colocar e converter:** usa-se uma carta da mão e não há reposição.
- A carta pública nunca pode ser usada para converter.
- Mão vazia não elimina o jogador: ele continua colocando a carta pública.

As duas representações da carta pública, ao lado das mãos no digital, são a mesma carta física. Cada uma mostra a face da cor daquele jogador; não são duas cartas disponíveis.

Quando a mão do jogador estiver vazia, o aplicativo seleciona automaticamente a carta pública. Ainda é preciso escolher uma casa e confirmar em **OK**.

## 5. Jogada e colocação normal

Os jogadores se alternam. Em cada jogada, coloca-se exatamente uma carta numa casa livre, com a face da cor de quem joga voltada para cima.

Uma colocação normal pode ocupar **qualquer casa livre**. Não há exigência de adjacência para simplesmente colocar.

**Na primeira jogada de cada jogador, somente a colocação normal é permitida. Portanto, não há conversão nem na jogada 1 nem na jogada 2 da partida. A partir da jogada 3, as conversões podem ocorrer, desde que legais.**

Não há descarte, movimento de cartas já colocadas ou conversão isolada sem colocar uma carta nova.

No digital, carta e casa podem ser selecionadas em qualquer ordem e trocadas até a confirmação. **COLOCAR** e **COLOCAR E CONVERTER** selecionam a modalidade. **OK** executa a jogada. Limpar seleção não altera a partida.

## 6. Adjacência

Duas casas são adjacentes quando se tocam por um lado ou por um canto: horizontal, vertical ou diagonal. São as oito direções ao redor de uma casa, respeitando os limites do tabuleiro.

Essa definição vale para apoios de conversão, grupos, cadeias de símbolos e conexões de combos.

## 7. Colocar e converter

A conversão é opcional. Ela vira **uma única carta adversária** para a cor de quem joga. O alvo tem dois símbolos visíveis, X e Y. Todos os requisitos abaixo são obrigatórios:

1. A primeira jogada de cada jogador já terminou: a partida está na jogada 3 ou posterior.
2. A carta nova vem da mão. A carta pública não converte.
3. A casa da carta nova é adjacente ao alvo adversário.
4. **A carta nova mostra um dos símbolos do alvo** (X ou Y). Apoios de outras cartas não dispensam essa coincidência.
5. **Uma carta aliada que já estava no tabuleiro**, adjacente ao alvo, mostra **o outro símbolo**. Se a carta nova mostra os dois símbolos do alvo, basta que a carta antiga mostre qualquer um deles. Uma única carta nunca cobre os dois símbolos sozinha.
6. Portanto, depois de colocar a carta nova, há pelo menos duas cartas aliadas adjacentes ao alvo, incluindo a carta colocada.
7. **Se o alvo pertence a um combo completo ativo antes da jogada, são necessárias três cartas aliadas adjacentes ao alvo, cada uma com ao menos um símbolo em comum com ele.** Entre essas três, continuam valendo os itens 4 e 5: a carta nova cobre um símbolo e uma carta antiga cobre o outro.

A colocação e a conversão são uma única jogada. A mão não recebe reposição. A conversão não se propaga para outras cartas.

Apoios não são gastos nem removidos. Após virar o alvo, seus símbolos e vínculos de combo válidos passam a ser os da nova face. Grupos, cadeias, combos e pontos são recalculados.

**Exemplo proibido:** #03 vermelha, com LEI e ECONOMIA, não pode converter #36 azul, com POLÍTICA e RELAÇÕES. Não existe símbolo em comum entre a carta colocada e o alvo, mesmo que outras cartas cubram os símbolos dele.

**Exemplo em combo:** FAMÍLIA azul (RELAÇÕES + VALORES), peça ativa de Deus, Pátria e Família. Vermelho coloca PROGRESSISMO (VALORES + INDIVÍDUO) numa casa vizinha; COMUNIDADE (RELAÇÕES + POLÍTICA), já vizinha, cobre RELAÇÕES; LAICIDADE (INDIVÍDUO + VALORES), também vizinha, é a terceira carta e tem VALORES. Converte. Com PACIFISMO (SEGURANÇA + POLÍTICA) como terceira carta, não converteria.

Não existe exceção que permita converter apenas por ter um combo. Completar um combo próprio pode ser o resultado da conversão; não substitui seus requisitos.

**Implementação.** O critério mecânico do motor (carta nova com símbolo em comum com o alvo; dois símbolos cobertos por duas cartas aliadas diferentes e adjacentes) é equivalente aos itens 4 a 6 e permanece. No alvo em combo, o motor passa a contar como apoio apenas as cartas aliadas adjacentes que tenham ao menos um símbolo do alvo, e exige três.

**Apresentação no digital.** Na prévia antes do OK, na resolução da jogada e no tutorial, o aplicativo destaca explicitamente a **carta nova** e o símbolo do alvo que ela cobre, e a **carta que já estava no tabuleiro** e o outro símbolo. No alvo em combo, a terceira carta aparece como apoio do combo, com o símbolo do alvo que ela tem destacado. As mensagens de recusa usam a mesma lógica (por exemplo: "A carta nova precisa ter VALORES ou INDIVÍDUO"; "Falta uma carta já no tabuleiro, vizinha do alvo, com INDIVÍDUO"; "Este alvo está num combo: são precisas 3 cartas suas vizinhas com ícones dele").

No digital, COLOCAR E CONVERTER só é habilitado se houver alguma conversão legal com a carta selecionada. Hoje, depois de escolher a casa, os alvos legais aparecem em amarelo; a Bíblia (seção 5.4) prevê a borda já ao selecionar a carta da mão — decisão pendente. Um único alvo é selecionado automaticamente; havendo vários, o jogador escolhe um. OK é sempre a confirmação final.

## 8. Formação e proteção de combos

Um combo está ativo quando suas três cartas específicas estão no tabuleiro, com a face da cor desse combo visível, e formam um conjunto conectado.

As próprias três peças precisam conectar-se entre si, pelas oito direções. Basta existir um caminho entre elas; não é necessário que cada uma toque as outras duas.

**Um combo pode ser completado pela carta recém-colocada ou por uma carta que tenha sido convertida.** Não há diferença de validade entre esses casos. Virar uma carta pode completar um combo da nova cor e desfazer um combo da cor anterior.

O combo completo dá 3 pontos adicionais e protege suas peças: para converter uma delas, são precisas três cartas adversárias adjacentes, todas com algum símbolo da peça (seção 7, item 7). No digital, um contorno grosso da cor do combo marca as três cartas.

### Regra única de conexão

Todo combo é gerado por três cartas conectadas com o mesmo nome de combo e a mesma cor. Não interessa como isso ocorreu: colocação, conversão ou uma combinação das duas. "Mesmo nome" refere-se ao nome do combo indicado no rodapé, não ao título individual de cada carta.

Cartas fora desse trio não substituem nenhuma das peças nem servem de ponte entre peças separadas. A opção anterior de conectividade alternativa foi eliminada do jogo e do laboratório.

## 9. Pontuação

A pontuação considera somente as cartas do tabuleiro e suas faces visíveis. São somadas três parcelas:

### Grupo

Cada grupo conectado de **três ou mais cartas da mesma cor** dá 1 ponto por carta. Grupos com uma ou duas cartas não dão pontos de grupo.

### Símbolo

Para cada símbolo, encontre as cadeias conectadas de **três ou mais cartas da mesma cor** que tenham esse símbolo. Cada carta da cadeia dá 1 ponto naquele símbolo.

Uma carta pode participar integralmente de duas cadeias e pontuar por seus dois símbolos: até 2 pontos de símbolos por carta. Ela não é retirada de uma cadeia por pontuar na outra. Vários caminhos entre as mesmas cartas não duplicam a contagem do mesmo símbolo na mesma carta.

Cartas intermediárias sem o símbolo não conectam uma cadeia daquele símbolo.

### Combo

Cada combo completo ativo dá **3 pontos adicionais**. Esses pontos se somam aos pontos de grupos e símbolos das mesmas cartas.

### Resultado

**Total = pontos de grupos + pontos de símbolos + pontos de combos.** A pontuação é recalculada após cada jogada; não é uma acumulação permanente de pontos ganhos em turnos anteriores. Converter uma carta pode reduzir a pontuação adversária.

No modo jogador, o placar mostra o total de cada jogador e os nomes dos combos completos. O detalhamento por grupo, símbolo e combo e o "Examinar os cálculos" ficam no laboratório. Mostrar ligações é um auxílio visual de leitura; não muda a mecânica.

## 10. Final da partida e revanche

A partida termina assim que as 24 casas estiverem ocupadas. Resolva a última colocação e sua eventual conversão antes de comparar os pontos.

Cartas na mão e no monte não pontuam. Maior total vence; totais iguais resultam em empate. Na próxima partida, o perdedor começa e o adversário escolhe a abertura. Em empate, sorteie novamente quem começa.

## 11. Particularidades do aplicativo

- **Tela inicial:** computador ou dois humanos no mesmo aparelho. Contra o computador, escolha a cor do humano e o nível antes de começar.
- **Iniciante:** avalia pontos imediatos e conexões simples, varia entre alternativas legais e não antecipa respostas adversárias. É o padrão para novas partidas contra o computador. Seu equilíbrio ainda será calibrado por playtests.
- **Experiente:** mantém o desafio anterior; compara respostas adversárias e possibilidades futuras da carta pública. Nenhum nível consulta a ordem real do monte oculto.
- **Escolha automática de A/B:** prioriza combo em comum com a própria mão; depois coincidências de símbolos; depois presença de combo da própria cor. Aplica-se quando o computador é o responsável pela abertura.
- **Orientação:** cartas da sua mão acima do tabuleiro; cartas da mão do adversário abaixo. Contra o computador, a posição do humano permanece fixa. No controle de dois humanos, a referência acompanha quem está decidindo.
- **Visualização:** vinhetas e versos podem ser recolhidos nas miniaturas; ampliação mostra a carta para leitura. Ambos os combos continuam visíveis.
- **Modo jogador e laboratório:** números de carta, códigos de combo e ferramentas de laboratório não aparecem no modo jogador nem no tutorial. A separação em duas interfaces distintas (jogador e teste) está decidida para uma etapa posterior.
- **Desfazer, salvar e carregar:** recursos de playtest; não são novas ações do jogo de mesa. O salvamento automático fica no navegador. Arquivos permitem transportar uma partida e seu histórico.
- **Partidas antigas:** são reproduzidas com as regras históricas. Conversões antigas hoje proibidas (inclusive conversões de peças de combo com terceiro apoio sem símbolo do alvo, válidas até a v9) podem permanecer no histórico e ser refeitas como reprodução; novas jogadas devem respeitar a versão vigente. Partidas iniciadas não têm a abertura refeita automaticamente.
- **Demonstração:** cenário didático preparado, disponível no laboratório. Substitui a partida de teste e não é o começo de uma partida normal.
- **Tutorial (previsto):** partida guiada em tabuleiro 4 × 4, exclusiva do tutorial, com fim em 16 casas. O motor recebe a geometria como configuração; o jogo normal continua 4 × 6 com fim em 24. Roteiro e arquitetura em `CM_Tutorial_Guiado_Arquitetura_v1.md`.
- **Publicação:** não há multiplayer remoto nem envio automático de arquivos de devolutiva. Dois humanos compartilham o mesmo aparelho.

## 12. Limites desta consolidação

O laboratório permite posições alternativas de abertura para investigação. Isso não muda a regra única de combos. Distribuição alternada começando por Azul é uma decisão operacional do protótipo. Animações e sons são propostas de experiência, não requisitos novos de regra.

Este documento não edita os arquivos editoriais sincronizados da Bíblia ou da planilha de produção. Registra em um único lugar as decisões de regras aprovadas para a mesa e para o digital.

## 13. Expansão de 48 cartas (prevista, ainda não ativa)

O impresso será produzido com 48 cartas. O playtest digital continua com 40 até o autor decidir ativar a expansão. Quando isso acontecer, valem estas definições, e nenhuma regra das seções 1 a 12 muda além das contagens.

**Fonte de dados.** A composição de 48 cartas está em `CM_DATA_MERGE_FULL_v3_48.csv` e em `CM_Planilha_Impressao_48_v1.xlsx` (raiz da pasta do projeto). As cartas novas têm os números 41 a 48.

**Contagens com 48 cartas.**
- 48 cartas físicas; embaralham-se as 48 na preparação.
- Cada um dos oito símbolos aparece 12 vezes em cada cor.
- 12 combos azuis e 12 vermelhos, cada um com três cartas específicas.
- O tabuleiro continua com 24 casas. Com o monte maior, os combos completos tendem a ficar um pouco mais raros (Bíblia, seção 2.1).

**As oito cartas novas.**
- 41 REDPILL × FEMINISMO
- 42 RACISMO ESTRUTURAL × POLÍTICAS DE REPARAÇÃO
- 43 HOMOFOBIA × DIREITOS LGBT
- 44 ARMAMENTO CIVIL × CONTROLE DE ARMAS
- 45 CANCELAMENTO × LIBERDADE DE EXPRESSÃO
- 46 EXTRATIVISMO × SUSTENTABILIDADE
- 47 OSTENTAÇÃO × CONSUMO CONSCIENTE
- 48 AGRO É POP × AGRICULTURA FAMILIAR

**Combos que só existem com a expansão.**
- Azul **Cada Um no Seu Lugar:** 41, 42 e 43.
- Azul **Export Brazil:** 18, 46 e 48.
- Vermelho **Inclusão:** 41, 42 e 43.
- Vermelho **Pegada Leve:** 46, 47 e 48.
- Ficam sem combo as duas faces da 44 e da 45 e a face azul da 47.

**Faces canônicas que mudam só no baralho de 48.**
- 34 azul (MERITOCRACIA): símbolos INSTITUIÇÕES + LEI. No baralho de 40, continua ECONOMIA + LEI, para manter o equilíbrio de 10.
- 18 azul (PROSPERIDADE): entra no combo Export Brazil. No baralho de 40, continua sem combo.

**Aplicativo (sugestão operacional).** Carregar o baralho a partir do CSV escolhido, em vez de fixar 40 cartas no código, e oferecer no laboratório a escolha entre 40 e 48. O motor de regras não precisa mudar: os combos são identificados pelo nome no rodapé de cada face, e a regra única de conexão (seção 8) vale para qualquer quantidade de combos.
