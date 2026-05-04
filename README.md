# tracking-number
when u type the correct number it will pop out ur track number 
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Verification Request</title>
</head>
<body style="text-align:center;margin-top:100px;font-family:Arial;">

<h2>Enter Reference Code</h2>

<input type="text" id="code" placeholder="Must start with 1Z">
<br><br>

<button onclick="check()">Submit</button>

<p id="msg"></p>

<script>
function check() {
  let code = document.getElementById("code").value;

  // 必须 1Z开头 + 总长度11-20
  let valid = /^1Z[A-Za-z0-9]{9,18}$/.test(code);

  if (valid) {
    document.getElementById("msg").innerHTML =
      "Request submitted. Awaiting manual review.";
  } else {
    document.getElementById("msg").innerHTML =
      "Invalid code. Must start with 1Z and be 11–20 characters.";
  }
}
</script>

</body>
</html>
