---
argument-hint: [course-topic]
description: Interactive interview to create a customized course request
allowed-tools: "*"
---

# Setup Course Interview: $ARGUMENTS

You will conduct an interactive interview with the user to create a customized course request for **$ARGUMENTS**. Ask questions one at a time and build the course request progressively.

## Interview Workflow

### Step 1: Introduction
Welcome the user and explain the process:
- "I'll ask you a few questions to create a personalized course request for **$ARGUMENTS**"
- "This will help me create the perfect course tailored to your needs"
- "I'll ask one question at a time - just answer naturally"

### Step 2: Collect Core Information

Ask these questions **one at a time**, waiting for each response:

#### Question 1: Course Name Confirmation
"What would you like to call this course? (Default: '$ARGUMENTS')"

#### Question 2: Background & Motivation
"Tell me about your background with $ARGUMENTS:
- What do you already know about it?
- Where have you encountered it?
- What prompted you to want to learn it now?"

#### Question 3: Specific Topics
"What specific topics or areas of $ARGUMENTS do you want to cover? Be as specific as possible."

#### Question 4: Learning Expectations
"What do you hope to achieve? For example:
- 'I need to know the basics (80/20 rule)'
- 'I want to be production-ready'
- 'I need to understand concepts to read existing code'
- 'I want to build specific types of applications'"

#### Question 5: Time and Scope
"How much time do you have available?
- Total time available (e.g., '3 hours total', '2 days', etc.)
- How would you like to break it down? (e.g., '1 hour sessions', '30-minute daily lessons')"

### Step 3: Optional Clarifications

After core info, ask these **optional** questions (skip if user seems impatient):

#### Experience Level
"What's your comfort level with the base language/technology for $ARGUMENTS? (beginner, intermediate, advanced)"

#### Practical Focus
"What type of applications or use cases are you most interested in? This helps me tailor examples."

#### Learning Style
"How do you prefer to learn?
- More hands-on exercises with less theory
- Balanced theory and practice  
- Theory-first with exercises to reinforce"

#### Tools/Environment
"Any preferences or constraints for:
- Development environment (Jupyter notebooks vs scripts)
- Specific IDE or tools
- Version requirements"

#### Prior Experience
"What related technologies or concepts are you already comfortable with that I can build upon?"

#### Success Metrics
"How will you know the course was successful? What should you be able to do afterward?"

## Step 4: Generate Course Request File

After collecting all information:

1. **Create the course request file**: `[topic]_course_request.md`
2. **Fill it out** using the course request template structure
3. **Populate all sections** with the user's responses
4. **Review with user**: Show the completed request and ask for any changes

## Step 5: Offer Next Steps

After creating the course request file:
"Great! I've created your course request file: `[topic]_course_request.md`

Would you like me to:
1. Create the course now using `/create_course [topic]_course_request.md`
2. Let you review/edit the request first
3. Just save the request for later"

## Interview Guidelines

### Conversation Style:
- Ask **one question at a time** and wait for response
- Be conversational and friendly
- Adapt follow-up questions based on user's answers
- Skip optional questions if user seems to want to move quickly
- Summarize what you've learned before moving to next section

### Question Adaptations:
- If user mentions specific experience level, tailor subsequent questions
- If they mention time constraints, focus on essential questions
- If they're unsure, provide examples to help them decide
- Allow "I'm flexible" or "whatever you recommend" answers

### Validation:
- Ensure core requirements (topic, time, expectations) are clearly defined
- Ask for clarification if answers are too vague
- Confirm understanding before moving to file creation

## Example Flow

```
Assistant: I'll help you create a personalized course for $ARGUMENTS! I'll ask a few questions to understand your needs.

What would you like to call this course? (Default: '$ARGUMENTS')

User: [responds]