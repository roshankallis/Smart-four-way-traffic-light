# Smart-four-way-traffic-light
A smart four way traffic signal using arduino 
// 4-Way Traffic Signal using Arduino UNO

// North
#define N_G 2
#define N_Y 3
#define N_R 4

// East
#define E_G 5
#define E_Y 6
#define E_R 7

// South
#define S_G 8
#define S_Y 9
#define S_R 10

// West
#define W_G 11
#define W_Y 12
#define W_R 13

void setup() {
  pinMode(N_G, OUTPUT);
  pinMode(N_Y, OUTPUT);
  pinMode(N_R, OUTPUT);

  pinMode(E_G, OUTPUT);
  pinMode(E_Y, OUTPUT);
  pinMode(E_R, OUTPUT);

  pinMode(S_G, OUTPUT);
  pinMode(S_Y, OUTPUT);
  pinMode(S_R, OUTPUT);

  pinMode(W_G, OUTPUT);
  pinMode(W_Y, OUTPUT);
  pinMode(W_R, OUTPUT);

  // Initially all RED
  allRed();
}

void loop() {

  // NORTH
  digitalWrite(N_R, LOW);
  digitalWrite(N_G, HIGH);
  delay(5000);

  digitalWrite(N_G, LOW);
  digitalWrite(N_Y, HIGH);
  delay(2000);

  digitalWrite(N_Y, LOW);
  digitalWrite(N_R, HIGH);

  // EAST
  digitalWrite(E_R, LOW);
  digitalWrite(E_G, HIGH);
  delay(5000);

  digitalWrite(E_G, LOW);
  digitalWrite(E_Y, HIGH);
  delay(2000);

  digitalWrite(E_Y, LOW);
  digitalWrite(E_R, HIGH);

  // SOUTH
  digitalWrite(S_R, LOW);
  digitalWrite(S_G, HIGH);
  delay(5000);

  digitalWrite(S_G, LOW);
  digitalWrite(S_Y, HIGH);
  delay(2000);

  digitalWrite(S_Y, LOW);
  digitalWrite(S_R, HIGH);

  // WEST
  digitalWrite(W_R, LOW);
  digitalWrite(W_G, HIGH);
  delay(5000);

  digitalWrite(W_G, LOW);
  digitalWrite(W_Y, HIGH);
  delay(2000);

  digitalWrite(W_Y, LOW);
  digitalWrite(W_R, HIGH);
}

void allRed() {
  digitalWrite(N_G, LOW);
  digitalWrite(N_Y, LOW);
  digitalWrite(N_R, HIGH);

  digitalWrite(E_G, LOW);
  digitalWrite(E_Y, LOW);
  digitalWrite(E_R, HIGH);

  digitalWrite(S_G, LOW);
  digitalWrite(S_Y, LOW);
  digitalWrite(S_R, HIGH);

  digitalWrite(W_G, LOW);
  digitalWrite(W_Y, LOW);
  digitalWrite(W_R, HIGH);
}
