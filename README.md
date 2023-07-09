

# SmarterGPT4 App
Leverages Philip's sample code to query gpt4's responses and improve them (possibly):)
https://www.youtube.com/@ai-explained-/about

This Python application leverages the capabilities of OpenAI's GPT-4 model to generate responses to user-input questions. The application is built using the Tkinter library for creating a simple and user-friendly GUI.
This script operates by first generating three potential responses from the OpenAI GPT-4 model to a user's question. These answer options are generated by encapsulating the user's question in a predefined question-answer structure and passing it to the model. After these initial answer options are returned, the program then forms a new "researcher" prompt that contains the original question and the three answer options. This new prompt tasks the AI model with evaluating and investigating the three answer options provided, identifying any flaws or faulty logic in each. This process essentially leverages the model's ability to critically assess information and generate a comparative analysis. Based on the feedback provided by this "researcher" role, the script then creates another prompt for the "resolver" role. This prompt is designed to encourage the model to take the researcher's feedback into account and to improve upon the best answer option, providing a final, optimized response. The use of multiple roles and prompts allows the script to generate, evaluate, and refine responses, enhancing the quality of the final output.

## Features

- User-friendly interface for inputting questions.
- Asynchronous processing of AI model responses, allowing the GUI to remain responsive during processing.
- Timer function to monitor the duration of AI model response generation.

## Dependencies

- Python 3.7 or later.
- Tkinter, included with Python by default.
- OpenAI Python v0.27.0 or later.
- The threading module, included with Python by default.

## How it Works

1. The application presents a user-friendly graphical interface to the user, where the user can input their question and submit it.
2. Upon submission, the question is sent to the GPT-4 model, which generates a response.
3. The response from the model is displayed in the application's interface.
4. Additionally, the application displays a timer, counting the duration from the moment the question was submitted until the response was received.

## Usage

1. Clone or download this repository to your local machine.
2. Install the required dependencies using pip:
    ```
    pip install openai
    ```
3. Replace "/path/to/your/openai/key.txt" with the path to your OpenAI API key file.
4. Run the application using Python:
    ```
    python main.py
    ```

## Configuration

- You may need to increase `max_tokens` in the `generate_gpt_response` function if you are dealing with particularly long queries or responses.
- The temperature in the `generate_gpt_response` function can be tweaked to influence the randomness of the model's responses (lower values make the output more deterministic, higher values increase randomness).
- [![Buy me a tea](https://img.shields.io/badge/Buy%20me%20a%20coffee--yellow.svg?logo=buy-me-a-coffee&logoColor=orange&style=social)](https://www.buymeacoffee.com/vjsible)


## Caution

Remember to securely store your OpenAI API key and not to expose it in your scripts or share it with others.

This application is just an example of what you can do with GPT-3.5-turbo. Always remember to use AI responsibly and ethically.
