
# Prerequisites

- Node version >= 21.0.0

- Python version >= 3.9.10
    
    Python version 3.9.10 or higher is recommended but other versions may also work.
- Globally installed packages for Truffle and Ganache-cli
    ```
    npm install -g truffle
    npm install -g ganache-cli
    ```
- Python packages
    
    Open application directory in pyCharm , exececute the command in pycharm's terminal:
    ```
    pip install -r application/requirements.txt
    ```
    It is recommended to create a virtual environment and then install the requirements and run the streamlit application in that virtual environment.

- Firebase project setup
    
    Create a project on Firebase Console. This will be used to setup an authentication service in the project. Enable email/password sign in method under Authentication in the Build section. Go to project settings. Add new app. Note the following details in a .env file inside the project's root directory.
    ```
    FIREBASE_API_KEY
    FIREBASE_AUTH_DOMAIN
    FIREBASE_DATABASE_URL (Set this to "")
    FIREBASE_PROJECT_ID
    FIREBASE_STORAGE_BUCKET
    FIREBASE_MESSAGING_SENDER_ID
    FIREBASE_APP_ID
    ```

- Pinata account setup
    
    Create an account on Pinata. Go to the API keys section and generate a new key. Note the API key and secret key in .env file.

- .env file
    
    Finally your .env file should contain the following things:
    ```
    PINATA_API_KEY = "<Your Pinata API key>"
    PINATA_API_SECRET = "<Your Pinata Secret Key>"
    FIREBASE_API_KEY = "<Your Firebase API key>"
    FIREBASE_AUTH_DOMAIN = "<Your Firebase auth domain>"
    FIREBASE_DATABASE_URL = ""
    FIREBASE_PROJECT_ID = "<Your Firebase project id>"
    FIREBASE_STORAGE_BUCKET = "<Your Firebase Storage Bucket>"
    FIREBASE_MESSAGING_SENDER_ID = "<Your Firebase messaging sender id>"
    FIREBASE_APP_ID = "<Your Firebase app id>"
    institute_email = "institute@gmail.com" # Feel free to modify this
    institute_password = "123456" # Feel free to modify this
    ```

## Running the project
1. Open a terminal anywhere and start the Ganache blockchain.
```
ganache-cli -h 127.0.0.1 -p 8545
```
2. Open a new terminal in the project's root directory and execute the following command to compile and deploy the smart contracts.

```
truffle migrate
```
3. Open application directory in pyCharm 

4. Launch the streamlit app.
```
streamlit run app.py
```
5. You can now view the app on your browser running on localhost:8501.

6. To stop the application, press Ctrl+C.
