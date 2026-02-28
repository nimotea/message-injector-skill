---
name: message-injector
description: Inject information from a source text into a target template with placeholders. Use this skill when the user provides source information and a template string, and wants to see the completed message.
---

# Message Injector

This skill extracts information from a provided source text and injects it into a target template string that contains placeholders.

## When to use this skill
- When the user provides a source text (e.g., "Bob is 30 years old") and a template (e.g., "Hello {name}, age {age}").
- When the user asks to "fill in the blanks" based on a description.
- When the user wants to parameterize a message with specific data.

## Instructions
1.  **Analyze the Source Text**: Identify key entities and information in the source text that correspond to the placeholders in the template.
2.  **Identify Placeholders**: Locate all placeholders in the template string. Placeholders are typically enclosed in curly braces `{}` or other delimiters (e.g., `{{}}`, `<>`).
3.  **Extract and Map**: Map the information from the source text to the corresponding placeholders. If a placeholder's value is not explicitly stated but can be inferred, infer it. If a value is missing, leave the placeholder as is or use a reasonable default if context implies one.
4.  **Inject**: Replace the placeholders in the template with the extracted values.
5.  **Output**: Return the final string with the injected values.

## Examples

### Example 1
**Input**:
Source: "The meeting is at 2 PM on Friday in Room 101."
Template: "Reminder: Meeting at {time} on {day} in {location}."

**Output**:
"Reminder: Meeting at 2 PM on Friday in Room 101."

### Example 2
**Input**:
Source: "User john_doe signed up with email john@example.com."
Template: "Welcome, {{username}}! We sent a verification link to {{email}}."

**Output**:
"Welcome, john_doe! We sent a verification link to john@example.com."
