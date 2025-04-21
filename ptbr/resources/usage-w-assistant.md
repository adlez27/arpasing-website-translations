# Tutorial de uso do Voicebank com o ARPAsing Assistant

Este tutorial explicará como usar um voicebank ARPAsing no UTAU, usando o ARPAsing Assistant.
É do seu interesse ter um voicebank totalmente OTO'd, antes de fazer USTs com ele, porque ajustar o tempo das notas dependerá dos valores de preenunciação.

Se você ainda não tem o plugin ARPAsing Assistant, você pode baixá-lo de [aqui](). Descompacte o toolkit e mova a pasta "arpasing-assistant" para a pasta "plugins" onde o UTAU está instalado.
Coloque palavras simples em inglês no UST, selecione as notas e execute o plugin ARPAsing Assistant para convertê-las. Como alternativa, você pode inserir fonemas simples de arpabet na nota, separados por espaços. Se você colocar `/u` no final de uma palavra, a nota será dividida uniformemente para cada difonema, em vez de cada difonema ter comprimentos diferentes.
As notas que você selecionar para conversão DEVEM ter outra nota depois delas. A melhor maneira de garantir isso é colocando uma pausa no final do UST.

Para fazer palavras multissílabas via **entrada de palavras**, você terá que excluir todas as notas, exceto a primeira sílaba, e estender a primeira nota para cobrir o comprimento de todas as notas combinadas. Coloque a palavra inteira na nota e converta normalmente. A partir daí, você terá que colocar as notas de volta no tom correto e corrigir o tempo.
No entanto, fazer palavras multissílabas via **entrada de fonemas** é muito mais simples, pois você pode simplesmente dividir os fonemas em várias notas existentes antes da conversão.

**PARA MULTIPITCH E AMOSTRAS EXTRAS:** Se o voicebank estiver configurado corretamente, ele deve funcionar sem problemas, mas há situações comuns que causam incompatibilidade com o ARPAsing Assistant. A pasta principal do voicebank deve conter um tom sem sufixos, e todos os outros toms devem estar em subpastas. Quaisquer amostras extras não padrão também devem estar em subpastas. O ARPAsing Assistant lê apenas o arquivo oto.ini no nível superior do voicebank, e esse arquivo deve conter apenas entradas OTO padrão do ARPAsing.

Ao converter palavras em notas de difone, o ARPAsing Assistant selecionará a melhor cópia de um difone específico com base no contexto. Por exemplo, se você inserir a palavra "stand", ele escolherá uma nota `[t ae]` de uma amostra "stae" em vez de uma amostra "tae". O contexto de gravações semelhantes a palavras cria uma pronúncia natural. Este é o propósito dos sufixos numéricos, para distinguir um do outro. Não exclua os números.

Embora seja recomendado usar um UST completamente desafinado, você pode ajustar o nível de volume das notas e sinalizadores antes da conversão, e eles serão mantidos. Pitchbends e vibrato ficam bagunçados e alinhados às notas erradas, então é recomendado removê-los completamente primeiro.

Ouça o UST como ele está agora para ter uma ideia de como ele soa e quais seções você precisa consertar. É provável que algumas notas estejam fora do tempo e que haja pronúncias com as quais você não esteja satisfeito.
Encontre as palavras ou sílabas cuja pronúncia não seja a desejada. Se você não estiver familiarizado com Arpabet, pode consultar [este artigo]() ou a [tabela de fonemas]() ao editar.

Vamos consertar o tempo. O problema mais gritante é com palavras multissilábicas. Como elas tiveram que ser combinadas em uma única nota antes da conversão, o tempo não é mais o mesmo que o pretendido. Mantenha pressionado ctrl e arraste as extremidades das notas para alterar os comprimentos sem empurrá-las. Alinhe-as de modo que os CVs principais de cada sílaba comecem na posição pretendida. Corrija os tons enquanto estiver nisso, selecionando todas as notas de uma sílaba e movendo-as para cima/baixo.
Procure frases que comecem com consoantes. (Elas seriam a primeira sílaba depois do que costumava ser uma pausa.) A nota `[- C]` é geralmente muito curta, então segure ctrl e arraste o lado esquerdo para torná-la mais longa dessa forma. Ajuste o comprimento para que comece onde o envelope da próxima nota começa.

A partir daí, você pode passar nota por nota, corrigindo o tempo de todas as notas pequenas, alterando-as para o comprimento do envelope de pré-enunciação da próxima nota. É por isso que você quer que seu banco já esteja totalmente OTO'd. Você provavelmente quer definir seu Quantize para 64 notas.
Conforme você avança, você também pode modificar a pronúncia. Por exemplo, "don't want" se tornará `[d ow][ow n][n t][t w][w aa]` etc., mas são notas demais para um espaço curto, onde na prática essa frase geralmente soa como "don want" ao cantar. Então, remova o `[n t]` e altere o `[t w]` para `[n w]`.

A partir daqui, você pode ajustar normalmente.