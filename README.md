<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sports League Management</title>
    <link rel="stylesheet" href="new.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        /* Add your CSS styles here */
    </style>
</head>
<body>
    <p>HEllo bro!!!</p>
    <header>
        <h1>Sports League Management</h1>
    </header>

    <nav>
        <button id="loadDataBtn">Load League</button>
        <button id="IplDataBtn"><a href="crick.html">Indian primier League</a></button>
        <button id="IccDataBtn"><a href="ICC.html">World Cup</a></button>
        <button id="BblDataBtn"><a href="bbl.html">Bash League</a></button>
        <button id="IaT20DataBtn"><a href="T20.html">Ind Vs Aus T20</a></button>
        <button id="PklDataBtn"><a href="pkl.html">Pro Kabaddi League</a></button>
    </nav>

    <main>
        <div id="leagueData"></div>
    </main>

    <footer>
        <p>&copy; 2023 Your League Name</p>
    </footer>

    <script>
        // Mock data for demonstration purposes
        const leagueData = {
            teams: [
                { name: 'Team A', points: 10 },
                { name: 'Team B', points: 8 },
                { name: 'Team C', points: 9 },
                { name: 'Team D', points: 10},
                { name: 'Team E', points: 7},
                { name: 'Team F', points: 9},
                // Add more teams as needed
            ],
            matches: [
                { homeTeam: 'Team A', awayTeam: 'Team B', result: '2-1' },
                // Add more matches as needed
            ],
        };

        // Function to load and display league data
        function loadLeagueData() {
            const leagueDataDiv = document.getElementById('leagueData');

            // Clear previous data
            leagueDataDiv.innerHTML = '';

            // Display teams
            leagueData.teams.forEach(team => {
                const teamDiv = document.createElement('div');
                teamDiv.textContent = ${team.name} - Points: ${team.points};
                leagueDataDiv.appendChild(teamDiv);
            });

            // Display matches
            leagueData.matches.forEach(match => {
                const matchDiv = document.createElement('div');
                matchDiv.textContent = ${match.homeTeam} vs ${match.awayTeam} - Result: ${match.result};
                leagueDataDiv.appendChild(matchDiv);
            });
        }

        // Event listener for the load data button
        const loadDataBtn = document.getElementById('loadDataBtn');
        loadDataBtn.addEventListener('click', loadLeagueData);

        // You would typically fetch data from a server instead of using mock data
    </script>
</body>
</html>
