# Four Cornes 2013 Boys - Red Team Roster

Welcome to the Four Corners 2013 boys red team roster. This is a way for us to get to know our kids' names, numbers, and parent names.

You can view the live site here: http://FrankDraws.github.io/fc2013boysroster

# Code
This is a typical data table. I used JavaScript to add sequential numbering in the first cell of each row in order to get the count of total players. 

The benefit of the sequential numbering code is that if a player is deleted or added, you don't have to manually update the numbers. If one player is added or removed, especially at the top of the table, you'd have to manually update the entire sequence. With the sequential numbering code, you can make any changes as needed and JavaScript will take care of the numbering. 

The following code was written by ChatGPT:
```javascript
    // Wait for the DOM content to be loaded
    document.addEventListener('DOMContentLoaded', function () {
      // Get the first table on the page
      var table = document.querySelector('tbody');

      // Get all the table rows within the first table
      var rows = table.querySelectorAll('tr');

      // Loop through each row and set the sequential number
      for (var i = 0; i < rows.length; i++) {
        // Get the first cell in the current row
        var cell = rows[i].querySelector('td:first-child');

        // Create a span element for the number
        var numberSpan = document.createElement('span');

        // Set the sequential number as the span's text
        numberSpan.textContent = i + 1;

        // Append the span element to the cell
        cell.appendChild(numberSpan);
      }
    });
```

This was the code I initially used and it worked. Then I received an email from Hashnode about Rix.chat, so I tried it out. Here's the result (and the code I'm using for this table):

```javascript
    const table = document.getElementById("main");
    const rows = table.rows;

    for (let i = 0; i < rows.length; i++) {
      rows[i].cells[0].textContent = i + 1;
    }
```

In this version, I decided to go with an `ID` to target the table. 