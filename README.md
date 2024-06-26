# Simple-Calculator-Using-Google-Colab-and-Streamlit

This project demonstrates how to create a simple web-based calculator using Google Colab and Streamlit. The app performs basic arithmetic operations (addition, subtraction, multiplication, and division) and can be accessed via a local tunnel.

Prerequisites
To run this project, you'll need:

A Google Colab account
Basic knowledge of Python

Instructions
Install Streamlit:
1. Install Streamlit within the Google Colab environment by running:
!pip install streamlit -q

2. Get Your IP Address:
Retrieve your external IP address using:
!wget -q -O - ipv4.icanhazip.com

3. Run the Streamlit App:
Create a Python script named app.py with the following content:
import streamlit as st

st.title("Simple Calculator")

number1 = st.number_input("Enter first number")
number2 = st.number_input("Enter second number")

operation = st.selectbox("Choose operation", ("Add", "Subtract", "Multiply", "Divide"))

if st.button("Calculate"):
    if operation == "Add":
        result = number1 + number2
    elif operation == "Subtract":
        result = number1 - number2
        else:
            result = "Error! Division by zero."
    st.write("Result:", result)


4. Run Streamlit and Expose the App:
Run the Streamlit app and expose it using a local tunnel:
!streamlit run app.py & npx localtunnel --port 8501

5. Access the App:
Follow the URL provided by localtunnel to access your calculator app from any web browser.


Usage
1). Open Google Colab and create a new notebook.
2). Follow the instructions above to install dependencies and run the app.
3). Use the provided local tunnel URL to access the calculator.
