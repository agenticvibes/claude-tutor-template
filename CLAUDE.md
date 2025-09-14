# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a course template project for creating educational content. The repository contains:
- Course request templates and examples
- Course creation guidelines and workflows
- Custom slash commands for automated course generation

## Key Files

- `course_request_template.md` - Generic template for any course topic
- `.claude/commands/setup_course.md` - Interactive interview to create course request
- `.claude/commands/create_course.md` - Custom slash command for automated course creation
- `.claude/commands/create_anki_deck.md` - Custom slash command for flashcard generation
- `.claude/commands/review_exercise.md` - Custom slash command for exercise feedback
- `examples/course_request.md` - Example filled course request (async Python)

## Research Requirements

**IMPORTANT**: Before creating any course content, always:

1. **Use WebSearch** to find the latest information about the technology/topic
2. **Use Context7 MCP server** (`mcp__context7__resolve-library-id` then `mcp__context7__get-library-docs`) to get up-to-date library documentation
3. **Verify version compatibility** and current best practices
4. **Check for recent changes** in APIs, syntax, or recommended patterns

This ensures courses are based on current, not outdated, information.

## Course Creation Workflow

### Using the Custom Slash Commands

#### Setup Course Request (Interactive):
```
/setup_course [course-topic]
```

This command will:
1. Interview you about your learning needs
2. Ask questions one at a time
3. Create a customized course request file
4. Prepare for course creation

#### Create a Complete Course:
```
/create_course [path-to-filled-course-request]
```

This command will:
1. Read your course request file
2. Research latest information about the topic
3. Generate complete course structure with lessons, exercises, and solutions
4. Create a topic-specific cheat sheet

#### Add Flashcards (Optional):
```
/create_anki_deck [course-directory]              # Default: 40-50 cards
/create_anki_deck [course-directory] 15           # Custom: exactly 15 essential cards
```

This command will:
1. Analyze course content to extract key concepts
2. Create an Anki deck with specified number of flashcards (or 40-50 default)
3. Generate mix of Basic and Cloze deletion cards
4. Tag cards by lesson for organized study

#### Review Exercise Solutions:
```
/review_exercise [path-to-exercise-file]
```

This command will:
1. Analyze your completed exercise
2. Provide detailed feedback and suggestions
3. Grade your work (x/10) with breakdown
4. Identify areas for improvement

### Manual Course Creation

If creating courses manually:

1. **Setup Phase**
   - Copy and fill out course_request_template.md with your requirements
   - Or use `/setup_course [topic]` for interactive setup

2. **Research Phase**
   - Use WebSearch for latest trends and best practices
   - Use Context7 for official documentation
   - Identify current version and breaking changes

3. **Content Creation**
   - Run `/create_course [your-course-request.md]`
   - Course will be generated with:
     - Lesson directories (lesson1/, lesson2/, etc.)
     - README.md for theory (10-15 min read)
     - Practical exercises (scripts or Jupyter notebooks)
     - Progressive complexity
     - Complete solutions
     - Comprehensive cheat sheet

4. **Learning & Review**
   - Work through exercises
   - Use `/review_exercise [your-solution]` for feedback
   - Optional: `/create_anki_deck [course-directory]` for flashcards

## File Organization Standards

### Course Structure
```
[course-name]/
├── SETUP.md                   # Environment setup guide
├── requirements.txt           # Dependencies (Python example)
├── lesson1/
│   ├── README.md             # Theory content
│   └── exercises.[py|ipynb]  # Hands-on practice
├── lesson2/
│   ├── README.md
│   └── exercises.[py|ipynb]
├── lesson[N]/                # Number of lessons based on time allocation
│   ├── README.md             # (e.g., 3 lessons for 3 hours,
│   └── project.[py|ipynb]    #        5 lessons for 5 hours, etc.)
├── solutions/
│   ├── lesson1_solutions.py
│   ├── lesson2_solutions.py
│   └── lesson[N]_solutions.py
└── [topic]_cheatsheet.md      # Quick reference
```

### Content Guidelines
- Lesson duration based on user's time allocation in course request
- Include mermaid diagrams for complex concepts
- Use TODO(human) markers for interactive learning
- Balance theory with practical application
- Focus on 80/20 principle (core concepts that cover most use cases)

## Common Tasks

### Research Latest Information
```bash
# Example workflow
1. WebSearch: "[technology] 2025 latest version best practices"
2. Context7: mcp__context7__resolve-library-id + get-library-docs
3. Check official docs and changelog
```

### Create New Course
```bash
# Interactive setup (recommended)
/setup_course react-hooks

# Then create the course
/create_course react-hooks_course_request.md

# Review your exercise solutions
/review_exercise react-hooks-course/lesson1/exercises.py

# Optionally add flashcards
/create_anki_deck react-hooks-course
```

### Update Existing Course
- Always check for technology updates first
- Update examples to use current versions
- Verify all code still works
- Update cheat sheet with new patterns