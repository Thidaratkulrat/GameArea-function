# GameArea-function
this.speedX = 0;   this.speedY = 0;   this.x = x;   this.y = y;   this.update = function() {     ctx = myGameArea.context;     ctx.fillStyle = color;     ctx.fillRect(this.x, this.y, this.width, this.height);   }   this.clicked = function() {     var myleft = this.x;     var myright = this.x + (this.width);     var mytop = this.y;     var mybottom = this.y + (this.height);     var clicked = true;     if ((mybottom &lt; myGameArea.y) || (mytop > myGameArea.y) || (myright &lt; myGameArea.x) || (myleft > myGameArea.x)) {       clicked = false;     }     return clicked;   } }  function updateGameArea() {   myGameArea.clear();   if (myGameArea.x &amp;&amp; myGameArea.y) {     if (myUpBtn.clicked()) {       myGamePiece.y -= 1;     }     if (myDownBtn.clicked()) {       myGamePiece.y += 1;     }     if (myLeftBtn.clicked()) {       myGamePiece.x += -1;     }     if (myRightBtn.clicked()) {       myGamePiece.x += 1;     }   }   myUpBtn.update();   myDownBtn.update();
