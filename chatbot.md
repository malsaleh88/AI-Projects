
import google.generativeai as genai

# Replace with your Google Gemini API Key
genai.configure(api_key="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")

# Initialize Gemini Model
model = genai.GenerativeModel("gemini-pro")

# Function to generate a chatbot response
def chat_with_gemini(user_input):
    response = model.generate_content(user_input)
    return response.text

# Test chatbot
user_message = "Tell me a joke."
response = chat_with_gemini(user_message)
print("AI:", response)
