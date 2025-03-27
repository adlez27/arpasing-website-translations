# Tutorial de uso do Voicebank sem ARPAsing Assistant
Este tutorial explicará como usar um voicebank ARPAsing no UTAU, sem o ARPAsing Assistant.

É do seu interesse ter um voicebank totalmente OTO'd, antes de fazer USTs com ele, porque ajustar o tempo das notas dependerá dos valores de preenunciação.

Se você não estiver usando o plugin, você pode ignorar todos os problemas envolvidos no ajuste do tempo e fonemas incorretos. No entanto, você perde toda a conveniência de ter conversões de base.
Se o seu computador for capaz de usar o ARPAsing Assistant, mas você optar por não usá-lo, você pode abrir o exe como um programa autônomo para procurar conversões de palavra para arpabet. No entanto, se você não puder usá-lo completamente (por exemplo, usuários de Mac), você pode usar [este site]() para encontrar conversões. O dicionário pode não ser tão robusto quanto o incorporado ao plugin, mas depois de se familiarizar com o sistema fonético, você deve ser capaz de transcrever quaisquer palavras faltantes. Se você não estiver familiarizado com o Arpabet, você pode consultar [este artigo]() ou o [gráfico de fonemas]().

Insira a letra em inglês simples no UST como faria normalmente, para referência.
Altere cada nota para o CV principal da sílaba, separando cada fonema com um espaço. Por exemplo, a palavra "cat" é "K AE T" em arpabet, então altere a letra para dizer `[k ae]`. Da mesma forma, "steps" é "S T EH P S", então coloque `[t eh]`.
As outras notas essenciais que precisamos são notas finais de frase. Sempre que houver uma pausa após uma nota, você precisa ter o fonema para silenciar. Como regra geral, se a pausa tiver menos de 1 semínima, altere a pausa inteira. Se a pausa for mais longa, apenas a primeira semínima precisa ser alterada. Para "cat" seria uma nota `[t -]`, e para "steps" seria `[s -]`.

O resto é inserir notas de transição. Esta lista funciona em difonemas, então cada nota da letra tem dois fonemas.
O silêncio conta como um, e é necessário sempre que houver transição entre letras cantadas e pausas. Já cobrimos notas com pausas DEPOIS delas, então vamos considerar notas com pausas antes. Se começar com uma vogal, você pode simplesmente adicionar um hífen. Por exemplo, "eye" `[ay]` se torna `[- ay]`. Se começar com uma consoante ou grupo consonantal, você deve trabalhar de trás para frente a partir da consoante mais interna. Veja "strand" como exemplo. Faça uma nota logo antes de `[r ae]` que tenha `[t r]`. Faça uma nota logo antes de `[t r]` que tenha `[s t]`. Faça uma nota logo antes de `[s t]` que tenha `[- s]`. Isso lhe dá uma transição completa do silêncio, através das consoantes, para o núcleo da sílaba.
Para transições entre sílabas, use este mesmo princípio de transições completas de difonema para difonema.

"encalhado nesta ilha"
`[- s][s t][t r][r ae][ae n][n d][d eh][eh d][d aa][aa n][n dh][dh ih][ih s][s ay][ay l][l eh][eh n][n d][d -]`

A duração das notas de transição depende da prelocução da nota que a segue. No entanto, você pode usar seu julgamento pessoal para torná-las mais longas ou mais curtas.
Se alguma nota em particular soar estranha ou desligada, você pode alternar para usar uma gravação alternativa do mesmo difonema adicionando um sufixo numérico, como mudar `[f ey]` para `[f ey1]` e assim por diante.

A partir daqui, você pode afinar normalmente.