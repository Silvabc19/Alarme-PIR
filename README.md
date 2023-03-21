Equipe 06

PAULO HENRIQUE

BRYAN CHRISTYAN

# Introdução 

O projeto a seguir trata-se de um alarme que pode ser utilizado na área residencial ou empresarial, pode ser utilizado não só para segurança antifurto, como para identificar presença em áreas restritas ou lugares ocupados por gases, onde ao se aproximar a pessoa será alertada do perigo.

# Objetivos

-Alertar ao acesso de áreas restritas
-Alerta em caso de invasão domiciliar
-Utilização do sensor de presença para identificação

# Materiais Utilizados

1-	Led Vermelho
1-	Resistor de 1k ohms
1-	Placa Arduino mega 2560
1-	Protoboard
3- Jumpers Branco
1-	Jumper Vermelho
1-	Jumper Preto
1-	Jumper Azul
1-	Jumper Marrom
1-	Jumper Verde

# Circuito

![512454 (1280×720)](https://user-images.githubusercontent.com/127743713/226620087-2e15e678-469c-417a-a05e-1b3dceba6758.jpg)

# Programção

const int PIR = 3;     // pino sinal sensor de presença

const int buzzer = 4;

const int led =  8;      

void setup() {

Serial.begin(9600);

pinMode(led, OUTPUT);

pinMode(buzzer, OUTPUT);

pinMode(PIR, INPUT);

}

void loop() {

// leitura do sensor

int leitura = digitalRead(PIR);

Serial.println(leitura);

delay(500); // delay 500ms para estabilizar sinal de leitura
  
  // verifica se leitura está em nivel alto

if (leitura == HIGH) {

digitalWrite(led, HIGH);

tone(buzzer,1200,500);   

delay(100);

noTone(buzzer);

delay(100);

//Desligando o buzzer.  

} else {

digitalWrite(led, LOW);

noTone(buzzer);

}
}

# Conclusão

Concluimos que o projeto tem grande aproveitamento para o mercado devido o seu baixo custo e a facilidade na montagem e elaboração da tarefa apresentada, onde uma pessoa que desconheça sobre liguagem de programação pode estar desenvolvendo seu proprio alarme seguindo o passo a passo e a programação deixada acima!

