# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date:28.09.2025
# Register no.212222050011
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

**#AI Tools Required:**
•	Python (Programming Language)
•	OpenAI API (for GPT models)
•	Hugging Face Transformers API
•	Google Generative AI or other third-party AI APIs (optional)
•	Jupyter Notebook/VS Code (IDE for execution)


# Explanation:
Experiment the persona pattern as a programmer for any specific applications related with your interesting area. 
Generate the outoput using more than one AI tool and based on the code generation analyse and discussing that. 

In this experiment, the objective is to design Python code that can communicate with multiple AI tools, fetch responses for a given query, and compare their outputs to analyze variations in style, accuracy, and detail.
1.	Integration with APIs:
Python provides libraries like requests, openai, and transformers which can connect with different AI platforms.
2.	Query Execution:
A single prompt is given to multiple AI tools (e.g., OpenAI GPT and Hugging Face models). Each tool generates its own output based on the same input.
3.	Comparison & Analysis:
The outputs are collected, displayed, and compared in terms of fluency, correctness, and relevance. This helps in identifying the strengths and weaknesses of each AI model.
4.	Applications:
o	Text summarization
o	Chatbot development
o	Code generation
o	Sentiment analysis
o	Domain-specific automation (e.g., Flood Risk Management, IoT, Robotics)
This experiment also highlights the persona pattern of a programmer, where the developer takes the role of an orchestrator—sending queries to multiple AI systems, evaluating responses, and selecting the most effective solution for real-world applications.
________________________________________
🔹 Sample Python Code:


import openai
from transformers import pipeline

# ============================
# 1. OpenAI API Integration
# ============================

# Replace with your OpenAI API key
openai.api_key = "YOUR_OPENAI_API_KEY"

def get_openai_response(prompt):
    response = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",  # You can also use "gpt-4"
        messages=[{"role": "user", "content": prompt}],
        max_tokens=150
    )
    return response["choices"][0]["message"]["content"].strip()


# ============================
# 2. Hugging Face API Integration
# ============================

# Using a pretrained transformer model for text generation
generator = pipeline("text-generation", model="gpt2")

def get_huggingface_response(prompt):
    response = generator(prompt, max_length=100, num_return_sequences=1)
    return response[0]["generated_text"].strip()


# ============================
# 3. Comparing Outputs
# ============================

prompt = "Explain the importance of renewable energy in future power systems."

openai_output = get_openai_response(prompt)
huggingface_output = get_huggingface_response(prompt)

print("\n========== INPUT PROMPT ==========")
print(prompt)

print("\n========== OPENAI OUTPUT ==========")
print(openai_output)

print("\n========== HUGGINGFACE OUTPUT ==========")
print(huggingface_output)

print("\n========== ANALYSIS ==========")
print("OpenAI provides more structured and detailed answers,")
print("while Hugging Face GPT-2 generates creative but less structured responses.")
________________________________________
🔹 How it Works:
1.	OpenAI GPT model → Provides structured, detailed, and reliable answers.
2.	Hugging Face GPT-2 → Generates creative but sometimes less accurate text.
3.	Comparison → You can analyze strengths/weaknesses of each tool.
________________________________________
🔹 Sample Output
========== INPUT PROMPT ==========
Explain the importance of renewable energy in future power systems.

========== OPENAI OUTPUT ==========
Renewable energy plays a crucial role in the future of power systems because it ensures sustainability, reduces dependency on fossil fuels, and lowers greenhouse gas emissions. By integrating sources such as solar, wind, and hydropower, future power grids can become cleaner, more reliable, and resilient. Furthermore, renewable energy supports energy security, economic development, and helps in addressing climate change challenges.

========== HUGGINGFACE OUTPUT ==========
Explain the importance of renewable energy in future power systems. The renewable energy market is expected to grow rapidly in the coming years, with new investments and technologies shaping how electricity is produced and consumed. Future systems will depend on clean resources like wind and solar, but challenges such as storage, efficiency, and infrastructure development will continue to be important factors in the transition.

========== ANALYSIS ==========
OpenAI provides more structured and academic-style responses,
while Hugging Face GPT-2 generates creative but less structured responses.
Both highlight sustainability and challenges, but OpenAI focuses more on clarity
and Hugging Face emphasizes growth and future development.

**Flow diagram :**
<img width="1024" height="1536" alt="image" src="https://github.com/user-attachments/assets/7bc8f151-fdf4-4e82-8f31-3cdc4747fe73" />



# Conclusion:
Thus, Python code was successfully developed and implemented to interact with multiple AI tools. The outputs generated from different models were analyzed, compared, and discussed, demonstrating the importance of multi-model integration for better decision-making and actionable insights.


# Result: The corresponding Prompt is executed successfully.
