# Flask-AI-Text-Translator
---
### Description
---
This repo contains simple and easy to use language translator. This project utilises the extensive flask framework in order your spin up a localhost where you can interact with the application. The application takes in text from the user, the user  selects one of the optional languages then presses translate. The translation is done using Azure AI Translator API. Learn more about setting up [Azure]. On press the user will receive the translated text and the original text and the language in was tranlsated into. The user willl then be prompted to try again.

| #   | Categories  | Technologies       |
| --- | ----------- | ------------------ |
| 1   | Languages   | Python, HTML       |
| 2   | Frameworks  | Flask              |
| 3   | Services    | Microsoft Azure    |

---
## Getting Started

 For this you will need
- Gitbash/Bash (Windows/Linux and Apple)
- VsCode or Editor of your choice
- Python 3.6 or later

## Installations
---
#### Install Python

```bash
python --version
```

#### Set up virtual environment
---
If you have python installed the next set is to create a `projects` folder if you dont already have one
```bash
mkdir projects
cd projects
```
To use a virtual environment, we'll create and activate it. We create it by using the venv module, which you installed as part of your Python installation instructions earlier. When we activate it, we tell our system to use the folder we created for all of its Python needs

```bash
# Windows, macOS or Linux
# Create the environment
python -m venv venv
```
Then we want to activate the said environment
```bash
# Windows
# Activate the environment
./venv/scripts/activate

# macOS or Linux
# Activate the environment
source ./venv/bin/activate
```

Open the directory in Visual Studio Code
```bash
code .
```
This command opens the current directory (.) in Visual Studio Code.

Create a requirements.txt file

In Visual Studio Code, in the Explorer window, select "New File" next to the contoso directory. Name the file `requirements.txt` and add the following text:

```plaintext
flask
python-dotenv
requests
```
Save the requirements.txt file
Save the file by clicking Ctrl-S (Cmd-S on a Mac) or using the save option in the editor.

Install dependencies using pip
Return to the command or terminal window and run the following command:

```bash
pip install -r requirements.txt
```

This command installs the Python libraries listed in the requirements.txt file, along with their dependencies.
Make sure you have Python and pip installed on your system before running these commands. Also, ensure that the terminal or command prompt is set to the correct directory where your project is located.

---
### Using the Application
---
Open the integrated terminal
Run the following command to set the Flask runtime to development, which means that the server will automatically reload with every change

```Bash
# Windows
set FLASK_ENV=development

# Linux/macOS
export FLASK_ENV=development
```
Then to run the applicatoin on your local machine run:
```Bash
flask run
```

Open the application in a browser by navigating to http://localhost:5000

### Adding Languages
---
As of right now there are only 8 options 
```HTML
<select name="language" class="form-control">
    <option value="en">English</option>
    <option value="es">Spanish</option>
    <option value="fr">French</option>
    <option value="it">Italian</option>
    <option value="ja">Japanese</option>
    <option value="ru">Russian</option>
    <option value="de">German</option>
    <option value="ar">Arabic</option>
</select>
```

To add more options you have to copy one of those a lines
paste it and where the `value` is set enter your selected language. 
This is what interacted with the API for the translate language.
The link to this information can be found [here](https://learn.microsoft.com/en-us/azure/ai-services/translator/language-support?WT.mc_id=python-11210-chrhar).

---
### Using API
---
#### Get Translator service key

1. Browse to the [Azure portal](https://portal.azure.com/).
2. Select **Create a resource**.
3. In the Search box, enter **Translator**.
4. Select **Translator**. ![Completed Translator create form](https://www.google.com/imgres?imgurl=https%3A%2F%2Fraw.githubusercontent.com%2FDevExpress-Examples%2FReporting-Register-Azure-Cognitive-Translation-Service%2F2023.1%2FImages%2FAZURECreateTranlatorTextResource.png&tbnid=yN8Vm1zEYvvieM&vet=12ahUKEwir7Y624vKCAxX4FFkFHTyUCksQMygNegQIARBp..i&imgrefurl=https%3A%2F%2Fsupportcenter.devexpress.com%2Fticket%2Fdetails%2Ft882919%2Fhow-to-use-the-microsoft-azure-translator-text-api-in-report-localization&docid=TJnkZPtvh4zVHM&w=685&h=367&q=azure%20translate%20api&ved=2ahUKEwir7Y624vKCAxX4FFkFHTyUCksQMygNegQIARBp)
5. Select **Create**.
6. Complete the Create Translator form with the following values:
   - **Subscription:** Your subscription
   - **Resource group:**
     - Select **Create new** 
     - **Name:** flask-ai
    - **Resource group region:** Select a region near you
    - **Resource region:** Select the same region as above
    - **Name:** A unique value, such as ai-yourname
    - **Pricing tier:** Free F0

7. Select **Review + create**.
8. Select **Create**.
9. After a few moments, the resource will be created.
10. Select **Go to resource**.
11. Select **Keys and Endpoint** on the left side under **RESOURCE MANAGEMENT** or **KEYS**.
12. Next to **KEY 1**, select **Copy to clipboard**.
   > **Note:** There's no difference between **Key 1** and **Key 2**. By providing two keys, you have the opportunity to migrate to new keys by regenerating one while using the other.
13. Make a note of the **Text Translation** and **location** values.
---
#### Create .env file to store the key

1. Return to Visual Studio Code and create a new file in the root of the application by selecting **New file** and naming it `.env`.

   > **Important:** The `.` at the beginning of the file is required.

2. Paste the following text into `.env`:
```plaintext
   KEY=your_key
   ENDPOINT=your_endpoint
   LOCATION=your_location
```
---
# Enjoyyyyy 😄✨ M


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>
   [Azure]: <https://azure.microsoft.com/en-ca/free/search/?ef_id=_k_Cj0KCQiAyKurBhD5ARIsALamXaG5Gg-aW9h9bIRy8PuJiMcBdz10ygXwEF63RuGDfdsLSVuEMI_O1q0aAuXgEALw_wcB_k_&OCID=AIDcmmqz3gd78m_SEM__k_Cj0KCQiAyKurBhD5ARIsALamXaG5Gg-aW9h9bIRy8PuJiMcBdz10ygXwEF63RuGDfdsLSVuEMI_O1q0aAuXgEALw_wcB_k_&gad_source=1&gclid=Cj0KCQiAyKurBhD5ARIsALamXaG5Gg-aW9h9bIRy8PuJiMcBdz10ygXwEF63RuGDfdsLSVuEMI_O1q0aAuXgEALw_wcB>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
