---
argument-hint: [path-to-exercise-file]
description: Review and grade a completed exercise with detailed feedback
allowed-tools: "*"
---

# Review Exercise: $ARGUMENTS

You are tasked with reviewing a completed exercise file at **$ARGUMENTS** and providing comprehensive feedback with a numerical grade.

## Review Process

### Step 1: Understand Context
1. **Read the exercise file** at `$ARGUMENTS` 
2. **Identify the lesson** it belongs to (check parent directory)
3. **Read the lesson README.md** to understand learning objectives
4. **Check if solutions exist** in the solutions directory for comparison

### Step 2: Code Analysis
Analyze the submitted code for:

#### Functional Correctness (3/10 points)
- Does the code work as intended?
- Are all requirements from the exercise met?
- Does it handle expected inputs correctly?
- Are there any runtime errors or bugs?

#### Code Quality (2/10 points)
- Is the code readable and well-structured?
- Are variable names meaningful and consistent?
- Is the code properly organized and formatted?
- Are functions/classes appropriately sized and focused?

#### Best Practices (2/10 points)
- Does it follow language-specific conventions?
- Are appropriate data structures and algorithms used?
- Is error handling implemented where needed?
- Are there any security or performance concerns?

#### Learning Objectives (2/10 points)
- Does the implementation demonstrate understanding of the lesson concepts?
- Are the key techniques from the lesson properly applied?
- Is the approach aligned with what was taught?

#### Innovation/Extras (1/10 points)
- Any creative or advanced implementations beyond requirements?
- Good use of additional concepts not explicitly required?
- Thoughtful optimizations or improvements?

## Review Report Structure

Generate a comprehensive review report with the following sections:

### 🎯 Overall Grade: X/10

### 📊 Breakdown
- **Functional Correctness**: X/3 - Brief explanation
- **Code Quality**: X/2 - Brief explanation  
- **Best Practices**: X/2 - Brief explanation
- **Learning Objectives**: X/2 - Brief explanation
- **Innovation/Extras**: X/1 - Brief explanation

### ✅ What You Did Well
- List 2-3 specific things that were implemented correctly
- Highlight good practices and techniques used
- Acknowledge creative or thoughtful approaches

### 🔧 Areas for Improvement
- List 2-3 specific areas that could be enhanced
- Provide concrete suggestions for improvement
- Reference best practices or alternative approaches

### 💡 Detailed Feedback

#### Code Review Comments
Go through the code section by section:
- **Lines X-Y**: Specific feedback about this code block
- **Function/Class Name**: Comments about implementation
- **Overall Structure**: Comments about organization

#### Suggestions for Enhancement
- Specific code improvements with examples
- Alternative approaches to consider
- Resources for further learning

### 🎓 Learning Assessment
- Which lesson concepts were demonstrated well?
- Which concepts need more practice?
- Recommended next steps for improvement

### 🚀 Next Steps
Based on the review, suggest:
- Specific areas to focus on in future exercises
- Additional practice recommendations
- Resources for concepts that need reinforcement

## Grading Guidelines

### Grade Ranges:
- **9-10**: Excellent - Exceeds expectations, demonstrates mastery
- **7-8**: Good - Meets expectations with minor areas for improvement  
- **5-6**: Satisfactory - Basic requirements met but significant room for improvement
- **3-4**: Needs Work - Some functionality but major issues present
- **1-2**: Poor - Minimal functionality, fundamental issues
- **0**: Non-functional or not submitted

### Constructive Tone:
- Be encouraging and supportive
- Focus on learning and improvement
- Provide specific, actionable feedback
- Balance criticism with positive reinforcement
- Remember this is educational, not production code

## Special Considerations

### For Beginner Exercises:
- Weight functionality higher than style
- Be more lenient on advanced best practices
- Focus on whether core concepts are understood
- Provide more detailed explanations

### For Advanced Exercises:
- Expect higher code quality standards
- Look for optimization and efficiency
- Assess architectural decisions
- Evaluate error handling and edge cases

### For Different File Types:
- **Python scripts**: Check for PEP 8, proper imports, docstrings
- **Jupyter notebooks**: Review cell organization, markdown explanations, output quality
- **JavaScript**: Check for modern syntax, proper async handling
- **Other languages**: Apply language-specific conventions

## Example Review Output

```
# Exercise Review: async_web_scraper.py

## 🎯 Overall Grade: 7/10

## 📊 Breakdown
- **Functional Correctness**: 3/3 - Code works perfectly, handles all test cases
- **Code Quality**: 1/2 - Some variable names could be clearer
- **Best Practices**: 2/2 - Good async/await usage and error handling
- **Learning Objectives**: 1/2 - Shows understanding but misses some key patterns
- **Innovation/Extras**: 0/1 - Basic implementation, no extras

## ✅ What You Did Well
- Excellent use of async/await syntax
- Proper error handling with try/catch blocks  
- Clean separation of concerns between functions

## 🔧 Areas for Improvement
- Variable names like `data` and `stuff` should be more descriptive
- Could benefit from adding type hints
- Missing docstrings for functions

[... detailed feedback continues ...]
```

Begin by reading the exercise file and understanding its context within the course structure.