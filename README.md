<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Salbinaza's Calorie Counter</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 2em; }
        .result { margin-top: 1em; color: #007700; }
    </style>
</head>
<body>
    <h1>Hello SALBINAZA</h1>
    <p>You are here to count your calories</p>
    <p>Let's start!</p>
    <form id="calorieForm">
        <label>
            Type the number of meals you ate today:
            <input type="number" id="mealCount" required>
        </label><br><br>
        <label>
            Input your current weight (kg):
            <input type="number" id="currentWeight" required>
        </label><br><br>
        <button type="submit">Calculate</button>
    </form>
    <div id="output" class="result"></div>
    <script>
        document.getElementById('calorieForm').onsubmit = function(e) {
            e.preventDefault();
            const add = 27831;
            const caladd = 23;
            const mealCount = Number(document.getElementById('mealCount').value);
            const currentWeight = Number(document.getElementById('currentWeight').value);
            const totalCalories = mealCount + add;
            const newWeight = currentWeight + caladd;
            document.getElementById('output').innerHTML = `
                OH NO!? You ate <b>${totalCalories}</b> calories today. Now you will gain 5 kg only today.<br>
                So your new weight is: <b>${newWeight} kg</b><br>
                Wow, good job you super passed me.<br>
                Dw, I'm still the best, love u.
            `;
        };
    </script>
</body>
</html>
