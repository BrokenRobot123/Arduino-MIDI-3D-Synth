#include <MIDI.h>

int noteValue;
int octivePin = A0;
int velocityPin = A1;
int noteOnPin = A2;
int noteOffPin = A3;
int shapePin = A4;

void setup(){
  MIDI.begin();
  Serial.begin(31250);
}

void loop(){
  int octave = map(analogRead(octivePin), 0, 1023, 0, 10);
  int velocity = map(analogRead(velocityPin), 0, 1023, 0, 127);
  switch(octave){
    case 0:
      noteValue = map(analogRead(shapePin), 0, 1023, 0, 11);
      break;
    case 1:
      noteValue = map(analogRead(shapePin), 0, 1023, 12, 23);
      break;
    case 2:
      noteValue = map(analogRead(shapePin), 0, 1023, 24, 35);
      break;
    case 3:
      noteValue = map(analogRead(shapePin), 0, 1023, 36, 47);
      break;
    case 4:
      noteValue = map(analogRead(shapePin), 0, 1023, 48, 59);
      break;
    case 5:
      noteValue = map(analogRead(shapePin), 0, 1023, 60, 71);
      break;
    case 6:
      noteValue = map(analogRead(shapePin), 0, 1023, 72, 83);
      break;
    case 7:
      noteValue = map(analogRead(shapePin), 0, 1023, 84, 95);
      break;
    case 8:
      noteValue = map(analogRead(shapePin), 0, 1023, 96, 107);
      break;
    case 9:
      noteValue = map(analogRead(shapePin), 0, 1023, 108, 119);
      break;
    case 10:
      noteValue = map(analogRead(shapePin), 0, 1023, 120, 127);
      break;
    }
  MIDI.sendNoteOn(noteValue, velocity, 1);
  delay(analogRead(noteOnPin));
  MIDI.sendNoteOff(noteValue, 0, 1);
  delay(analogRead(noteOffPin));
}
      
