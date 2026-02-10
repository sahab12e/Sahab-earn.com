<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <title>टास्क कमाएँ पैसा</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        .task { margin: 20px; padding: 10px; border: 1px solid #ccc; }
        button { padding: 10px; background: green; color: white; border: none; cursor: pointer; }
    </style>
</head>
<body>
    <h1>टास्क पूरा करें और पैसा कमाएँ!</h1>
    <p>आपके पॉइंट्स: <span id="points">0</span></p>
    
    <div class="task">
        <p>टास्क 1: एक सवाल का जवाब दें - भारत की राजधानी क्या है?</p>
        <input type="text" id="answer1" placeholder="जवाब टाइप करें">
        <button onclick="checkTask(1)">सबमिट</button>
    </div>
    
    <div class="task">
        <p>टास्क 2: एक फोटो अपलोड करें (सिमुलेशन)।</p>
        <input type="file" id="file2">
        <button onclick="checkTask(2)">सबमिट</button>
    </div>
    
    <script>
        let points = 0;
        function checkTask(taskId) {
            if (taskId === 1) {
                const answer = document.getElementById('answer1').value.toLowerCase();
                if (answer === 'दिल्ली') {
                    points += 10;
                    alert('सही! 10 पॉइंट्स मिले।');
                } else {
                    alert('गलत जवाब।');
                }
            } else if (taskId === 2) {
                // सिमुलेशन: असल में फाइल चेक करें
                points += 20;
                alert('फाइल अपलोड हुई! 20 पॉइंट्स मिले।');
            }
            document.getElementById('points').innerText = points;
        }
    </script>
</body>
</html>
