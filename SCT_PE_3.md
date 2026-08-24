__TASK 3: PROMPTING FOR TASK AUTOMATION__

__Objective:__

Automate customer feedback analysis by converting unstructured customer feedback into structured JSON data\.

1. __Reusable Prompt:__

You are a customer feedback analyst\. Your task is to analyze the given customer feedback and extract the required information\.

Extract the following fields:

- Sentiment
- Category
- Issue
- Priority
- Action Required

Rules:

- Use only the information provided in the customer feedback\. 
- Do not invent or assume any missing information\. 
- If no issue is mentioned, return "None"\. 
- Keep the output concise and clear\. 
- Sentiment must be one of: "Positive", "Negative", "Mixed", or "Neutral"\. 
- Category must be one of: "Product", "Delivery", "Payment", "Service", or "Other"\. 
- Priority must be one of: "Low", "Medium", or "High"\. 
- For Action Required, provide a concise action based only on the issue mentioned\. If no action is needed, return "None"\. 
- Always return the result in the same JSON format\.  
Output format:  
\{  
"Sentiment": "",  
"Category": "",  
"Issue": "",  
"Priority": "",  
"Action Required": ""  
\}

Customer Feedback:  
\[Insert customer feedback here\]

1. __Input\-Output Examples:__

__Example 1:__

__Input:__  
“The dress quality is excellent and the color is beautiful, but my order arrived two days late\.”

__Output:__

\{

  "Sentiment": "Mixed",

  "Category": "Delivery",

  "Issue": "Order arrived two days late",

  "Priority": "Medium",

  "Action Required": "Review the delivery delay and take steps to prevent future delays"

\}

__Example 2:__

__Input:__  
“I was charged twice for my order\. Please refund the extra payment\.”

__Output:__

\{

  "Sentiment": "Negative",

  "Category": "Payment",

  "Issue": "Charged twice",

  "Priority": "High",

  "Action Required": "Refund the extra payment"

\}

__Example 3__

__Input:__  
“The product is great and arrived on time\. Thank you\!”

__Output:__

\{

  "Sentiment": "Positive",

  "Category": "Product",

  "Issue": "None",

  "Priority": "Low",

  "Action Required": "None"

\}

__3__\.__Reflection:__

Initially, my prompt did not specify fixed values for sentiment, category, and priority, which could produce inconsistent results\. I improved the prompt by defining allowed values for these fields and requiring a consistent JSON format\. I tested the revised prompt with different customer feedback examples and found that the outputs became more consistent and reliable\.

