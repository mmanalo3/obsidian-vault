# Linux
`export API_KEY=sk-1234567890abcdef`
# Windows
- [i] To set environment variable run the following command in the terminal:
	`set SAMPLE_VARIABLE=sv-1123456jdkjs9`
- [i] environment variables are not persistent

# Using .env file
- [!] should be added in the .gitignore file
- [i] requires `pip install python-dotenv`
#### Usage
`from dotenv import load_env`
`load_dotenv() # automatically locate .env file`
`# load_dotenv('/file/.env') # to manually locate .env file`

