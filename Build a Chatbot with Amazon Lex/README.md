<div align="left">
  <h1 style="font-size: 36px; color: #2F855A; font-weight: bold;">Build a Chatbot with Amazon Lex</h1>
  <p style="font-size: 18px; color: #555;">Welcome to this interactive guide on building your own chatbot using Amazon Lex! Follow these steps to set up <strong>BankerBot</strong>, your personal banking assistant chatbot.</p>
</div>

---

## **Project Overview**

<div align="center">
  <table style="border: 1px solid #ddd; border-collapse: collapse; width: 80%;">
    <tr>
      <th style="text-align: left; padding: 8px;">Goal</th>
      <td style="padding: 8px;">Set up a basic chatbot that welcomes users and responds dynamically.</td>
    </tr>
    <tr>
      <th style="text-align: left; padding: 8px;">AWS Service Used</th>
      <td style="padding: 8px;">Amazon Lex</td>
    </tr>
    <tr>
      <th style="text-align: left; padding: 8px;">Difficulty</th>
      <td style="padding: 8px;">Easy</td>
    </tr>
    <tr>
      <th style="text-align: left; padding: 8px;">Time Required</th>
      <td style="padding: 8px;">60 Minutes</td>
    </tr>
    <tr>
      <th style="text-align: left; padding: 8px;">Cost</th>
      <td style="padding: 8px;">$0 (AWS Free Tier)</td>
    </tr>
  </table>
</div>

---

## **Step-by-Step Guide**

### **1. Set Up Your Lex Chatbot**

<div style="background: #F7FAFC; padding: 10px; border-left: 4px solid #2F855A; margin-bottom: 10px;">
  <p><strong>1. Create a New Bot:</strong></p>
  <ul>
    <li><strong>Name:</strong> BankerBot</li>
    <li><strong>Description:</strong> Banker Bot to help customers check their balance and make transfers.</li>
    <li><strong>IAM Permissions:</strong> Allow Lex to create a new role with basic permissions.</li>
    <li><strong>COPPA Compliance:</strong> Set to <code>No</code>.</li>
    <li><strong>Idle Session Timeout:</strong> 5 minutes.</li>
  </ul>
</div>

<div style="background: #EDF2F7; padding: 10px; border-left: 4px solid #2B6CB0; margin-bottom: 10px;">
  <p><strong>2. Choose a Voice:</strong></p>
  <ul>
    <li>Select a voice for your bot (e.g., Joanna or Matthew).</li>
    <li>Set the <strong>Intent Classification Confidence Score</strong> to <code>0.40</code>.</li>
  </ul>
</div>

<div style="background: #E2E8F0; padding: 10px; border-left: 4px solid #3182CE; margin-bottom: 10px;">
  <p><strong>3. Save and Build:</strong></p>
  <p>Click <strong>Save</strong> and then <strong>Build</strong> to generate your chatbot structure.</p>
</div>

---

### **2. Create Your First Intent**

<div style="background: #F7FAFC; padding: 10px; border-left: 4px solid #2F855A; margin-bottom: 10px;">
  <p><strong>1. Define the Intent:</strong></p>
  <ul>
    <li><strong>Name:</strong> WelcomeIntent</li>
    <li><strong>Description:</strong> Welcomes the user when they initiate interaction.</li>
  </ul>
</div>

<div style="background: #EDF2F7; padding: 10px; border-left: 4px solid #2B6CB0; margin-bottom: 10px;">
  <p><strong>2. Add User Inputs (Utterances):</strong></p>
  <pre style="background: #E2E8F0; padding: 10px; border-radius: 4px;">
Hi  
Hello  
I need help  
Can you help me?  
  </pre>
</div>

<div style="background: #E2E8F0; padding: 10px; border-left: 4px solid #3182CE; margin-bottom: 10px;">
  <p><strong>3. Define the Response:</strong></p>
  <p>Message: <code>Hi! I'm BB, the Banking Bot. How can I help you today?</code></p>
</div>

<div style="background: #F7FAFC; padding: 10px; border-left: 4px solid #2F855A; margin-bottom: 10px;">
  <p><strong>4. Save and Build:</strong></p>
  <p>Click <strong>Save Intent</strong> and then <strong>Build</strong>.</p>
</div>

<div style="background: #EDF2F7; padding: 10px; border-left: 4px solid #2B6CB0; margin-bottom: 10px;">
  <p><strong>5. Test Your Bot:</strong></p>
  <ul>
    <li>Use the <strong>Test</strong> interface to interact with your bot.</li>
    <li>Try predefined utterances like <code>Hi</code> and <code>Hello</code>.</li>
    <li>Test alternative inputs like <code>Help me</code> or <code>Hiya</code>.</li>
  </ul>
</div>

---

### **3. Manage FallbackIntent**

<div style="background: #F7FAFC; padding: 10px; border-left: 4px solid #2F855A; margin-bottom: 10px;">
  <p><strong>1. Customize Fallback Response:</strong></p>
  <p>Message: <code>Sorry, I am having trouble understanding. Can you describe what you'd like to do in a few words? I can help you find your account balance, transfer funds, and make a payment.</code></p>
</div>

<div style="background: #EDF2F7; padding: 10px; border-left: 4px solid #2B6CB0; margin-bottom: 10px;">
  <p><strong>2. Add Response Variations:</strong></p>
  <ul>
    <li><code>Hmm, could you try rephrasing that? I can assist with account balance, fund transfers, and payments.</code></li>
    <li><code>I didn't quite catch that. Please tell me if you need help with your account balance, fund transfers, or making a payment.</code></li>
  </ul>
</div>

<div style="background: #E2E8F0; padding: 10px; border-left: 4px solid #3182CE; margin-bottom: 10px;">
  <p><strong>3. Save and Build:</strong></p>
  <p>Save the changes, rebuild, and test the bot again.</p>
</div>

---

## **Conclusion**

<div align="left">
  <p style="font-size: 16px; color: #555;">Congratulations! You've successfully built a chatbot using Amazon Lex. BankerBot is now ready to welcome users and handle basic conversations. 🚀</p>
</div>
