---
argument-hint: [course-directory] [optional: card-count]
description: Generate Anki flashcards for memorizing key concepts from a course
allowed-tools: "*"
---

# Create Anki Flashcards: $ARGUMENTS

Generate Anki flashcards for the course to help reinforce key concepts and enable spaced repetition learning.

## Parse Arguments

1. **Extract course directory** from first argument
2. **Check for card count** in second argument (optional)
   - If specified: Use the requested number (e.g., "10", "15", "20-25")
   - If not specified: Generate comprehensive coverage (40-50 cards total)

## Card Count Strategy

### User-Specified Count
If user provides a number:
- Focus on the **most essential** concepts only
- Prioritize fundamental concepts over advanced details
- Create cards that cover the core 80/20 principles
- Distribution: Spread cards across all lessons proportionally

### Default Comprehensive Mode
If no count specified:
- Generate 40-50 total cards for thorough coverage
- Include both fundamental and advanced concepts
- Cover edge cases and best practices
- Distribution: 10-15 cards per lesson

## Anki Deck Creation Process

### Step 1: Analyze Course Content
1. **Read all lesson README.md files** to extract key concepts
2. **Review exercise files** to identify practical patterns
3. **Check cheat sheet** for core concepts and code snippets
4. **Identify learning objectives** from each lesson

### Step 2: Create Deck Structure
1. **Create main deck**: `[Course Topic] - Concepts`
2. **Create subdeck for each lesson**: `[Course Topic] - Lesson N`
3. **Use appropriate card types**:
   - **Basic cards**: For definitions and concept explanations
   - **Cloze deletion**: For code patterns and fill-in-the-blank

### Step 3: Generate Card Types

#### Basic Cards (Front/Back)
- **Concept definitions**: "What is [concept]?" → "Definition and explanation"
- **When to use**: "When should you use [pattern]?" → "Use cases and scenarios"
- **Comparison cards**: "Difference between X and Y?" → "Key distinctions"
- **Best practices**: "What's the best practice for [situation]?" → "Recommended approach"

#### Cloze Deletion Cards
- **Code patterns**: `async def {{c1::function_name}}({{c2::parameters}}):`
- **Syntax**: `await {{c1::asyncio.gather}}({{c2::*tasks}})`
- **Key methods**: `{{c1::asyncio.create_task}}({{c2::coroutine}})`
- **Error handling**: `except {{c1::asyncio.CancelledError}}:`

### Step 4: Content Guidelines

#### Card Content Requirements:
- **Clear and concise** questions and answers
- **Include code examples** where relevant
- **Add context** to make cards memorable
- **Use consistent formatting** across all cards
- **Progressive difficulty** from basic to advanced

#### Example Card Templates:

**Basic Concept Card:**
```
Front: What is the main purpose of async/await in Python?
Back: To enable concurrent execution of I/O-bound operations without blocking the main thread, allowing other tasks to run while waiting for I/O operations to complete.
```

**Code Pattern Card (Cloze):**
```
Text: To run multiple coroutines concurrently, use: {{c1::await asyncio.gather}}({{c2::coro1(), coro2(), coro3()}})
Back Extra: This waits for all coroutines to complete and returns results in order.
```

**Practical Application Card:**
```
Front: When should you use asyncio.wait() instead of asyncio.gather()?
Back: Use asyncio.wait() when you need fine-grained control over task completion, such as processing the first completed task or handling partial results.
```

## Implementation Steps

1. **Read course content** from the specified directory
2. **Extract key concepts** from each lesson
3. **Create Anki deck** with appropriate name
4. **Generate Basic cards** for concepts, definitions, and explanations
5. **Generate Cloze cards** for code patterns and syntax
6. **Add lesson-specific subdecks** for organized study
7. **Batch create all cards** in Anki

## Card Categories by Lesson Type

### Lesson 1 (Fundamentals):
- Basic definitions and concepts
- Core syntax patterns
- When to use vs. when not to use
- Simple code examples

### Lesson 2 (Practical Patterns):
- Coordination patterns (gather, wait, as_completed)
- Error handling approaches
- Timeout management
- Queue patterns

### Lesson 3 (Real-world Applications):
- Best practices and pitfalls
- Performance considerations
- Debugging techniques
- Production patterns

## Quality Standards

### For User-Specified Count (e.g., 10-15 cards total):
- **Focus on essentials**: Only the most critical concepts
- **Higher impact cards**: Each card should teach something fundamental
- **Mix of types**: Still maintain 70% basic, 30% cloze ratio
- **Even distribution**: Spread across lessons proportionally

### For Default Comprehensive Mode:
- **10-15 cards per lesson** (40-50 total)
- **Mix of basic and cloze cards** (70% basic, 30% cloze)
- **Progressive difficulty** within each lesson
- **Cross-reference related concepts** between lessons
- **Include practical examples** from the course exercises

## Success Metrics

After creating the deck:
- Cards should cover **80/20 of key concepts** from the course
- **Spaced repetition** should reinforce learning over time
- Cards should be **answerable** within 10-15 seconds
- **Code examples** should be practical and memorable

## Example Output

### If user requests "15 cards":
Generate exactly **15 high-impact cards**:
- Lesson 1: 5 cards (core fundamentals)
- Lesson 2: 5 cards (essential patterns)  
- Lesson 3: 5 cards (key advanced concepts)

### If no count specified (default):
Generate approximately **40-50 total cards**:
- Lesson 1: 15 cards (comprehensive fundamentals)
- Lesson 2: 18 cards (patterns and practices)  
- Lesson 3: 17 cards (advanced concepts)

The deck will be created in Anki and ready for immediate study to reinforce course learning through spaced repetition.