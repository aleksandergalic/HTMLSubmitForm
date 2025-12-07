# HTMLSubmitForm
An example with steps of how to make an HTML Submit Form

## Basic Structure
- add a HTML document declaration, a lang, stylesheet link, favicon, charset and standard elements, like <head>, <body>, <title>...
  
```
<!DOCTYPE html>
<html lang="sl">
<link rel="stylesheet" href="css/style.css">
<link rel="icon" type="image/x-icon" href="/images/favicon.ico">
<meta charset="utf-8">

<head>
  <body>
    <h1 class="center">Spletno naročilo majice</h1>
  </body>
</head>
</html>
```

## Actual Submit Form
- Now, add the actual submit form. You have multiple choices of how to make an organized submit form. Here, I chose to put all items in a <table> element
- Use the method="POST" to hide input data from the user
- Add a file like submission.html that loads when the user fills out the data and submits it

```
<form action="submission.html" method="POST">
```
```
<table>

      <tr>
        <th class="vsebina"><label for="ime">Ime*:</label></th>
        <td><input type="text" id="ime" placeholder="ime"></td>
      </tr>
      <td>
          <input type="submit" value="Oddaj naročilo">
        </td>
      </tr>
    </table>
</form>
```

## Result
- The resulting code should be something like this:

```
<!DOCTYPE html>
<html lang="sl">
<link rel="stylesheet" href="css/style.css">
<link rel="icon" type="image/x-icon" href="/images/favicon.ico">
<meta charset="utf-8">

<head>

<body>
  <h1 class="center">Spletno naročilo majice</h1>
  <img src="majica.png" alt="majica">
  <form action="submission.html" method="POST">
    <table>

      <tr>
        <th class="vsebina"><label for="ime">Ime*:</label></th>
        <td><input type="text" id="ime" placeholder="ime"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="priimek">Priimek*:</label></th>
        <td><input type="text" id="priimek" placeholder="priimek"></td>
      </tr>

      <tr class="vsebina">
        <th class="vsebina"><label for="email">E-mail</label></th>
        <td><input type="email" id="email" name="email" placeholder="email@example.com"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="ime">Naslov spletne strani*:</label></th>
        <td><input type="text" id="naslov" placeholder="naslov"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="datum">Datum naročila:</label></th>
        <td><input type="date" id="datum" name="datum"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="ime">Barva majice*:</label></th>
        <td><input type="text" id="ime" placeholder="ime"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="ime">Velikost majice*:</label></th>
        <td><input type="text" id="ime" placeholder="ime"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="ime">Velikost majice*:</label></th>
        <td><p>&ensp;S&ensp;&ensp;&ensp;M&ensp;&ensp;&ensp;L&ensp;&ensp;&ensp;XL&ensp;&ensp;XXL</p></td>
      </tr>
      <tr>
        <td></td><td><input type="range" min="1" max="5" value="3" class="slider" id="myRange"></td>
      </tr>
      <tr>
        <th class="vsebina"><label for="kolicina">Količina(med 1 in 100)*:</label></th>
        <td><input type="number" id="kolicina" name="kolicina" min="1" max="100" /></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="kolicina">Dan dostave:</label></th>
        <td><input type="date" id="datum" name="datum"></td>
      </tr>

      <tr>
        <th class="vsebina"><label for="dan">Ura dostave</label></th>
        <td><input type="time" id="ura" name="ura" required /></td>
      </tr>
      <tr>
        <td class="center"><input type="reset" value="Znova">
        </td>
        <td>
          <input type="submit" value="Oddaj naročilo">
        </td>
      </tr>

    </table>
  </form>
</body>

</html>
```
## Images
<img src="result1" alt="Submit Form">

<img src="result2" alt="submission.html">
