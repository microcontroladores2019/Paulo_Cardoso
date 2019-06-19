# Paulo Cardoso

# Motivação

Instrumentos de corda desafinam devido a vários fatores no dia a dia, criando a necessidade de afina-los de novo. Além disso em alguns casos é necessário alterar a afinação.
Isso é possível através da audição com um som de referência, porém requer prática. Com isso a proposta é, usando o microfone digital MP45DT02 e a blibioteca de matemática CMIS, fazer um afinador digital através da fft do sinal.

# Documentação das Funções

MP45DT02_config: configuração do microfone da comunicação I2S

fftConfig: configuração da arquiteruda de DSP utilizada na FFT

Init_LEDS: configura a inicialização dos LEDS de GPIO

LEDS_OFF: desliga os LEDS

AudioRecStart: Inicializa a comunicação I2S para o microfone

AudioRecStop: Desliga a comunicação I2S, na finalização 

Waiting: função da tarefa de leitura do botão

PDM_Filter: função da tarefa de conversão PDM para PCM

Store_Analyse: função da tarefa de análise espectral

# Periféricos e configuração dos pinos

Será utilizado nesse projeto o microfone MP45DT02 conectado através do I2S.

GPIO10 -> Output push-pull speed 50MHz (Conectado ao clock do microfone)

GPIO3 -> Input(Conectado ao Dout do microfone)

PD12,PD13,PD14,PD15 -> Output(LEDS)

PA0 -> Input(BUTTON USER)

# Diagrama de Blocos

<img align="center" src="blocos.PNG" width="500" height="400">

# Fluxograma

<img align="center" src="Fluxograma.PNG" width="500" height="400">
