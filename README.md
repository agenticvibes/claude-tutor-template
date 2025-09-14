# Claude Tutor Template

A comprehensive template for creating educational courses on any technology topic using claude code.
Specify what you would like to explore and claude will generte a short course according to your specifications.

## Quick Start

### Option 1: Interactive Setup (Recommended)

```bash
# Claude Code will interview you to create a customized course request
/setup_course [your-topic]

# Examples:
/setup_course react-hooks
/setup_course golang-basics
/setup_course docker-containers

# Then create the course from your customized request
/create_course [your-topic]_course_request.md

# Optional: Add flashcards for spaced repetition learning
/create_anki_deck [course-directory]                    # Default: 40-50 cards
/create_anki_deck [course-directory] 15                 # Custom: exactly 15 cards
/create_anki_deck [course-directory] 10-20              # Custom: 10-20 cards

# Get feedback on your exercise solutions
/review_exercise [path-to-your-exercise-file]
```

### Option 2: Manual Course Creation

1. **Fill out a course request**:

   ```bash
   cp course_request_template.md my_course_request.md
   # Edit my_course_request.md with your specific requirements
   ```

2. **Create the course**:

   ```bash
   /create_course my_course_request.md
   ```

## What You Get

A complete course structure including:

- **Environment setup guide** with dependencies and verification
- **Progressive lessons** based on your time allocation (e.g., 3 hours, 5 hours, 2 days)
- **Hands-on exercises** with TODO(human) sections for active learning
- **Complete solutions** for all exercises
- **Comprehensive cheat sheet** for quick reference
- **Mermaid diagrams** for complex concepts
- **Optional Anki flashcards** for spaced repetition (separate command)

## Template Files

- `course_request_template.md` - Generic template for any course topic
- `CLAUDE.md` - Instructions for Claude Code integration
- `.claude/commands/setup_course.md` - Interactive interview to create course request
- `.claude/commands/create_course.md` - Custom slash command for course creation
- `.claude/commands/create_anki_deck.md` - Custom slash command for flashcard generation
- `.claude/commands/review_exercise.md` - Custom slash command for exercise feedback and grading
- `examples/course_request.md` - Example filled course request (async Python)

## Features

✅ **Always Up-to-Date**: Courses research latest versions and best practices  
✅ **Interactive Setup**: Interview-based course customization  
✅ **Interactive Learning**: TODO(human) sections for hands-on practice  
✅ **Progressive Structure**: Build from basics to real-world projects  
✅ **80/20 Focus**: Core concepts that cover most practical use cases  
✅ **Visual Learning**: Mermaid diagrams for complex concepts  
✅ **Complete Solutions**: Full implementations for reference  
✅ **Exercise Feedback**: Detailed code reviews with grades (x/10)  
✅ **Optional Flashcards**: Anki integration for spaced repetition learning  

## Course Structure

```text
[topic]-course/
├── SETUP.md                   # Environment setup guide
├── requirements.txt           # Dependencies (language-specific)
├── test_setup.py             # Environment verification
├── lesson1/
│   ├── README.md             # Theory content
│   └── exercises.[py|ipynb]  # Practice exercises
├── lesson2/
│   ├── README.md
│   └── exercises.[py|ipynb]
├── lesson[N]/                # Number of lessons based on your time
│   ├── README.md             # (e.g., 3 lessons for 3 hours,
│   └── project.[py|ipynb]    #        5 lessons for 5 hours)
├── solutions/
│   ├── lesson1_solutions.py
│   ├── lesson2_solutions.py
│   └── lesson[N]_solutions.py
└── [topic]_cheatsheet.md     # Quick reference
```

## Usage Tips

1. **Clone this template** for each new learning project
2. **Always research first**: Template ensures courses use latest information
3. **Customize for your level**: Specify experience level in course request
4. **Practice actively**: Complete TODO(human) sections for best learning
5. **Use flashcards**: Run `/create_anki_deck` for spaced repetition
6. **Keep cheat sheet handy**: Perfect for quick lookups during real work

## Getting Started

1. **Clone this repository**:

   ```bash
   git clone [your-repo-url] my-learning-project
   cd my-learning-project
   ```

2. **Setup your course**:

   ```bash
   # Interactive interview to create course request
   /setup_course [topic-you-want-to-learn]
   
   # Then create the course
   /create_course [topic]_course_request.md
   ```

3. **Optional - Add flashcards**:

   ```bash
   # Default comprehensive deck (40-50 cards)
   /create_anki_deck [generated-course-directory]
   
   # Or specify exact count for essential concepts only
   /create_anki_deck [generated-course-directory] 15
   ```

4. **Get feedback on exercises**:

   ```bash
   /review_exercise [path-to-your-completed-exercise]
   ```

## Examples

The `examples/` directory contains filled course requests demonstrating how to use the template for different learning scenarios.

---

**Ready to learn something new?** Clone this template and try `/setup_course [your-topic]` in Claude Code!
