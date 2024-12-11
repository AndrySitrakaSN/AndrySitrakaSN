<style>
        #text {
          font-size: 50px;
          font-family: cursive;
          white-space: nowrap;
          display: inline-block;
          padding-right: 5px;
          color: rgb(110, 119, 133);
        }
</style>
<div id="text"></div>  
<h1 align="center">Hi 👋, I'm SOLONIRINA Andry Sitraka</h1>

<img src="https://camo.githubusercontent.com/89a46b75cb2af1de643c4ae5e510aff5c0fa30e7e2a9cdfa5e4ab46eae39a19e/68747470733a2f2f692e696d6775722e636f6d2f315a76566b44632e676966" alt="">
<h3 align="center">💥 Python and AI Developer From Madagascar 💥</h3>
<p align="left"> <img src="https://komarev.com/ghpvc/?username=andrysitrakasn&label=Profile%20views&color=0e75b6&style=flat" alt="andrysitrakasn" /> </p>
<!-- ----------------------------------------------------------------------------------- -->
<script>
        const textElement = document.getElementById('text');
        const message1 = 'SOLONIRNA Andry Sitraka';
        const message2 = 'Coucou tous les mode 😅?';
        function typeWriter(message, callback) {
          let i = 0;
          textElement.innerHTML = ''; // Réinitialise le texte à chaque début de cycle
          function writeChar() {
            if (i < message.length) {
              textElement.innerHTML += message.charAt(i);
              i++;
              setTimeout(writeChar, 100); // délai entre chaque caractère
            } else if (callback) {
              setTimeout(callback, 1000); // Appelle la fonction de callback après une pause
            }
          }
          writeChar(); // Démarre l'écriture
        }
       function eraseText(callback) {
          let i = textElement.innerHTML.length;
          function deleteChar() {
            if (i > 0) {
              textElement.innerHTML = textElement.innerHTML.slice(0, i - 1);
              i--;
              setTimeout(deleteChar, 50); // délai pour effacer chaque caractère
            } else if (callback) {
              callback(); // Appelle la fonction de callback après avoir tout effacé
            }
          }
          deleteChar(); // Démarre l'effacement
        }
        function startAnimation() {
          typeWriter(message1, function() {
            eraseText(function() {
              typeWriter(message2, function() {
                eraseText(function() {
                  startAnimation(); // Redémarre l'animation après tout effacé
                });
              });
            });
          });
        }
    startAnimation(); // Démarre l'animation immédiatement
</script>

