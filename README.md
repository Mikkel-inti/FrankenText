# FrankenText

Dette C-program er lavet i forbindelse med kursus: **62712- Basic C-programmeing**, 
der genererer en random tekst, baseret på bogen Frankenstein.

#### Konstanter

- `MAX_WORD_COUNT`  
  Det højste antal unikke tokens (ord) programmet kan gemme.  
  I dette program, er det sat til **15.000 ord**.

- `MAX_SUCCESSOR_COUNT`  
  Det højste antal successors et ord kan have.
  I dette program, er det sat til **MAX_WORD_COUNT/2**.
### Vigtigste funktioner

- `tokenize_and_fill_succs()`
  - Deler teksten op i tokens 
  - laver en liste over hvilke ord der kan følge efter hinanden (successors).

- `build_start_token_list()`
  - Finder alle tokens der kan starte en sætning:
    - ord der starter med et stort bogstav,
    - ikke slutter på `.`, `!` eller `?`,
    - og har mindst én efterfølger gemt.

- `generate_sentence()`
  - Genererer en random tekst ved først at vælge et startord og derefter fortsætte gennem successors, indtil der et ord, som afslutter sætningen.

- `token_ends_a_sentence()`
  - Returnerer `true`, hvis et ord afslutter en sætning. Ordet skal enten slutte på `.`, `!` eller `?`.

- `random_token_id_that_starts_a_sentence()`
  - Vælger et random ord fra listen over gyldige sætningstartere, der blevet

## How to use eksempel:

- Compile programmet (kan tage lidt tid)

### **Eksempel på udskrift**:
#### **Eksempel 1**:
<img width="639" height="115" alt="image" src="https://github.com/user-attachments/assets/0c475024-bab0-478f-b7d5-c04ba15af8db" />

#### **Eksempel 2**:
<img width="971" height="162" alt="image" src="https://github.com/user-attachments/assets/3826f6cc-faa6-4f1b-bd16-421393639d94" />


