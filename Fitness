import streamlit as st

# Page title
st.title("💪 Fitness Chatbot")

# Initialize chat history
if "messages" not in st.session_state:
    st.session_state.messages = []

# Display chat history
for message in st.session_state.messages:
    with st.chat_message(message["role"]):
        st.markdown(message["content"])

# User input
user_input = st.chat_input("Ask me about fitness, diet, workouts...")

# Simple rule-based responses
def fitness_bot(user_input):
    user_input = user_input.lower()

    if "workout" in user_input:
        return "Try a mix of cardio and strength training. Example: Push-ups, squats, running."
    
    elif "diet" in user_input:
        return "Focus on protein, healthy fats, and carbs. Drink plenty of water!"
    
    elif "weight loss" in user_input:
        return "Calorie deficit + regular exercise is key. Stay consistent!"
    
    elif "muscle gain" in user_input:
        return "Progressive overload + high protein diet will help build muscle."
    
    elif "hello" in user_input or "hi" in user_input:
        return "Hey! I'm your fitness assistant 💪 Ask me anything!"
    
    else:
        return "I'm not sure, but stay active and eat healthy! 💪"

# When user sends message
if user_input:
    # Show user message
    st.session_state.messages.append({"role": "user", "content": user_input})
    
    with st.chat_message("user"):
        st.markdown(user_input)

    # Bot response
    response = fitness_bot(user_input)

    st.session_state.messages.append({"role": "assistant", "content": response})

    with st.chat_message("assistant"):
        st.markdown(response)
