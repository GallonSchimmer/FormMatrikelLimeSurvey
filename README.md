# Umfrageformular für LimeSurvey

Dies ist ein einfaches HTML-Formular, das QR-Codes für LimeSurvey-Umfragen generiert. Der Benutzer kann die Matrikel und die Sprache auswählen und erhält QR-Codes für die Umfrage mit den entsprechenden Parametern.

## Verwendung

1. Kopieren Sie den folgenden Link zur HTML-Datei: [FormMatrikelLimeSurvey.html](https://github.com/GallonSchimmer/FormMatrikelLimeSurveyTemplate/blob/main/FormMatrikelLimeSurvey.html)

2. Öffnen Sie einen neuen Tab und besuchen Sie den folgenden Link: [htmlpreview.github.io](https://htmlpreview.github.io/)

3. Fügen Sie den kopierten Link zur HTML-Datei in das Input-Feld auf der Seite ein und drücken Sie Enter.

4. Kopieren Sie den LimeSurvey-Link: https://surveys.ak.tu-berlin.de/index.php/492863?newtest=Y&lang=en

5. Fügen Sie Ihre Matrikel in das entsprechende Feld im geöffneten Formular ein.

6. Wählen Sie Ihre bevorzugte Sprache aus dem Dropdown-Menü.

7. Klicken Sie auf den Button "QR-Codes generieren".
 
8. Die generierten QR-Codes werden unter dem Formular angezeigt.

9. # LimeSurvey Survey Form

This is a simple HTML form that generates QR codes for LimeSurvey surveys. Users can input their student ID and select a language to receive QR codes for the survey with the respective parameters.

## Usage

1. Copy the following link to the HTML file: [FormMatrikelLimeSurvey.html](https://github.com/GallonSchimmer/FormMatrikelLimeSurveyTemplate/blob/main/FormMatrikelLimeSurvey.html)

2. Open a new tab and visit the following link: [htmlpreview.github.io](https://htmlpreview.github.io/)

3. Paste the copied link to the HTML file into the input field on the page and press Enter.

4. Copy the LimeSurvey link: https://surveys.ak.tu-berlin.de/index.php/492863?newtest=Y&lang=en
   
6. Enter your student ID in the corresponding field in the opened form.

7. Choose your preferred language from the dropdown menu.

8. Click the "Generate QR Codes" button.

9. The generated QR codes will be displayed below the form.

## Note

Below is the syntax form of the code with placeholders for user instructions:

```javascript
<script>
    // Function to generate QR codes
    function generateQR() {
        // Get values from input fields
        var matrikel = document.getElementById("matrikel").value;
        var sprache = document.getElementById("sprache").value;

        // Prompt user for the first half of the LimeSurvey URL
        var baseUrl = prompt("Enter the first half of the LimeSurvey URL:");

        // Construct the complete URL for generating QR code
        var qrUrl = baseUrl + "&lang=" + sprache + "&m_id=" + matrikel;

        // Display the generated QR code below the form
        document.getElementById("qrCodes").innerHTML = "<img src='https://api.qrserver.com/v1/create-qr-code/?data=" + encodeURIComponent(qrUrl) + "' alt='QR-Code " + sprache + "'>";
    }
</script>
```

Explanation:

- `var matrikel = document.getElementById("matrikel").value;`:
  - **Tool Used:** `document.getElementById`: JavaScript DOM (Document Object Model) method to get the HTML element with the specified ID.
  - **Purpose:** Retrieves the value entered by the user in the input field with the ID "matrikel."

- `var sprache = document.getElementById("sprache").value;`:
  - **Tool Used:** `document.getElementById`: JavaScript DOM method.
  - **Purpose:** Retrieves the value selected by the user in the dropdown menu with the ID "sprache."

- `var baseUrl = prompt("Enter the first half of the LimeSurvey URL:");`:
  - **Tool Used:** `prompt`: JavaScript function that displays a dialog box with a message and an input field, prompting the user for input.
  - **Purpose:** Prompts the user to enter the first half of the LimeSurvey URL.

- `var qrUrl = baseUrl + "&lang=" + sprache + "&m_id=" + matrikel;`:
  - **Purpose:** Constructs the complete URL for generating the QR code by combining the user-provided base URL, language, and Matrikel number.

- `document.getElementById("qrCodes").innerHTML = "<img src='https://api.qrserver.com/v1/create-qr-code/?data=" + encodeURIComponent(qrUrl) + "' alt='QR-Code " + sprache + "'>";`:
  - **Tool Used:** `document.getElementById` and `innerHTML`: JavaScript DOM methods.
  - **Purpose:** Updates the HTML content of an element with the ID "qrCodes" to include an image tag with the dynamically generated QR code. The `encodeURIComponent` function ensures proper encoding of the URL for inclusion in the HTML.






