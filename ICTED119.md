#Run a simple code using online editor that displays your full name and address

from flask import Flask, render_template

app = Flask(__name__)

# Define a dictionary with the user's information
user_info = {
    'name': 'April Montenegro',
    'address': {
        'Brgy': 'San Isidro Jaro',
        'city': 'Iloilo City',
    }
}

# Define a route that displays the user's information
@app.route('/')
def home():
    return render_template('home.html', user_info=user_info)

if __name__ == '__main__':
    app.run(debug=True)
