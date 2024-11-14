## Exercici 18:

- __Classes d'equivalencia:__ 0 - 120

- __Valors limit:__ 0, -1, 120, 121, -213, 3424 
    Perquè són els límits, surten per un valor del límit i estan fora del límit.
    Escriu tests per a cadascun dels casos de prova.
- __Casos de prova:__
    - Test 1:
    Entrada: 0
    Resultat esperat: True
    Resultat obtingut: True
    - Test 2:
    Entrada: -1
    Resultat esperat: False
    Resultat obtingut: False
    - Test 3:
    Entrada: 120
    Resultat esperat: True
    Resultat obtingut: True
    - Test 4:
    Entrada: 121
    Resultat esperat: False
    Resultat obtingut: False
    - Test 5:
    Entrada: -213
    Resultat esperat: False
    Resultat obtingut: False
    - Test 6:
    Entrada: 3424
    Resultat esperat: False
    Resultat obtingut: False

## Exercici 19:

- __Classes d'equivalencia:__
    - 50%{0-12}
    - 25%{13-17}
    - 0%{18-64}
    - 30%{65-infinit}
- __Valors limit:__ 0, -1, 12, 13, 17, 18, 64, 65, 435, -45
Son valors limit ja que estan a cada limit de rang i proven a sobrepasarr-lo.
- __Casos de prova:__
    - Test 1:
    Entrada: 0
    Resultat esperat: 50
    Resultat Obtingut: 50
    - Test 2:
    Entrada: -1
    Resultat esperat: Error
    Resultat Obtingut: Error
    - Test 3:
    Entrada: 12
    Resultat esperat: 50
    Resultat Obtingut: 50
    - Test 4:
    Entrada: 13
    Resultat esperat: 25
    Resultat Obtingut: 25
    - Test 5:
    Entrada: 17
    Resultat esperat: 25
    Resultat Obtingut: 25
    - Test 6:
    Entrada: 18
    Resultat esperat: 0
    Resultat Obtingut: 0
    - Test 7:
    Entrada: 64
    Resultat esperat: 0
    Resultat Obtingut: 0
    - Test 8:
    Entrada: 65
    Resultat esperat: 30
    Resultat Obtingut: 30
    - Test 9:
    Entrada: 435
    Resultat esperat: 30
    Resultat Obtingut: 30
    - Test 10:
    Entrada: -45
    Resultat esperat: Error
    Resultat Obtingut: Error