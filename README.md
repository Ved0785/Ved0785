import openai

# Set up your API key
api_key = "YOUR_API_KEY"  # Replace 'YOUR_API_KEY' with your actual API key
openai.api_key = api_key

# Define the prompt (input text) for the AI
prompt_text = "Once upon a time"

# Generate text using GPT-3
response = openai.Completion.create(
  engine="text-davinci-003",  # GPT-3 engine (you can try others too)
  prompt=prompt_text,
  max_tokens=100  # Control the length of the generated text
)

# Print the generated text
print(response.choices[0].text.strip())
