# TCL_practice


### 1 CODE to count letter in given string


set str "LIHAKHDBLICIHJAADFDCSDBBBDFDB"

set l [string length $str]
puts $l

set cnt_A 0
set cnt_B 0
set cnt_C 0
set i 0

while {$i <= $l} {
  
  if { "A" == [string index $str $i] } {
  incr cnt_A
  } elseif {"B" == [string index $str $i]} {
  incr cnt_B
  } elseif {"C" == [string index $str $i]} {
    incr cnt_C
  }
  
  incr i
}

puts "The count of A is $cnt_A \n
The count of B is $cnt_B \n
The count of C is $cnt_C "
      





#### 2 Code to find factorial of number without using built in function without recursion

#### Without Recursion FACTORIAL


proc fact {n} {
  
  set f 1
  
  while {$n >= 2} {
    
    set f [expr {$f * $n} ]
    incr n -1
  }
  
  return $f
}

set value [fact 4]
puts " The factorial value without recursion is $value "


#### 2 Code to find factorial of number without using built in function with recursion

#### With Recursion FACTORIAL

proc refact n {
  
  if {$n <= 1} {
  return 1
    
  }
  
  expr $n * refact [ expr { $n -1 }]]
  
}

puts "The factorial value with recursion is [refact 4] "



