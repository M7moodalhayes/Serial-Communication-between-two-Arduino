# Serial-Communication-between-two-Arduino
![Screenshot 2023-07-25 200954](https://github.com/M7moodalhayes/Serial-Communication-between-two-Arduino/assets/79692306/df182b1b-3db8-4d88-94bf-ab6fb7ff8d1c)

Code for Sender Arduino

char mystr[5] = "Hello"; //String data

void setup() {
  // Begin the Serial at 9600 Baud
  Serial.begin(9600);
}

void loop() {
  Serial.write(mystr,5); //Write the serial data
  delay(1000);
}

Code for Receiver Arduino

char mystr[10]; //Initialized variable to store recieved data

void setup() {
  // Begin the Serial at 9600 Baud
  Serial.begin(9600);
}

void loop() {
  Serial.readBytes(mystr,5); //Read the serial data and store in var
  Serial.println(mystr); //Print data on Serial Monitor
  delay(1000);
}
