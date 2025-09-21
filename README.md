# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12               24:1204                                                     
          1201:34               68:1205
          1202:12               00:1206
          1203:34               c4:1207                                

#### Manual Calculations




---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="645" height="445" alt="Screenshot 2025-09-01 202246" src="https://github.com/user-attachments/assets/c328d11d-0f7c-485e-8445-61c372490910" />

<img width="633" height="411" alt="Screenshot 2025-09-01 203255" src="https://github.com/user-attachments/assets/6f150890-38be-4ab3-9714-ff6de898be48" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12               24:1204                                                       
          1201:34               68:1205
          1202:12               00:1206
          1203:34               c4:1207                              

#### Manual Calculations


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="632" height="409" alt="Screenshot 2025-09-01 203401" src="https://github.com/user-attachments/assets/ce795537-a7c5-4db1-a37b-8a0aa0e20768" />

<img width="645" height="438" alt="Screenshot 2025-09-01 203043" src="https://github.com/user-attachments/assets/1e95aadb-e1db-440d-97b3-1e4f2f708b1a" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12               24:1204                                                       
          1201:34               68:1205
          1202:12               00:1206
          1203:34               c4:1207                               

#### Manual Calculations


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="620" height="409" alt="Screenshot 2025-09-14 144437" src="https://github.com/user-attachments/assets/f142c6e7-a527-4e09-a0a0-55e7f55dcece" />

<img width="636" height="425" alt="Screenshot 2025-09-01 203932" src="https://github.com/user-attachments/assets/e4dc503e-16f8-45cd-b009-e15a8eec0671" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12               24:1204                                                       
          1201:34               68:1205
          1202:12               00:1206
          1203:34               c4:1207                                

#### Manual Calculations



---
## OUTPUT FROM MASM SOFTWARE

<img width="643" height="413" alt="Screenshot 2025-09-14 145031" src="https://github.com/user-attachments/assets/ed0e11db-7015-43e1-8236-3c02a69ca927" />


<img width="641" height="427" alt="Screenshot 2025-09-01 204330" src="https://github.com/user-attachments/assets/0a4f3429-c969-4929-b24e-2c452c324936" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

