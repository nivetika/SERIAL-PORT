
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

<img width="1501" height="735" alt="Screenshot 2025-10-15 072933" src="https://github.com/user-attachments/assets/8e9645ce-63e9-4fc6-90ea-51c40f43d541" />


### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
