# Conversão de VCCV para ARPAsing

A lista de recados em inglês do VCCV do PaintedCZ é popular na comunidade UTAU no exterior, com uma abundância de bancos de voz e USTs disponíveis nesse formato. Esses bancos de voz e USTs também podem ser convertidos para o padrão ARPAsing.

## Convertendo bancos de voz

A estrutura organizacional original dos bancos de voz VCCV divide amostras entre várias subpastas chamadas "CC-", "CV_CVC" e assim por diante. As amostras de áudio devem primeiro ser retiradas das subpastas e colocadas na pasta principal do banco de voz. Baixe o arquivo de índice [aqui]() e renomeie-o para "index.csv", depois adicione-o à pasta.
Agora você pode arrastar e soltar a pasta no Moresampler para geração de OTO. No entanto, **não renomeie/numere duplicatas**. Haverá centenas de duplicatas, o que fará com que o ARPAsing Assistant não funcione corretamente. Baixe [esta ferramenta]() para excluir as duplicatas do OTO gerado. O máximo recomendado é entre 10-20.

## Convertendo USTs

Baixe [este plugin](), descompacte e coloque-o na pasta de plugins onde o UTAU está instalado. Usar este plugin em um UST irá convertê-lo de fonemas CZ para fonemas arpabet. No entanto, isso não o tornará perfeitamente compatível com um banco de vozes arpasing imediatamente. (Por exemplo, algumas notas podem ter mais de 2 fonemas.) Faça ajustes para se adequar ao banco.
Plugin original por ChieP
Conversor inspirado por Ivory @TheIvoryShield
Modificações de plugin por KLAD