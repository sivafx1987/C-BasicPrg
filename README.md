<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
 <meta charset="utf-8" />
 <title></title>
 
 <style>
#button {
    width: 6em;
    border: 2px solid green;
    background: #ffe;
    border-radius: 5px;
}
a {
    display: block;
    width: 100%;
    line-height: 2em;
    text-align: center;
    text-decoration: none;
    border-radius: 5px;
}
a:hover {
    color: red;
    background: #eff;
}
</style>

<script type="text/javascript">
 window.onload = function() {
    document.getElementById('Easy').style.display = 'none';
    document.getElementById('Hard').style.display = 'none';
}
function yesnoCheck() {
    if (document.getElementById('yesCheck').checked) {
        document.getElementById('Easy').style.display = 'block';
        document.getElementById('Hard').style.display = 'none';
       
       
    } 
    else if(document.getElementById('yesCheck1').checked) {
        document.getElementById('Hard').style.display = 'block';
        document.getElementById('Easy').style.display = 'none';
       
   }
}

</script>

</head>
<body>

<center>
SELECT GAME TYPE:<br>
EASY:
<input type="radio" onclick="javascript:yesnoCheck();" name="yesno" id="yesCheck"/>Hard:
<input type="radio" onclick="javascript:yesnoCheck();" name="yesno" id="yesCheck1"/>
<br>
<div id="Easy">
<form name=Easymove>
<table border=2 cellpadding=2 cellspacing=2>
<tr>
<td colspan=4 align=center>Game Demo</td>
</tr> 
<SCRIPT LANGUAGE="javascript">
    bx = 3; by = 3;
    for (y = 0; y < 4; y++) {
        document.write('<tr>');
        for (x = 0; x < 4; x++) {
            document.write('<td><tt><input type=button value="   " ');
            document.write('onclick="move(' + x + ',' + y + ');"></tt></td>');
        }
        document.write('</tr>');
        }
   
    function move(x, y) {
        ax = Math.abs(bx - x);
        ay = Math.abs(by - y);
        if (((ax * ay) == 0) && ((ax + ay) == 1)) {
            f = document.Easymove;
            f.elements[4 * by + bx].value = f.elements[4 * y + x].value;
            f.elements[4 * y + x].value = "   ";
            bx = x; by = y;
            f.msg.value++;

            if (document.Easymove.elements[0].value == "A" && document.Easymove.elements[1].value == "B" && document.Easymove.elements[2].value == "C"
                && document.Easymove.elements[3].value == "D" && document.Easymove.elements[4].value == "E" && document.Easymove.elements[5].value == "F"
               && document.Easymove.elements[6].value == "G" && document.Easymove.elements[7].value == "H" && document.Easymove.elements[8].value == "I"
                && document.Easymove.elements[9].value == "J" && document.Easymove.elements[10].value == "K" && document.Easymove.elements[11].value == "L"
                && document.Easymove.elements[12].value == "M" && document.Easymove.elements[13].value == "N" && document.Easymove.elements[14].value == "O" )
             {
                alert("Game finished Sucessfully");
            
            }
        }
    }
    function rndize() {
        alpha = "ABCDEFGHIJKLMNO ";
        for (i = 0; i < 16; i++) {
            x = 0;
            y = 0;
            while (document.Easymove.elements[4 * y + x].value != "   ") {
                x = Math.floor(Math.random() * 4);
                y = Math.floor(Math.random() * 4);
            }
            document.Easymove.elements[4 * y + x].value = alpha.substring(i, i + 1);
        }
        bx = x;
        by = y;  
 }
    rndize();
</script>
 
<tr>
<td colspan=4 align=center>Your Move Count:<input type=text size=20 name=msg></td>
</tr>

<div id="button">Easy</a></div>

</table>
</form>
</div>

<div id="Hard">
<form name=pad>
<table border=2 cellpadding=2 cellspacing=2>
<tr>
<td colspan=5 align=center>Game Demo</td>
</tr> 


<SCRIPT LANGUAGE="JavaScript">
 bx = 4; by = 4;
    for (y = 0; y < 5; y++) {
        document.write('<tr>');
        for (x = 0; x < 5; x++) {
            document.write('<td><tt><input type=button value="   " ');
            document.write('onclick="movex(' + x + ',' + y + ');"></tt></td>');
        }
        document.write('</tr>');
        }
    function movex(x, y) {
        ax = Math.abs(bx - x);
        ay = Math.abs(by - y);
        if (((ax * ay) == 0) && ((ax + ay) == 1)) {
            f = document.pad;
            f.elements[5 * by + bx].value = f.elements[5 * y + x].value;
            f.elements[5 * y + x].value = "   ";
            bx = x; by = y;
            f.msgeasy.value++;

            if (document.pad.elements[0].value == "A" && document.pad.elements[1].value == "B" && document.pad.elements[2].value == "C"
                && document.pad.elements[3].value == "D" && document.pad.elements[4].value == "E" && document.pad.elements[5].value == "F"
               && document.pad.elements[6].value == "G" && document.pad.elements[7].value == "H" && document.pad.elements[8].value == "I"
                && document.pad.elements[9].value == "J" && document.pad.elements[10].value == "K" && document.pad.elements[11].value == "L"
                && document.pad.elements[12].value == "M" && document.pad.elements[13].value == "N" && document.pad.elements[14].value == "O"
               && document.pad.elements[15].value == "P" && document.pad.elements[16].value == "Q" && document.pad.elements[17].value == "R"
                && document.pad.elements[18].value == "S" && document.pad.elements[19].value == "T" && document.pad.elements[20].value == "U"
                && document.pad.elements[21].value == "V" && document.pad.elements[22].value == "W" && document.pad.elements[23].value == "X" )
                           
            {
                alert("Game finished Sucessfully");
              //  rndize();
                
               // break
            }
        }
    }
    function rndizehard() {
        alpha = "ABCDEFGHIJKLMNOPQRSTUVWX ";
        for (i = 0; i < 25; i++) {
            x = 0;
            y = 0;
            while (document.pad.elements[5 * y + x].value != "   ") {
                x = Math.floor(Math.random() * 5);
                y = Math.floor(Math.random() * 5);
            }
            document.pad.elements[5 * y + x].value = alpha.substring(i, i + 1);
        }
        bx = x;
        by = y;
        

    }
    rndizehard();
    
    
</script>
 
<tr>
<td colspan=4 align=center>Your Move Count:<input type=text size=20 name=msgeasy></td>
</tr>

<div id="button"><a href="login.html">Hard</a></div>

</table>
</form>
</div>


</center>

</body>
</html>
