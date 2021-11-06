# Diamond-Lang
This is an interpreter for my own programming language


## Hello World:
  set 0:72
  set 1:101
  set 2:108
  set 3:111
  set 4:32
  set 5:87
  set 6:114
  set 7:100

  call out(0, 1, 2, 2, 3, 4, 5, 3, 6, 2, 7)
  call sleep(0)


## Instructions:
	set <arg1>:<arg2>             ; Sets integer at <arg1> to <arg2>
	call <arg1>(<arg2...>)        ; calls method <arg1> with arguments <arg2...>
	extrn <arg>                   ; runs cmd command <arg>
	#<arg>                        ; creates label <arg>
	jump <arg>                    ; jumps to label <arg>
	jmpif <arg>                   ; if boolean-register is true, it'll jump to label <arg>
	jmpifn <arg>                  ; if boolean-register is false, it'll jump to label <arg>
  
  
## Methods:
  	out(<args...>)                ; outputs arg. If it has multiple arguments, they will be outputted as characters
  	outln(<arg>)                  ; outputs arg with new line
  	sleep(<arg>)                  ; if arg is 0, it'll wait until user presses key, else it will wait for arg seconds
	add(<arg1>, <arg2>)           ; adds arg-2 to arg-1
	sub(<arg1>, <arg2>)           ; subtracts arg-2 from arg-1
	multi(<arg1>, <arg2>)         ; multiplies arg-1 with arg-2
	devide(<arg1>, <arg2>)        ; devides arg-1 by arg-2
	mod(<arg1>, <arg2>)           ; devides arg-1 by arg-2 and sets arg-1 to it's remainder
	pow(<arg1>, <arg2>)           ; sets arg-1 to it's power of arg-2
	inc(<arg>)                    ; increases arg by 1
	dec(<arg>)                    ; decreases arg by 1
  
## Arguments in methods:
  If you have a simple integer as argument, it will represent the value of the integer at this location.
  
  Example:
  
  	set 5:12
	call outln(5)
  
  This won't ouput 5, but 12.
  
  If you set a * in front of your argument, it will represent the value at the value of the integer at this location.
  
  Example:
  
    set 0:3
    set 3:102
    call outln(*0)
  
  This will output 102.
  
  With a % in front of the number, it will be the simple number.
 
 Example:
 
    call outln(%143)
  
  This will ouput 143.
