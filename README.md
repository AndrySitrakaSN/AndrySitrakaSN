
<style>
        body {font-family: 'Arial', sans-serif; background-color: #f4f7fc; margin: 0; padding: 0; color: #333;}
        #text {font-size: 50px; font-family: cursive; white-space: nowrap; display: inline-block; padding-right: 5px; color: rgb(110, 119, 133);}
        h1, h3 {text-align: center; color: #444;}
        img {display: block; margin: 0 auto; max-width: 100%; height: auto; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);}
        .container {max-width: 800px; margin: 20px auto; padding: 20px; background-color: #fff; border-radius: 10px; box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);}
        .profile-stats {text-align: center; margin-top: 20px;}
        @media (max-width: 600px) {#text {font-size: 40px;} h1 {font-size: 1.5em;} h3 {font-size: 1.2em;}}
    </style>


<div class="container">
        <h1>Hi 👋, I'm <span id="text"></span></h1>
        <img src="https://camo.githubusercontent.com/89a46b75cb2af1de643c4ae5e510aff5c0fa30e7e2a9cdfa5e4ab46eae39a19e/68747470733a2f2f692e696d6775722e636f6d2f315a76566b44632e676966" alt="Photo de profil">
        <h3>💥 Python and AI Developer From Madagascar 💥</h3>
        <div class="profile-stats">
            <p><img src="https://komarev.com/ghpvc/?username=andrysitrakasn&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views"></p>
        </div>
    </div>
    <script>
        const textElement = document.getElementById('text');
        const message1 = 'SOLONIRINA Andry Sitraka';
        const message2 = 'Coucou tous les mode 😅?';
        function typeWriter(message, callback) {
            let i = 0;
            textElement.innerHTML = '';
            function writeChar() {
                if (i < message.length) {
                    textElement.innerHTML += message.charAt(i);
                    i++;
                    setTimeout(writeChar, 100);
                } else if (callback) {
                    setTimeout(callback, 1000);
                }
            }
            writeChar();
        }
        function eraseText(callback) {
            let i = textElement.innerHTML.length;
            function deleteChar() {
                if (i > 0) {
                    textElement.innerHTML = textElement.innerHTML.slice(0, i - 1);
                    i--;
                    setTimeout(deleteChar, 50);
                } else if (callback) {
                    callback();
                }
            }
            deleteChar();
        }
        function startAnimation() {
            typeWriter(message1, function() {
                eraseText(function() {
                    typeWriter(message2, function() {
                        eraseText(function() {
                            startAnimation();
                        });
                    });
                });
            });
        }
        startAnimation();
</script>

