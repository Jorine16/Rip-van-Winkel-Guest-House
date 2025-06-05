<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Rip van Winkel Guest House</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 text-gray-800">
  <header class="bg-white py-4 shadow text-center">
    <img src="logo Rvwgh.png" alt="Rip van Winkel Guest House Logo" class="mx-auto h-24 mb-2" />
    <h1 class="text-xl font-medium">Welcome to Rip van Winkel Guest House</h1>
    <p class="text-sm text-gray-600">Book your stay with ease</p>
  </header>

  <main class="p-6 max-w-5xl mx-auto">
    <section class="bg-white p-6 rounded-lg shadow mb-8">
      <h2 class="text-xl font-semibold mb-4">Make a Booking</h2>
      <form class="grid gap-4 md:grid-cols-2">
        <input type="text" placeholder="Full Name" class="p-2 border rounded" required />
        <input type="email" placeholder="Email Address" class="p-2 border rounded" required />
        <input type="date" class="p-2 border rounded" required />
        <input type="number" placeholder="Number of Guests" class="p-2 border rounded" required />
        <button type="submit" class="col-span-2 bg-green-600 text-white py-2 rounded hover:bg-green-700">Book Now</button>
      </form>
    </section>

    <section class="bg-white p-6 rounded-lg shadow mb-8">
      <h2 class="text-xl font-semibold mb-4">Availability Calendar</h2>
      <table class="w-full text-center border-collapse" id="calendar-table"></table>
    </section>

    <div class="text-center">
      <a href="checkin.html" class="inline-block bg-blue-600 text-white px-6 py-3 rounded hover:bg-blue-700">
        Fill in Check-In Form
      </a>
    </div>
  </main>

  <script>
    const calendarTable = document.getElementById("calendar-table");
    const date = new Date();
    const year = date.getFullYear();
    const month = date.getMonth();

    function buildCalendar(y, m) {
      const firstDay = new Date(y, m, 1).getDay();
      const daysInMonth = new Date(y, m + 1, 0).getDate();
      const weekdays = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
      let html = "<tr>" + weekdays.map(d => `<th class='p-2 border bg-gray-200'>${d}</th>`).join("") + "</tr><tr>";

      for (let i = 0; i < firstDay; i++) html += "<td class='p-2 border'></td>";
      for (let day = 1; day <= daysInMonth; day++) {
        const isToday = day === date.getDate() && m === date.getMonth() && y === date.getFullYear();
        html += `<td class='p-2 border ${isToday ? "bg-green-500 text-white" : ""}'>${day}</td>`;
        if ((day + firstDay) % 7 === 0) html += "</tr><tr>";
      }
      html += "</tr>";
      calendarTable.innerHTML = html;
    }

    buildCalendar(year, month);
  </script>
</body>
</html>
