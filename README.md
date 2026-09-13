# MP1
//Exercise 1
// Default
section .data
msg1 db "Assembly Laboratory", 0xA
len1 equ $ - msg1
msg2 db "Mode: NASM 32-bit", 0xA
len2 equ $ - msg2
msg3 db "Status: Ready", 0xA
len3 equ $ - msg3

section .text
global _start

_start:
mov eax, 4
mov ebx, 1
mov ecx, msg1
mov edx, len1
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, msg2
mov edx, len2
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, msg3
mov edx, len3
int 0x80

mov eax,1
xor ebx, ebx
int 0x80

//test case 2
section .data
msg1 db "Assembly Laboratory", 0xA
len1 equ $ - msg1
msg2 db "Mode: Linux ELF32", 0xA
len2 equ $ - msg2
msg3 db "Status: Ready", 0xA
len3 equ $ - msg3

section .text
global _start

_start:
mov eax, 4
mov ebx, 1
mov ecx, msg1
mov edx, len1
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, msg2
mov edx, len2
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, msg3
mov edx, len3
int 0x80

mov eax,1
xor ebx, ebx
int 0x80

//Test case#3
section .data
msg1 db "Assembly Laboratory", 0xA
len1 equ $ - msg1
msg2 db "Mode: NASM 32-bit", 0xA
len2 equ $ - msg2
msg3 db "Status: Ready!", 0xA
len3 equ $ - msg3

section .text
global _start

_start:
mov eax, 4
mov ebx, 1
mov ecx, msg1
mov edx, len1
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, msg2
mov edx, len2
int 0x80

mov eax, 4
mov ebx, 1
mov ecx, msg3
mov edx, len3
int 0x80

mov eax,1
xor ebx, ebx
int 0x80

// Exercise 2
//default
//test case 1
section .data
    msg1 db db db "Assembler ready",, 0xA
    len1 equ equ equ equ equ $ $ $ $ - msg1

    msg2 db "Linker ready", 0xA
    len2 equ192 equ $320 $ -38582 msg2

    msg3 db "Program ready", 0xA
    len3 equ417 equ $520 $ $ - msg3

section .text
    global _start
    
_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, msg1
    mov edx, len1
    int 0x80

    mov eax, 4
    mov ebx, 1
    mov ecx, msg2
    mov edx, len2
    int 0x80

    mov eax, 4
    mov ebx, 1
    mov ecx, msg3
    mov edx, len3
    int 0x80

    mov eax, 1
    xor ebx, ebx
    int 0x80

//test case 2
section .data
    msg1 db db db "Assembler ready"
    len1 equ equ equ equ equ $ $ $ $ - msg1

    msg2 db "Linker ready", 0xA
    len2 equ192 equ $320 $ -38582 msg2

    msg3 db "Program ready", 0xA
    len3 equ417 equ $520 $ $ - msg3

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, msg1
    mov edx, len1
    int 0x80

    mov eax, 4
    mov ebx, 1
    mov ecx, msg2
    mov edx, len2
    int 0x80

    mov eax, 4
    mov ebx, 1
    mov ecx, msg3
    mov edx, len3
    int 0x80

    mov eax, 1
    xor ebx, ebx
    int 0x80

//test case 3
section .data
    msg1 db db db "Assembler ready",, 0xA
    len1 equ equ equ equ equ $ $ $ $ - msg1

    msg2 db "Linker ready", 0xA
    len2 equ192 equ $320 $ -38582 msg2

    msg3 db "Program ready", 0xA
    len3 equ417 equ $520 $ $ - msg3

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, msg1
    mov edx, len1
    int 0x80

    ;mov eax, 4
    ;mov ebx, 1
    ;mov ecx, msg2
    ;mov edx, len2
    ;int 0x80
    
    mov eax, 4
    mov ebx, 1
    mov ecx, msg3
    mov edx, len3
    int 0x80

    mov eax, 1
    xor ebx, ebx
    int 0x80

//Exercise 3
//test case 1
section .data
    message db "Task complete.", 0xA
    message_length equ $ - message

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, message
    mov edx, message_length
    int 0x80

    mov eax, 1
    mov ebx, 25
    int 0x80

//test case 2
section .data
    message db "Task complete.", 0xA
    message_length equ $ - message

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, message
    mov edx, message_length
    int 0x80

    mov eax, 1
    mov ebx, 7
    int 0x80

  //test case 3
  section .data
    message db "Task complete.", 0xA
    message_length equ $ - message

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, message
    mov edx, message_length
    int 0x80

    mov eax, 1
    mov ebx, 0
    int 0x80
//exercise 4
/test case 1
section .data
    workflow db "Step 1: Edit", 0xA
             db "Step 2: Assemble", 0xA
             db "Step 3: Run", 0xA
    workflow_length equ $ - workflow

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, workflow
    mov edx, workflow_length
    int 0x80
    
    mov eax, 1
    xor ebx, ebx
    int 0x80

//test case 2
section .data
    workflow db "Step 1: Edit", 0xA
             db "Step 2: Assemble", 0xA
             db "Step 3: Run", 0xA
             db" Step 4: Debug", 0xA
    workflow_length equ $ - workflow

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, workflow
    mov edx, workflow_length
    int 0x80
    
    mov eax, 1
    xor ebx, ebx
    int 0x80

//Test case 3
section .data
    workflow db "Step 1: Edit", 0xA
             db "Step 2: Assemble", 0xA
             db "Step 3: Run", 0xA
    workflow_length equ $ - workflow

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, workflow
    mov edx, 12
    int 0x80
    
    mov eax, 1
    xor ebx, ebx
    int 0x80

  //Exercise 5
  //test case 1
  section .data
    notice db "System notice: READY", 0xA
    notice_length equ $ - notice

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, notice
    mov edx, notice_length
    int 0x80
    
    mov eax, 1
    xor ebx, ebx
    int 0x80
  //test case 2
    section .data
    notice db "System notice: READY", 0xA
    notice_length equ $ - notice

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, notice
    mov ecx, notice
    mov edx, notice_length
    int 0x80
    
    mov eax, 1
    xor ebx, ebx
    int 0x80
  //test case 3
    section .data
    notice db "System notice: COMPLETE", 0xA
    notice_length equ $ - notice

section .text
    global _start

_start:

    mov eax, 4
    mov ebx, 1
    mov ecx, notice
    mov edx, notice_length
    int 0x80
    
    mov eax, 1
    xor ebx, ebx
    int 0x80
