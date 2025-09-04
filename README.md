Weather Dashboard - Save Weather Data to AWS S3


This is a Python application built by that:

* Fetches real-time weather data from the OpenWeather API.

* Ensures your Amazon S3 bucket exists (creates it if not).

* Saves weather information as timestamped JSON files inside S3.

   !Features

* Get live weather for one or more cities.

* Store results safely in Amazon S3.

* Automatically creates the S3 bucket if it doesn’t exist.

* Each file has a timestamp for unique tracking.

   !Requirements

* Python 3.8+

* AWS account with IAM user having S3 permissions

* OpenWeather API key (Free Signup)

   !Setup Instructions

Create a project folder and move your script inside. Example structure:

my_dashboard/
├── src/
│   └── bhargav-dashboard.py    # Your Python script
├── .env                        # Store API keys and AWS details here
└── requirements.txt

 install Dependencies

!Create a requirements.txt file with:
    boto3
    requests
    python-dotenv
!Then install:
  pip install -r requirements.txt

! Environment Variables

Create a .env file in the root folder with:

OPENWEATHER_API_KEY=your_openweather_api_key_here
AWS_BUCKET_NAME=bhargava-weather-bucket-09042025
AWS_REGION=ap-south-1


 Bucket Naming Rules:

Must be lowercase

No spaces

Must be globally unique

Example: bhargava-weather-bucket-1816

! Configure AWS  run credentials 
   
   AWS configure

* AWS Access Key

* AWS Secret Key

* Default Region

* Output format
 
! Running the Application

From the root folder, run:

python src/bhargav-dashboard.py

 Expected output :

Bucket bhargava-weather-bucket-09042025 not found, creating...
Successfully created bucket bhargava-weather-bucket-09042025 in ap-south-1

Fetching weather for Hyderabad...Temperature: 81.16°F ,Feels like: 83.73°F ,Humidity: 63%
Conditions: overcast clouds
Successfully saved data for Hyderabad to S3

