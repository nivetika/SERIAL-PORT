
# Serial Transfer of Single Byte / Character using 8051 (Keil)

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character

```
ORG 00H
MOV TMOD,#20H
MOV TH1,#0FDH
MOV SCON,#40H
SETB TR1
MOV SBUF ,#'B'
WAIT:JNB TI,WAIT
CLR TI
END

```
### (ii) Serial Port to Transfer a Message

```



```

### OUTPUT:

<img width="577" height="314" alt="image" src="https://github.com/user-attachments/assets/00faab0a-5bc5-42db-8b0f-ae3cb75d8e64" />



### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
