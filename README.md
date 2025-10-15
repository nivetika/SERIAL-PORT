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
ORG 00H
MOV DPTR,#4500H
MOV TMOD,#20H
MOV TH1,#0FDH
MOV SCON,#40H
SETB TR1
AGAIN:MOVX A,@DPTR
MOV SBUF,A
WAIT:JNB TI,WAIT
CLR TI
INC DPTR
SJMP AGAIN
END


```

### OUTPUT:


<img width="1501" height="735" alt="image" src="https://github.com/user-attachments/assets/2366cbce-088e-4cd2-8379-b43c3c24a7b4" />



<img width="1159" height="595" alt="Screenshot 2025-10-15 073919" src="https://github.com/user-attachments/assets/776cf053-3e74-4746-80dc-41b2513eeb60" />


### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
