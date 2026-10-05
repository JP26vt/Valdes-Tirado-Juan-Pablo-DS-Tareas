/*
  Práctica: Monitor de humedad del suelo
  Desarrollo Sustentable (ACD-0908) - Unidad 2: Escenario natural
  Tecnológico Nacional de México, campus Mazatlán
  Placa: Arduino UNO R4 WiFi (compatible también con Uno R3)

  Conexiones:
    Sensor VCC -> 5V
    Sensor GND -> GND
    Sensor SIG -> A0
*/

const int PIN_SENSOR = A0;   // Señal del sensor
const int PIN_LED    = 13;   // LED integrado (alerta de riego)

// ===== CALIBRACIÓN (ajustar con el sensor real) =====
// 1. Deja el sensor al aire o en tierra seca y anota la lectura -> VALOR_SECO
// 2. Mételo en tierra muy mojada o en agua y anota la lectura   -> VALOR_MOJADO
const int VALOR_SECO   = 1020;
const int VALOR_MOJADO = 400;

// Porcentaje mínimo de humedad para considerar la tierra húmeda
const int UMBRAL_PORCENTAJE = 40;

void setup() {
  Serial.begin(9600);
  while (!Serial && millis() < 3000);  // Espera hasta 3 s a que abra el Monitor Serie

  // Solo existe en placas ARM como el UNO R4. En el Uno R3 ya lee de 0 a 1023.
  #if defined(ARDUINO_ARCH_RENESAS)
    analogReadResolution(10);          // Lecturas de 0 a 1023
  #endif

  pinMode(PIN_LED, OUTPUT);

  Serial.println("=== Monitor de humedad del suelo ===");
}

void loop() {
  int lectura = analogRead(PIN_SENSOR);

  int porcentaje = map(lectura, VALOR_SECO, VALOR_MOJADO, 0, 100);
  porcentaje = constrain(porcentaje, 0, 100);

  Serial.print("Lectura: ");
  Serial.print(lectura);
  Serial.print("  |  Humedad: ");
  Serial.print(porcentaje);
  Serial.print("%  |  Estado: ");

  if (porcentaje < UMBRAL_PORCENTAJE) {
    Serial.println("TIERRA SECA -> Se recomienda regar");
    digitalWrite(PIN_LED, HIGH);   // Alerta encendida
  } else {
    Serial.println("TIERRA HUMEDA -> No necesita riego");
    digitalWrite(PIN_LED, LOW);    // Alerta apagada
  }

  delay(1000);  // Una lectura por segundo
}
