// Set up the chat form
const chatForm = document.getElementById('chat-form');
const chatInput = document.getElementById('chat-input');
const chatOutput = document.getElementById('chat-output');

// Handle form submission
chatForm.addEventListener('submit', (event) => {
  event.preventDefault();

  // Get the user's message
  const message = chatInput.value;

  // Clear the input field
  chatInput.value = '';

  // Send the message to the GPT model and get a response
  fetch('/chat', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({ message }),
  })
  .then((response) => response.json())
  .then((response) => {
    // Display the GPT response in the chat output
    chatOutput.innerHTML += `<p><strong>GPT:</strong> ${response.message}</p>`;
  });
});
