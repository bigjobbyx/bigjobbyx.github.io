---
layout: null
permalink: /staff/
---

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="robots" content="noindex, nofollow">
    <title>Password Protected Page</title>
    <style>
        html, body {
            margin: 0;
            width: 100%;
            height: 100%;
            font-family: Arial, Helvetica, sans-serif;
        }
        #dialogText {
            color: white;
            background-color: #333333;
        }
        
        #dialogWrap {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: table;
            background-color: #EEEEEE;
        }
        
        #dialogWrapCell {
            display: table-cell;
            text-align: center;
            vertical-align: middle;
        }
        
        #mainDialog {
            max-width: 400px;
            margin: 5px;
            border: solid #AAAAAA 1px;
            border-radius: 10px;
            box-shadow: 3px 3px 5px 3px #AAAAAA;
            margin-left: auto;
            margin-right: auto;
            background-color: #FFFFFF;
            overflow: hidden;
            text-align: left;
        }
        #mainDialog > * {
            padding: 10px 30px;
        }
        #passArea {
            padding: 20px 30px;
            background-color: white;
        }
        #passArea > * {
            margin: 5px auto;
        }
        #pass {
            width: 100%;
            height: 40px;
            font-size: 30px;
        }
        
        #messageWrapper {
            float: left;
            vertical-align: middle;
            line-height: 30px;
        }
        
        .notifyText {
            display: none;
        }
        
        #invalidPass {
            color: red;
        }
        
        #success {
            color: green;
        }
        
        #submitPass {
            font-size: 20px;
            border-radius: 5px;
            background-color: #E7E7E7;
            border: solid gray 1px;
            float: right;
            cursor: pointer;
        }
        #contentFrame {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        #attribution {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            text-align: center;
            padding: 10px;
            font-weight: bold;
            font-size: 0.8em;
        }
        #attribution, #attribution a {
            color: #999;
        }
        .error {
            display: none;
            color: red;
        }
    </style>
  </head>
  <body>
    <iframe id="contentFrame" frameBorder="0" allowfullscreen></iframe>
    <div id="dialogWrap">
        <div id="dialogWrapCell">
            <div id="mainDialog">
                <div id="dialogText">This page is password protected.</div>
                <div id="passArea">
                    <p id="passwordPrompt">Password</p>
                    <input id="pass" type="password" name="pass" autofocus>
                    <div>
                        <span id="messageWrapper">
                            <span id="invalidPass" class="error">Sorry, please try again.</span>
                            <span id="trycatcherror" class="error">Sorry, something went wrong.</span>
                            <span id="success" class="notifyText">Success!</span>
                            &nbsp;
                        </span>
                        <button id="submitPass" type="button">Submit</button>
                        <div style="clear: both;"></div>
                    </div>
                </div>
                <div id="securecontext" class="error">
                    <p>
                        Sorry, but password protection only works over a secure connection. Please load this page via HTTPS.
                    </p>
                </div>
                <div id="nocrypto" class="error">
                    <p>
                        Your web browser appears to be outdated. Please visit this page using a modern browser.
                    </p>
                </div>
            </div>
        </div>
    </div>
    <div id="attribution">
        Protected by <a href="https://www.maxlaumeister.com/pagecrypt/">PageCrypt</a>
    </div>
    <script>
    (function() {

        var pl = "JVJk15/VDAfskwMFO83U19PdYs+6tjiKtUGe+ghzh5H3FrYyoQXJicjGAe7jZFUSC+TKwKaVVTbfXoC2hle/0NQMHpmjloibNEb8zSGkvYj6QqXIbDdON7FLjhCQ3lStKjnPirgm2tlJVQg4amp3K91IxMT7heFHgDNEnSiqfs//qvt9ljNgPAOCZvK9aw21q8QkP/0tzcLoTVKYlIKHnJa02PO3O+2SY29cuhP8dTgVleOvzYq1NL18cWDu6oDdQQv/FIpn7xEEgPQAfL6vCk+zOpDNmDPwqMsJY2L48uY85pONQmuNdZ2RaR0ub0b1nVHed4nrpb/WGAcy+6POjCn2WTky4ENpr1Im1623dWzQgNwQxbjNF3rQE83RrOhBMXVoMlf6+xmwraH/tV0Oly0jtD5gKwxNtb8/KhFGOwBjOFpGN7G6KtaHAf2Hk0OdX82PWeejcas4Z5ar2t7wz7aOoqiP3SdyhinqZ/oaE9Y7RpoOFUJjhbKtqJky+nfmWCFz50kMduLcqqr5smkKQGVjsmTWuJjo3n+Z8kiHYmxCXFySgpscXaVF8b9xU7hRE8bfXFAamMfg39gxThdSvnzRBLvaxT3Q3vmeomIeeDjO6S3aBTV0MmhB7KRVa2TJaIU2lIeuurESEs9x4QZkAeDNy9sf2HF+jzXCbopmotx7tu56wjT++Kt8hjSe8wbTtXJQ5VNsofUwYxiDI160Wzcei0bJQE5dEFhpHVZOQbP5U4aSHuB1kq3RDVNAwLMmB6zgVjFKA2xFWbDHbbJRzAD021SZq2pMnOnjnOX1c6hPXFgxgIL9P/cFjvlRNj3k42Fof7czd9M6MfPllDlLXeIeXvBvtyGfMlNp/30hVL1V/lEM4rNzqSrjYrHq70dFwZwPHzy9PIoqDIDb0K37DrnnT5nNgg23KpLmM1I9/pXGH1euFydDLwnv9beCa1JD9UamycsRn+m5brkaY/IBb+AVaHRNxWxcI6j9b0jKiF6PVn97ssJ6KKcd7Ca/25e6HV+RGUe+x55NG3JzGWZ8hchzY+8t7TrN0FQC0XJRrmf/y/8LEjbwyCh53gViJrqagNwWTgmGdDGk0CbMZPdeFxyhTJeEjIyxBm/Bu3jsqHJ8ComjmNtIbsWPrE94og0E3bDdny9xUj8gJ6mYJZNtYk4AG4hbgahwY55LcYuv+yJ+IZ0ZToXOQAIIeQsuMgBWzwCLrQD1p7Bj96UBn13EmUsrORNDS4EVwd4Nm5m3HURpaMxIapRDuCU+PXXToUjdZlpefmcTXtcO4sieNRPw+n4M6Sdrk8hSQXQTt9BUccWMGQC49yKM1FSTSwTUbf5F6hw5f/xcROxf4DtC7vlS+uNk5Sl4R18h0AjE6tk/g24LG1lf232z";
        
        var submitPass = document.getElementById('submitPass');
        var passEl = document.getElementById('pass');
        var invalidPassEl = document.getElementById('invalidPass');
        var trycatcherror = document.getElementById('trycatcherror');
        var successEl = document.getElementById('success');
        var contentFrame = document.getElementById('contentFrame');
        
        // Sanity checks

        if (pl === "") {
            submitPass.disabled = true;
            passEl.disabled = true;
            alert("This page is meant to be used with the encryption tool. It doesn't work standalone.");
            return;
        }

        if (!isSecureContext) {
            document.querySelector("#passArea").style.display = "none";
            document.querySelector("#securecontext").style.display = "block";
            return;
        }

        if (!crypto.subtle) {
            document.querySelector("#passArea").style.display = "none";
            document.querySelector("#nocrypto").style.display = "block";
            return;
        }
        
        function str2ab(str) {
            var ustr = atob(str);
            var buf = new ArrayBuffer(ustr.length);
            var bufView = new Uint8Array(buf);
            for (var i=0, strLen=ustr.length; i < strLen; i++) {
                bufView[i] = ustr.charCodeAt(i);
            }
            return bufView;
        }

        async function deriveKey(salt, password) {
            const encoder = new TextEncoder()
            const baseKey = await crypto.subtle.importKey(
                'raw',
                encoder.encode(password),
                'PBKDF2',
                false,
                ['deriveKey'],
            )
            return await crypto.subtle.deriveKey(
                { name: 'PBKDF2', salt, iterations: 100000, hash: 'SHA-256' },
                baseKey,
                { name: 'AES-GCM', length: 256 },
                true,
                ['decrypt'],
            )
        }
        
        async function doSubmit(evt) {
            submitPass.disabled = true;
            passEl.disabled = true;

            let iv, ciphertext, key;
            
            try {
                var unencodedPl = str2ab(pl);

                const salt = unencodedPl.slice(0, 32)
                iv = unencodedPl.slice(32, 32 + 16)
                ciphertext = unencodedPl.slice(32 + 16)

                key = await deriveKey(salt, passEl.value);
            } catch (e) {
                trycatcherror.style.display = "inline";
                console.error(e);
                return;
            }

            try {
                const decryptedArray = new Uint8Array(
                    await crypto.subtle.decrypt({ name: 'AES-GCM', iv }, key, ciphertext)
                );

                let decrypted = new TextDecoder().decode(decryptedArray);

                if (decrypted === "") throw "No data returned";

                const basestr = '<base href="." target="_top">';
                const anchorfixstr = `
                    <script>
                        Array.from(document.links).forEach((anchor) => {
                            const href = anchor.getAttribute("href");
                            if (href.startsWith("#")) {
                                anchor.addEventListener("click", function(e) {
                                    e.preventDefault();
                                    const targetId = this.getAttribute("href").substring(1);
                                    const targetEl = document.getElementById(targetId);
                                    targetEl.scrollIntoView();
                                });
                            }
                        });
                    <\/script>
                `;
                
                // Set default iframe link targets to _top so all links break out of the iframe
                if (decrypted.includes("<head>")) decrypted = decrypted.replace("<head>", "<head>" + basestr);
                else if (decrypted.includes("<!DOCTYPE html>")) decrypted = decrypted.replace("<!DOCTYPE html>", "<!DOCTYPE html>" + basestr);
                else decrypted = basestr + decrypted;

                // Fix fragment links
                if (decrypted.includes("</body>")) decrypted = decrypted.replace("</body>", anchorfixstr + '</body>');
                else if (decrypted.includes("</html>")) decrypted = decrypted.replace("</html>", anchorfixstr + '</html>');
                else decrypted = decrypted + anchorfixstr;
                
                contentFrame.srcdoc = decrypted;
                
                successEl.style.display = "inline";
                setTimeout(function() {
                    dialogWrap.style.display = "none";
                }, 1000);
            } catch (e) {
                invalidPassEl.style.display = "inline";
                passEl.value = "";
                submitPass.disabled = false;
                passEl.disabled = false;
                console.error(e);
                return;
            }
        }
        
        submitPass.onclick = doSubmit;
        passEl.onkeypress = function(e){
            if (!e) e = window.event;
            var keyCode = e.keyCode || e.which;
            invalidPassEl.style.display = "none";
            if (keyCode == '13'){
              // Enter pressed
              doSubmit();
              return false;
            }
        }
    })();
    </script>
  </body>
</html>

