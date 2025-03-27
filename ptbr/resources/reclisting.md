# Tutorial de escrita de reclist ARPAsing

ARPAsing não é um reclist único e estático, mas um método de UTAU em inglês. É semelhante a como VCV não é um reclist único, mas um método de UTAU em japonês. O único critério para um reclist ser um reclist arpasing é a compatibilidade com o auto-OTOer do Moresampler e com o plugin ARPAsing Assistant.

Você pode escrever seu reclist inglês ou addon reclist da maneira que quiser, desde que os fonemas que você incluir correspondam diretamente ao Arpabet. Depois de escrito, você precisará criar um arquivo index.csv para que o Moresampler saiba como fazer OTO nele.
Se você estiver escrevendo um addon reclist, você pode simplesmente adicionar ao index.csv existente para esse reclist. Se você estiver fazendo uma lista do zero, você terá que criar um novo arquivo index. Você pode usar qualquer editor de texto para criar um, mas você também pode usar qualquer editor csv que você goste.

A primeira coluna contém todos os nomes de arquivo, que geralmente são exatamente os mesmos do arquivo reclist que você usaria no OREMO. Você precisa incluir a extensão do arquivo. Se estiver usando um editor de texto, separe esta coluna da próxima coluna com uma vírgula. A segunda coluna tem a versão arpabet dos fonemas para essa linha. Cada fonema deve ser separado por um sublinhado.
Como alternativa, você pode escrever seu reclist diretamente no Arpabet para começar e separar cada fonema com um sublinhado. Isso elimina a necessidade de escrever um index.csv.

Todos os fonemas arpabet são aceitos pelo OTOer automático do Moresampler, exceto estes:
`[em] [en] [eng] [el] [nx] [dx]`

Se você criou um complemento reclist, deve regenerar o OTO para todo o banco, para que as duplicatas possam ser numeradas corretamente.

Para facilitar a gravação, você também pode criar um arquivo de comentário OREMO. Este arquivo é chamado "OREMO-comment.txt" e vai para a pasta de destino do voicebank. A primeira coluna contém todos os nomes de arquivo, correspondendo ao reclist. A extensão do arquivo não é necessária, ela só precisa corresponder ao arquivo reclist. Separe as colunas com uma tabulação. A próxima coluna tem o comentário, que é onde você pode escrever notas, como a forma como a amostra deve ser pronunciada.