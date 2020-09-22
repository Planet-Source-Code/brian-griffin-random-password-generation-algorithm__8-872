<div align="center">

## Random Password Generation Algorithm


</div>

### Description

This is a simple algorithm written for PHP4+ (Works with PHP3 with a few modifications) to randomly generate a password composed of 2 lower case characters, 2 upper case characters, and 2 integers.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Brian Griffin](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/brian-griffin.md)
**Level**          |Beginner
**User Rating**    |4.3 (13 globes from 3 users)
**Compatibility**  |PHP 4\.0
**Category**       |[Algorithims](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/algorithims__8-29.md)
**World**          |[PHP](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/php.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/brian-griffin-random-password-generation-algorithm__8-872/archive/master.zip)





### Source Code

```
<?php<br>
/*<br>
 * RANDOM PASSWORD GENERATION ALGORITHM<br>
 * PROGRAMMED BY: BRIAN GRIFFIN<br>
 * January 1, 2003<br>
 * MXrider005@hotmail.com<br>
 *<br>
 * You can use this freely. Just don't credit it as your own work! And please e-mail me if you do just to let me know. Thanks.<br>
 */<br>
 // DEFINE STRINGS TO USE FOR CHARACTER COMBINATIONS IN THE PASSWORD<br>
 $LCase = "abcdefghijklmnopqrstuvwxyz";<br>
 $UCase = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";<br>
 $Integer = "0123456789";<br>
 <p>
 // DEFINE CONSTANTS FOR ALGORTTHM<br>
 define("LEN", "1");<br>
 /* THIS FUNCTION GENERATES A RANDOM NUMBER THAT WILL BE USED TO<br>
  * RANDOMLY SELECT CHARACTERS FROM THE STRINGS ABOVE<br>
  */<br><p>
 function RndInt($Format){<br>
  switch ($Format){<br>
   case "letter":<br>
    $Rnd = rand(0,25);<br>
    if ($Rnd > 25){<br>
     $Rnd = $Rnd - 1;<br>
    }<br>
    break;<br>
   case "number":<br>
    $Rnd = rand(0,9);<br>
    if ($Rnd > 9){<br>
     $Rnd = $Rnd - 1;<br>
    }<br>
    break;<br>
   }<br>
  return $Rnd;<br>
  } // END RndInt() FUNCTION<p>
 /* RUN THE FUNCTION TO GENERATE RANDOM INTEGERS FOR EACH OF THE<br>
  * 6 CHARACTERS IN THE PASSWORD PRODUCED.<br>
  */<br>
 $a = RndInt("letter");<br>
 $b = RndInt("letter");<br>
 $c = RndInt("letter");<br>
 $d = RndInt("letter");<br>
 $e = RndInt("number");<br>
 $f = RndInt("number");<br><p>
 // EXTRACT 6 CHARACTERS RANDOMLY FROM THE DEFINITION STRINGS<br>
 $L1 = substr($LCase, $a, LEN);<br>
 $L2 = substr($LCase, $b, LEN);<br>
 $U1 = substr($UCase, $c, LEN);<br>
 $U2 = substr($UCase, $d, LEN);<br>
 $I1 = substr($Integer, $e, LEN);<br>
 $I2 = substr($Integer, $f, LEN);<br><p>
 // COMBINE THE CHARACTERS AND DISPLAY THE NEW PASSWORD<br>
 $PW = $L1 . $U2 . $I1 . $L2 . $I2 . $U1;<br>
 echo("<center><b>The Password Is:\t$PW</b></center>");<br>
?><br>
```

