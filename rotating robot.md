# HW10
// Motor A
int IN1 = 7;
int IN2 = 8;

// Motor B
int IN3 = 10;
int IN4 = 11;

void stop() {
  // Motor A
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, LOW);

  // Motor B
  digitalWrite(IN3, LOW);
  digitalWrite(IN4, LOW);
}

void forward() {
  // Motor A
  digitalWrite(IN1, HIGH);
  digitalWrite(IN2, LOW);

  // Motor B
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);  
}

void turning() {
  // Motor A
  digitalWrite(IN1, LOW);
  digitalWrite(IN2, LOW);

  // Motor B
  digitalWrite(IN3, HIGH);
  digitalWrite(IN4, LOW);  
}


void setup() {
  pinMode(IN1, OUTPUT);
  pinMode(IN2, OUTPUT);
  pinMode(IN3, OUTPUT);
  pinMode(IN4, OUTPUT);
  stop();
}

void loop() {
  forward();
  delay(4000);
  stop();
  delay(2000);
  turning();
  delay(2000);
  stop();
  delay(2000);
}
