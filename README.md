# sa_sensor_fim_curso
===================================

Código-fonte

int sensor = 7;



void setup() {
  pinMode(sensor, INPUT);
  Serial.begin(9600);
}

void loop() {
 if (digitalRead(sensor) ==HIGH){
  Serial.println("porta aberta");
  delay(1000);

 }else{
  Serial.println("porta fechada");
  delay(1000);
 }

}

=====================================

Informações sobre o tema - Desligamento Automático com sensor de fim de curso. 

Criar um algoritmo para uma máquina de corte a laser desligar automaticamente.
Nossa ideia é utilizar um sensor de fim de curso, enquanto o sensor identificar a linha a ser cortada vai continuar cortando até acabar a linha.
Componentes utilizados:
- * Arduino (Nano ou Uno)
- *Sensores de Fim de Curso
- *Jumper
- *cabo de conexão do arduino

====================================

Fluxograma

**https://cdn.discordapp.com/attachments/1485802925665030186/1501018781689053244/ChatGPT_Image_4_de_mai._de_2026_21_32_23.png?ex=69fb34ed&is=69f9e36d&hm=df9bc6539934e53bfcd2cdf6b2aa5395dc7a245fca9bbf2f5cc7775745d97243&**
