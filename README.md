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
|<img width="638" height="429" alt="Screenshot 2025-09-21 194309" src="https://github.com/user-attachments/assets/f6e81a81-bf99-4a0b-bec5-c5499b8d803f" />|<img width="637" height="435" alt="Screenshot 2025-09-21 193103" src="https://github.com/user-attachments/assets/3eb8c879-c380-44eb-9302-7812e5ddf490" />|

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 19 42 49_a4368223](https://github.com/user-attachments/assets/78a88750-2581-41ab-982f-3072dc8a747b)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="637" height="435" alt="Screenshot 2025-09-21 193103" src="https://github.com/user-attachments/assets/d2683294-4c02-429d-a910-a5172ada729d" />


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
|<img width="642" height="427" alt="Screenshot 2025-09-21 194357" src="https://github.com/user-attachments/assets/1f3b5a45-3695-4e98-8d28-ff556ddd070e" />|<img width="641" height="431" alt="Screenshot 2025-09-21 193359" src="https://github.com/user-attachments/assets/d8385165-a02c-4a4d-a09d-ed4f02c7d580" />|

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 19 42 50_c9aa25e2](https://github.com/user-attachments/assets/acb2bff8-426c-49e0-988c-7e97161ccb52)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="641" height="431" alt="Screenshot 2025-09-21 193359" src="https://github.com/user-attachments/assets/637197d6-a36d-4f41-9372-00590ac12903" />



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
|<img width="637" height="428" alt="Screenshot 2025-09-21 194423" src="https://github.com/user-attachments/assets/6b7b340f-b23e-4af6-9b73-0cc0fd169923" />|<img width="638" height="432" alt="Screenshot 2025-09-21 193726" src="https://github.com/user-attachments/assets/cfd1b42e-5e1f-483e-98bb-7f8b33b36eae" />|

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 19 42 49_93047a93](https://github.com/user-attachments/assets/5520ab96-4cc4-48a8-9017-4c92c272e70b)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="638" height="432" alt="Screenshot 2025-09-21 193726" src="https://github.com/user-attachments/assets/1eb5e0c3-2af5-4fba-8061-489e42ef3255" />

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
|<img width="637" height="424" alt="Screenshot 2025-09-21 194453" src="https://github.com/user-attachments/assets/4207dd39-7e6e-4413-b381-3e4a41b69d7c" />|<img width="639" height="429" alt="Screenshot 2025-09-21 193949" src="https://github.com/user-attachments/assets/e83117ae-df8b-47cb-9a71-cefcf08bce5e" />|

#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 19 42 49_258e976c](https://github.com/user-attachments/assets/f8657f42-70b0-4432-ac53-09954dbfb1cd)


---
## OUTPUT FROM MASM SOFTWARE

<img width="639" height="429" alt="Screenshot 2025-09-21 193949" src="https://github.com/user-attachments/assets/e5de323f-5324-46c2-b737-6d749756aa3a" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

