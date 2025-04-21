# Tutorial de criação de Voicebank

Este tutorial abrange tanto a gravação quanto a OTO.

Embora você possa usar o que quiser para gravar, será muito, muito mais fácil usar o OREMO. Se você não estiver familiarizado com o uso dele, veja isso como uma oportunidade de aprender. Se você planeja fazer o processamento de amostra, terá que fazê-lo após a gravação.
Download oficial: [OSDN]()
Wine wrapper para macOS: [UTAForum]()
Tradução nativa para o inglês do Mac: [UTAForum]()
(Eu recomendo o wine wrapper, porque a versão nativa do Mac não tem a caixa de comentários.)

Para começar, baixe a última reclist padrão da [página reclist](). Você pode escolher a versão com ou sem o índice. Se não estiver usando o OREMO, a versão sem o índice será muito mais fácil de ler.

Se você estiver usando a lista com o índice:
- A pasta contém um arquivo reclist, um arquivo de comentário OREMO e um arquivo de índice.
- A reclist são os números de 000 a 334.
- O arquivo de comentário OREMO permite que você veja os fonemas ou palavras reais que correspondem a cada número.
- O arquivo de índice é para moresampler referenciar ao gerar o OTO.

Se você estiver usando a lista sem o índice:
- A pasta contém um arquivo reclist e um arquivo de comentário OREMO.
- A reclist contém fonemas arpabet.
- O arquivo de comentário OREMO permite que você veja as palavras que correspondem aos fonemas.
- Nenhum arquivo de índice é necessário, porque moresampler pode ler os nomes dos arquivos como estão.

Configure uma pasta para seu voicebank e copie e cole OREMO-comment.txt (e index.csv, se aplicável) em sua nova pasta. No OREMO, abra a reclist. Defina a pasta de destino para sua nova pasta.

Você pode gravar com ou sem guideBGM. Se você quiser usar o guideBGM, recomendo usar um curto feito para reclistas CVVC, como o CVVChinese BGMs ou o VCCV English BGMs.

Nota para o tradutor: Estas duas linhas a seguir foram escritas para falantes de inglês.

O arquivo de comentários lhe dirá como pronunciar aproximadamente usando palavras e precisamente usando fonemas arpabet. [Este pequeno artigo]() explicará como ler e pronunciar arpabet. Na verdade, é bem simples! Se você já estiver familiarizado com outro sistema fonético como o sistema PaintedCZ ou X-SAMPA, consulte a tabela em [esta página]().
Além das sequências de vogais, cada sequência tem apenas 1 tipo de vogal. Todas as três sílabas rimarão.

Nota para o tradutor: Por favor, escreva uma nova seção aqui sobre como pronunciar corretamente os fonemas ingleses, para pessoas que podem não estar familiarizadas com eles.

Cante as 3 sílabas consecutivamente, como se estivesse gravando VCV. Se em algum momento houver um "q" na fonética (ou um apóstrofo nas palavras), significa uma breve pausa (uma parada glotal).
Para referência, você pode baixar os voicebanks existentes do [diretório voicebank]().

**PARA MULTIPITCH:** A pasta principal do voicebank deve conter um pitch que não tenha sufixos. Todos os outros pitches devem ser colocados em subpastas. Ao gravar, não adicione sufixos aos nomes dos arquivos, ou o Moresampler não conseguirá ler o index.csv durante o OTOing.
**PARA AMOSTRAS EXTRAS:** Quaisquer samples extras que não sejam padrão no ARPAsing devem ser colocados em uma subpasta, para que tenham um arquivo oto.ini separado. Isso permite que o ARPAsing Assistant leia corretamente o arquivo oto.ini principal com apenas entradas OTO padrão do ARPAsing.

Vamos para o OTOing! Basta arrastar e soltar a pasta no moresampler.exe para fazer isso.
Digite 3 para escolher arpasing. Quando solicitado a renomear duplicatas, digite y ou yes. Sempre que houver vários do mesmo difonema, como [s t], isso adicionará um sufixo numérico ao final de cópias adicionais. Isso serve para distinguir cada um do outro, pois eles podem soar diferentes com base no contexto de fonemas próximos na sequência. Você também pode escolher se deseja ou não incluir um sufixo. Não é possível usar caracteres como setas ou kanji, então você terá que usar sufixos como "S" ou "A#3".

Se estiver usando Mac ou Linux, você terá que usar o wine para executar o Moresampler. Abra o terminal na pasta em que o moresampler.exe está e digite "wine moresampler.exe /path/to/voicebank". Se você não conseguir fazer isso, transfira seus arquivos para um computador Windows ou peça ajuda a um amigo com Windows para gerá-lo.

Agora que sua OTO base foi gerada, é hora de refiná-la. Cada entrada da OTO é um difonema, o que significa que há apenas dois fonemas ou dois sons. Em geral, o primeiro é um conector para a nota anterior, enquanto o segundo é o fonema principal para a nota atual. Para OTO, primeiro encontre a seção correspondente ao primeiro fonema, depois encontre a seção para o segundo fonema.

## Primeiro fonema

Isso cobre o deslocamento azul e a sobreposição.

**[-]**
A quantidade de sobreposição realmente não importa para este, porque essas notas sempre vêm no início de uma frase, logo após uma pausa. A única coisa importante é que ele cubra uma área de silêncio.

**[c]**
*Plosivas surdas (p t k)*
Se este for o primeiro fonema na sequência, mova o deslocamento de forma que a sobreposição termine cerca de 15 ms antes do consonante.
Se houver outros fonemas antes deste, mova o deslocamento para onde o anterior terminou. Certifique-se de que você não consegue ouvir o anterior. Coloque a sobreposição cerca de 15 ms antes da consoante.

*Plosivas e africadas sonoras (b d g ch jh)*
Se este for o primeiro fonema na sequência, mova o deslocamento de forma que a sobreposição termine onde a consoante começa.
Se houver outros fonemas antes deste, mova o deslocamento para onde o anterior terminou. Certifique-se de que você não consegue ouvir o anterior. Coloque a sobreposição onde a consoante começa.

*Fricativas, nasais e líquidas (f v th dh s z sh zh hh m n ng l r)*
Mova o deslocamento para onde a consoante começa. Para 'r' em particular, você pode querer consultar a seção de glides para obter ajuda.

*Desliza (y w)*
Essas consoantes podem ser difíceis de ver em uma forma de onda normal. Ao clicar no botão [s], você pode alternar para a visualização do espectrograma, que oferece outra maneira de visualizar o áudio. As áreas brilhantes são as frequências mais altas. Essas consoantes aparecem como uma mudança nas frequências ao longo do tempo.
Mova o deslocamento para onde a consoante começa e, em seguida, coloque a sobreposição onde ela é consistente antes da mudança. A pré-enunciação terminará após a mudança.

**[v]**
Por padrão, a sobreposição para essas amostras deve estar em uma quantidade decentemente alta. Se for absurdamente pequena, movê-la para cerca de 50 ms deve ser bom.
Mova o deslocamento inicial para que a área entre ele e a sobreposição esteja em um nível consistente.

Para ditongos, a sobreposição deve cobrir a área antes das mudanças de vogais.

## Segundo fonema

Para todos os casos, a pré-enunciação deve ser colocada onde o primeiro fonema termina e o segundo fonema começa. Isso também cobre a área rosa, a área branca e o corte azul.

**[c]**
*Paradas (p b t d k g ch jh)*
Deve haver um pequeno pedaço de silêncio ou quase silêncio antes da consoante. Mova o rosa onde o silêncio começa e o corte para onde o silêncio termina. Sim, não estamos incluindo a consoante em si. Isso porque, em um UST, essa nota seria seguida por outra nota que TEM a consoante. Isso permite uma transição suave sem um som consonantal duplo estranho.

*Fricativas (f v th dh s z sh zh hh)*
Cubra toda a consoante com rosa até pouco antes do final. Traga o corte para o mesmo lugar, deixando um pequeno espaço. Sem esse espaço, os reamostradores não conseguirão renderizá-lo. No entanto, não queremos que essas consoantes sejam esticadas.

Se houver silêncio após a consoante, faça com que a área branca seja silêncio.

*Nasais, líquidos e glides (m n ng l r y w)*
Mova o rosa para onde a consoante começa a ficar estável e consistente. Use o corte para remover onde a consoante termina ou desaparece. Essas consoantes são seguras para esticar.

**[v]**
Mova o rosa para onde a vogal começa a ficar estável e consistente. Use o corte para remover onde a vogal desaparece. A área branca será a parte sustentada da nota, o que garante que soará bem.

Para difonemas vogais-vogais, coloque a prelocução no final da mudança de vogal.

Para ditongos, coloque o corte antes das mudanças de vogal.

**[-]**
Cubra tudo com rosa, de modo que tudo em branco seja silêncio.

E assim, seu banco de vozes já está pronto. Envie quaisquer bancos liberados para o diretório. Divirta-se, boa sorte!