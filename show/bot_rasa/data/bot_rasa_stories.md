## happy path               <!-- name of the story - just for debugging -->
* greet
  - utter_greet
* affirm
  - utter_direct
* affirm
  - utter_channel
* affirm
  - utter_channel_created
* deny
  - utter_ask_sell
* affirm
  - utter_call_sell

## bad path 1
* greet
  - utter_greet
* deny
  - utter_bye

## bad path 2
* greet
  - utter_greet
* affirm
  - utter_direct
* deny
  - utter_bye

## bad path 3
* greet
  - utter_greet
* affirm
  - utter_direct
* affirm
  - utter_channel
* deny
  - utter_bye

## bad path 4
* greet
  - utter_greet
* affirm
  - utter_direct
* affirm
  - utter_channel
* affirm
  - utter_channel_created
* deny
  - utter_bye

## bad path 5
* greet
  - utter_greet
* affirm
  - utter_direct
* affirm
  - utter_channel
* affirm
  - utter_channel_created
* affirm
  - utter_explain
* affirm
  - utter_bye

## bad path 6
* greet
  - utter_greet
* affirm
  - utter_direct
* affirm
  - utter_channel
* affirm
  - utter_channel_created
* deny
  - utter_ask_sell
* deny
  - utter_bye
