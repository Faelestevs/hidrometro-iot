// Configurações
const int PINO_SENSOR = 2;
const float FATOR_CALIBRACAO = 7.5;

// Variáveis
volatile int pulsos_contador = 0;
unsigned long tempo_anterior = 0;

// Função de interrução
void contarPulsos() {
  pulsos_contador++;
}

void setup() {
  Serial.begin(9600);
  pinMode(PINO_SENSOR, INPUT);
  digitalWrite(PINO_SENSOR, HIGH);
  attachInterrupt(digitalPinToInterrupt(PINO_SENSOR), contarPulsos, RISING);
  tempo_anterior = millis();
}

void loop() {
  // Verifica se já passou 1 segundo (1000 ms)
  if ((millis() - tempo_anterior) > 1000) {
    
    // Desliga a interrupção para fazer a conta
    detachInterrupt(digitalPinToInterrupt(PINO_SENSOR));

    // Calcula a vazão (L/min)
    float vazao_atual = pulsos_contador / FATOR_CALIBRACAO;

    // Envia APENAS a vazão para o Node-RED
    Serial.print("{\"vazao\": ");
    Serial.print(vazao_atual);
    Serial.println("}");

    // Zera o contador e atualiza o tempo
    pulsos_contador = 0;
    tempo_anterior = millis();

    // Liga a interrupção de volta
    attachInterrupt(digitalPinToInterrupt(PINO_SENSOR), contarPulsos, RISING);
  }
}
