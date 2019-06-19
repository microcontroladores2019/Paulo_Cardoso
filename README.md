# Paulo Cardoso

# Motiva��o

Instrumentos de corda desafinam devido a v�rios fatores no dia a dia, criando a necessidade de afina-los de novo. Al�m disso em alguns casos � necess�rio alterar a afina��o.
Isso � poss�vel atrav�s da audi��o com um som de refer�ncia, por�m requer pr�tica. Com isso a proposta �, usando o microfone digital MP45DT02 e a blibioteca de matem�tica CMIS, fazer um afinador digital atrav�s da fft do sinal.

# Documenta��o das Fun��es

MP45DT02_config: configura��o do microfone da comunica��o I2S

fftConfig: configura��o da arquiteruda de DSP utilizada na FFT

Init_LEDS: configura a inicializa��o dos LEDS de GPIO

LEDS_OFF: desliga os LEDS

AudioRecStart: Inicializa a comunica��o I2S para o microfone

AudioRecStop: Desliga a comunica��o I2S, na finaliza��o 

Waiting: fun��o da tarefa de leitura do bot�o

PDM_Filter: fun��o da tarefa de convers�o PDM para PCM

Store_Analyse: fun��o da tarefa de an�lise espectral

# Perif�ricos e configura��o dos pinos

Ser� utilizado nesse projeto o microfone MP45DT02 conectado atrav�s do I2S.

GPIO10 -> Output push-pull speed 50MHz (Conectado ao clock do microfone)

GPIO3 -> Input(Conectado ao Dout do microfone)

PD12,PD13,PD14,PD15 -> Output(LEDS)

PA0 -> Input(BUTTON USER)

# Diagrama de Blocos

<img align="center" src="blocos.PNG" width="500" height="400">

# Fluxograma

<img align="center" src="Fluxograma.PNG" width="500" height="400">
