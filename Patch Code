 Common code / codigo comun

 cmp byte ptr [00BCC1B1], 05   ; Compare the byte value at memory address 00BCC1B1 with 5 / compara el multiplicador con 05 valor maximo
jnl 005E58B9           ; Jump to address 005E58B9 if the comparison is not less (jump if not less) / salta a la direccion 005E58B9 si la comparacion es no menor

Instructions between / mas instrucciones en medio

cmp byte ptr [00BCC1B1], 01   ; Compare the byte value at memory address 00BCC1B1 with 1 / compara el multiplicador con 01, valor minimo valido
jle 005E58B9     ;  jumps if comparison is less / salta si la comparacion da menor

005E58B9 = call 0060CCB0 ; llama a una funcion

0060CCB0 = Corrective function / funcion correctora

******************************************************************************

 Original code / codigo original
Corrective function
mov al,[sh3.exe+6CE6721] ;moves random address value to AL register / moves un valor en memoria random al registro AL


******************************************************************************

Modified code / codigo modificado
Corrective function
code:
  mov al,[sh3.exe+6CE6721] ; preserves original instruction just in case it's important for other game function / mantenemos el codigo original en caso de que sea necesario para otra funcion del juego
  mov [sh3.exe+7CC1B1], 1 ;resets multiplier to 1 / resetear multiplicador a 1
  jmp return

