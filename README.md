<!DOCTYPE html>
<html>
<head>
  <title>Jokes Bro</title>
  <style>
    body {text-align:center; font-family:sans-serif; padding:20px; background:#FFD700}
    button {padding:15px; font-size:18px; border-radius:10px; border:none}
  </style>
</head>
<body>
  <h1>😂 Jokes Bro 😂</h1>
  <p id="joke">Button dabao joke aayega</p>
  <button onclick="newJoke()">Naya Joke</button>

  <script>
    async function newJoke() {
      let res = await fetch("https://official-joke-api.appspot.com/random_joke")
      let data = await res.json()
      document.getElementById("joke").innerText = data.setup + "\n\n" + data.punchline
    }
  </script>
</body>
</html>
