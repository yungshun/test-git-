# Example Markdown with Copy to Clipboard

Click the icon to copy the text:

<p id="text-to-copy">This is the text to be copied.</p>
<button onclick="copyToClipboard()">📋 Copy</button>

<script>
  function copyToClipboard() {
    var text = document.getElementById("text-to-copy").innerText;
    var textArea = document.createElement("textarea");
    textArea.value = text;
    document.body.appendChild(textArea);
    textArea.select();
    document.execCommand("copy");
    document.body.removeChild(textArea);
    alert("Copied the text: " + text);
  }
</script>
