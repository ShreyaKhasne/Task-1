<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Student Details</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .card {
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      width: 500px;
    }
    h2 {
      text-align: center;
      color: #333;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
    }
    th, td {
      border: 1px solid #ddd;
      padding: 10px;
      text-align: center;
    }
    th {
      background: #4CAF50;
      color: white;
    }
    button {
      display: block;
      margin: 15px auto;
      background: #4CAF50;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    button:hover {
      background: #45a049;
    }
  </style>
</head>
<body>

  <div class="card">
    <h2>Student Details</h2>
    <button onclick="showStudents()">Show All Students</button>
    <table id="studentTable">
      <thead>
        <tr>
          <th>Name</th>
          <th>Age</th>
          <th>Roll No</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
  </div>

  <script>
    // Array of 5 Student Objects
    const students = [
      { name: "Sayali", age: 20, rollNo: 101 },
      { name: "Aarav", age: 21, rollNo: 102 },
      { name: "Priya", age: 19, rollNo: 103 },
      { name: "Rahul", age: 22, rollNo: 104 },
      { name: "Ananya", age: 20, rollNo: 105 }
    ];

    // Function to show students in table
    function showStudents() {
      const tableBody = document.querySelector("#studentTable tbody");
      tableBody.innerHTML = ""; // clear old data

      students.forEach(student => {
        let row = `<tr>
                    <td>${student.name}</td>
                    <td>${student.age}</td>
                    <td>${student.rollNo}</td>
                   </tr>`;
        tableBody.innerHTML += row;
      });
    }
  </script>

</body>
</html>
