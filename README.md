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

graph TD
    A[Início: Leitura do G-Code] --> B[Movimentação Eixos X e Y]
    B --> C{Fim de Curso Atingido?}
    
    C -- SIM --> D[PARADA DE EMERGÊNCIA - Hard Limit]
    D --> D1[Corte de Energia e Travamento Manual]
    
    C -- NÃO --> E{Erro de Lógica ou Hardware?}
    
    E -- SIM --> F[PARADA CONTROLADA]
    F --> F1[1. Soft Limits: Desenho fora da área]
    F --> F2[2. Perda de Passos: Motor travado]
    F --> F3[3. Interrupção: Falha de Água/Tampa]
    
    E -- NÃO --> G[Conclusão do Caminho do Corte]
    G --> B
