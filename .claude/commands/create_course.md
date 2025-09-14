---
argument-hint: [path-to-filled-course-request]
description: Create a complete educational course based on a filled course request file
allowed-tools: "*"
---

# Create Educational Course: $ARGUMENTS

You are tasked with creating a comprehensive educational course based on the course request file at **$ARGUMENTS**. Follow the course creation workflow defined in CLAUDE.md.

## Step 1: Read Course Request

**MANDATORY**: First, read the course request file to understand user requirements:
1. **Read the course request file** at `$ARGUMENTS`
2. **Extract key information**:
   - Course topic and name
   - User's background and experience level
   - Specific topics to cover
   - Time allocation and lesson breakdown
   - Learning style preferences
   - Success metrics and expectations
3. **Use this information** to tailor the course structure and content

## Research Phase (CRITICAL - Do After Reading Course Request)

**MANDATORY**: After reading the course request, research the latest information about the topic:

1. **WebSearch**: Search for "[course-topic] 2024 latest version best practices tutorial"
2. **Context7**: If it's a library/framework, use:
   - `mcp__context7__resolve-library-id` with the course topic
   - `mcp__context7__get-library-docs` with the resolved library ID
3. **Verify current versions**, recent changes, and modern best practices

## Course Specification

Create a course following the requirements from the course request file:
- **Duration**: Use time allocation specified in course request
- **Target**: Match expectations specified in course request (80/20, production-ready, etc.)
- **Structure**: Break into lessons based on requested time breakdown
- **Format**: Use learning style preference from course request
- **Experience Level**: Tailor content to user's stated background and experience

## Content Requirements

This is a purely educational project - focus on teaching concepts clearly rather than production-ready code.

### Course Structure
Typically a topic should be broken down into lessons, reflected in the file structure.

### Lesson Structure
Each lesson must include:
- `README.md` with theory and concepts (10-15 minute read)
  - Brief and targeted content that can be read and understood in 10-15min
  - Include mermaid diagrams whenever possible and meaningful to make concepts more digestible
- Practical exercises file (`.py`, `.ipynb`, or instructions as appropriate)
  - Good mix of explaining and exercises
  - Use jupyter notebooks, scripts, or implementation instructions - whatever is most suitable for teaching the topic
  - Add TODO(human) sections for interactive learning

### Exercise Guidelines
- Use realistic, practical examples
- Progress from basic to advanced concepts
- Include proper error handling examples
- Add timing estimates for each exercise
- Balance theory with hands-on practice

## Environment Setup Requirements

Every course must include proper environment setup instructions:

### Required Files:
- **SETUP.md** - Complete environment setup guide
- **requirements.txt** (Python) / **package.json** (Node) / **go.mod** (Go) / etc. - Dependencies file
- **Verification script** - Test that environment is working correctly

### Setup Guide Must Include:
1. **Prerequisites** - Language version, system requirements
2. **Installation steps** - Step-by-step setup process
3. **Virtual environment** - Isolated development environment
4. **Dependency installation** - Package manager commands
5. **Verification** - Test script to confirm setup works
6. **Troubleshooting** - Common issues and solutions
7. **IDE setup** - Optional but helpful development environment configuration
8. **Alternative methods** - Docker, conda, or other setup approaches

### Technology-Specific Examples:

#### Python Courses:
- requirements.txt with pinned versions
- Virtual environment setup (venv/conda)
- Python version requirements (3.8+, 3.10+, etc.)
- Jupyter setup for interactive courses

#### Node.js Courses:
- package.json with exact versions
- Node version specification (.nvmrc)
- npm/yarn/pnpm setup instructions

#### Go Courses:
- go.mod with module dependencies
- Go version requirements
- Environment variables (GOPATH, etc.)

#### Docker-based Courses:
- Dockerfile for consistent environment
- docker-compose.yml for multi-service setups
- Port mappings and volume configurations

#### System-level Courses:
- OS-specific instructions (macOS/Linux/Windows)
- Package manager commands (homebrew, apt, choco)
- System dependencies and tools

## Implementation Steps

1. **Create course directory**: `[topic]-course/`
2. **Create environment setup** (see requirements above)
3. **Generate lessons** based on time breakdown from course request
4. **Create solutions directory** with complete implementations for each lesson
5. **Generate cheat sheet** - summary, cheat-sheet style document with core concepts, code snippets, etc. that helps during lessons and serves as a reference later

## Quality Standards

- Verify all code examples work with current versions
- Include proper imports and dependencies
- Add clear learning objectives for each lesson
- Provide comprehensive solutions
- Create practical, memorable examples

## Clarifying Questions

If the course topic is ambiguous, ask these questions:
- What's your experience level with related technologies?
- Are there specific use cases or applications you're interested in?
- Do you prefer more hands-on practice or balanced theory/practice?
- Any version or tool constraints?

## Deliverables

Generate a complete course including:
- 3 lesson directories with content
- Complete solutions for all exercises
- Comprehensive cheat sheet
- Updated README for the course

Begin by reading the course request file at **$ARGUMENTS**, then research the latest information about the course topic, and proceed with course creation based on the user's specific requirements.