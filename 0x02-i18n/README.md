# 0x02. i18nObjective
The project aims to implement internationalization (i18n) in a Flask web application, enabling it to support multiple languages and display localized content based on user preferences. This involves setting up a basic Flask app, integrating the Flask-Babel extension for language translation, and handling user-specific settings like preferred language and time zone.


| **Task** | **Description** |
|---|---|
| **0. Basic Flask app** | Set up a basic Flask app with a single route `/` that displays "Welcome to Holberton" in the title and "Hello world" as a header. This establishes the initial structure for the web application. |
| **1. Basic Babel setup** | Introduce internationalization (i18n) by setting up Flask-Babel. The task involves installing the library, configuring supported languages, and setting the default locale and timezone. This is crucial for supporting multiple languages. |
| **2. Get locale from request** | Implement logic to detect the preferred language of the user based on the request headers. This enhances the app's ability to serve content in the user's preferred language. |
| **3. Parametrize templates** | Modify templates to use gettext functions for translation, set up a configuration file for Babel, and create message catalogs. This step allows for the extraction and translation of text in the application. |
| **4. Force locale with URL parameter** | Enable users to manually select a language via URL parameters, overriding automatic detection. This provides users with more control over the language settings. |
| **5. Mock logging in** | Simulate user login to test localization features under different user settings. This is done by setting a user context based on URL parameters. |
| **6. Use user locale** | Prioritize user locale settings in determining the displayed language, ensuring a personalized experience based on user preferences. |
| **7. Infer appropriate time zone** | Implement logic to determine and validate the user's time zone, enhancing the app's ability to display localized time information. |
| **8. Display the current time** | Use the determined time zone to display the current time in the appropriate format and language. This feature adds dynamic, localized content to the web page. |

### Additional Details for Each Task

#### 0. Basic Flask app
- **Purpose**: Establish a simple web server framework.
- **Outcome**: A minimal Flask application that renders a basic HTML page.

#### 1. Basic Babel setup
- **Purpose**: Prepare the application for internationalization by configuring language support.
- **Outcome**: The app can now recognize English and French as supported languages.

#### 2. Get locale from request
- **Purpose**: Automatically detect the user's preferred language.
- **Outcome**: The app can dynamically adjust the language based on the client's browser settings.

#### 3. Parametrize templates
- **Purpose**: Enable dynamic translation of content.
- **Outcome**: The application can now handle multiple languages by translating text in templates.

#### 4. Force locale with URL parameter
- **Purpose**: Allow users to explicitly set the language.
- **Outcome**: Users can change the language by adding a `locale` parameter to the URL.

#### 5. Mock logging in
- **Purpose**: Simulate different user experiences without a real authentication system.
- **Outcome**: The app can show different content based on the simulated user's settings.

#### 6. Use user locale
- **Purpose**: Prioritize personalized user settings over browser settings.
- **Outcome**: The app provides a more tailored experience by considering user preferences.

#### 7. Infer appropriate time zone
- **Purpose**: Determine and validate the user's time zone.
- **Outcome**: Accurate time display according to the user's location or settings.

#### 8. Display the current time
- **Purpose**: Enhance the user interface by showing real-time data.
- **Outcome**: Users see the current time formatted according to their locale and language preferences.
