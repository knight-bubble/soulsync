# SoulSync Repository Instructions

**ALWAYS follow these instructions first before attempting any other actions. Only fallback to additional search and context gathering if the information in these instructions is incomplete or found to be in error.**

## Current Repository State

SoulSync is currently a fresh repository containing only a LICENSE file. This is a greenfield project ready for initial development.

**CRITICAL**: Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Current Repository Contents
- **Verified working commands:**
  - `ls -la` - Shows only LICENSE file and .git directory
  - `git status` - Shows clean working directory
  - `git log --oneline` - Shows minimal commit history

### Repository Setup (Current State)
- Clone the repository: `git clone https://github.com/knight-bubble/soulsync.git`
- Navigate to directory: `cd soulsync`
- Current structure contains:
  ```
  .
  ├── .git/
  ├── .github/
  │   └── copilot-instructions.md
  └── LICENSE
  ```

### Development Environment Preparation
**Since this is a greenfield project, determine the technology stack first before proceeding with setup.**

Common setup patterns to validate and implement based on project requirements:

#### For Node.js/JavaScript Projects:
- Initialize package.json: `npm init -y`
- Install dependencies: `npm install`
- Build command: `npm run build` (define in package.json scripts)
- Test command: `npm test` (define in package.json scripts)
- Development server: `npm run dev` (define in package.json scripts)

#### For Python Projects:
- Create virtual environment: `python -m venv venv`
- Activate environment: `source venv/bin/activate` (Linux/Mac) or `venv\Scripts\activate` (Windows)
- Install dependencies: `pip install -r requirements.txt`
- Run tests: `python -m pytest`

#### For Go Projects:
- Initialize module: `go mod init github.com/knight-bubble/soulsync`
- Install dependencies: `go mod tidy`
- Build: `go build`
- Test: `go test ./...`
- Run: `go run main.go`

#### For Rust Projects:
- Initialize project: `cargo init`
- Build: `cargo build`
- Test: `cargo test`
- Run: `cargo run`

### Build and Test Guidelines

**CRITICAL TIMING EXPECTATIONS:**
- **NEVER CANCEL** any build or test commands
- Set timeouts to **minimum 60 minutes** for build commands
- Set timeouts to **minimum 30 minutes** for test commands
- Even if commands appear to hang, wait **at least 60 minutes** before considering alternatives

**Build Validation Process:**
1. Always run the complete build process after making changes
2. **NEVER CANCEL** builds even if they take 45+ minutes
3. Document actual build times and add 50% buffer for timeout recommendations
4. If build fails, fix issues before proceeding

**Test Validation Process:**
1. Always run the full test suite after changes
2. **NEVER CANCEL** tests even if they take 15+ minutes  
3. Create focused tests for new functionality
4. Ensure all tests pass before committing

### Validation Requirements

**MANUAL VALIDATION REQUIREMENT:**
- After building and running the application, **MUST** test actual functionality through complete user scenarios
- Simply starting and stopping the application is **NOT** sufficient validation
- Execute real workflows that a user would perform
- Take screenshots of UI changes when applicable
- Test CLI applications with actual command sequences

### Future Development Guidance

**When adding the first code to this repository:**
1. Determine and document the technology stack
2. Create appropriate project structure
3. Add build and test configurations
4. Update these instructions with specific commands
5. Validate all new commands work correctly

**Key Files to Create:**
- README.md - Project overview and quick start
- CONTRIBUTING.md - Development guidelines
- Project-specific configuration files (package.json, requirements.txt, etc.)
- Build scripts and configuration
- Test configuration
- CI/CD pipeline configuration (.github/workflows/)

### Linting and Code Quality

**Before committing any changes:**
- Implement and run appropriate linters for the chosen technology
- Format code using standard formatters
- Run security scans if applicable
- Ensure all quality checks pass

**Common linting patterns by technology:**
- Node.js: `npm run lint`, `npm run format` (ESLint, Prettier)
- Python: `flake8`, `black`, `isort`
- Go: `go fmt`, `golint`, `go vet`
- Rust: `cargo fmt`, `cargo clippy`

### Repository Navigation

**Current Important Locations:**
- Root directory: Basic project setup
- .github/: Repository configuration and this instructions file
- LICENSE: MIT license terms

**Future Important Locations (to be created):**
- src/: Source code (typical location)
- docs/: Documentation
- tests/: Test files
- scripts/: Build and utility scripts
- config/: Configuration files

### Common Tasks

**Repository Status Check:**
```bash
git status
git log --oneline -5
ls -la
```

**Initial Development Setup:**
1. Determine technology stack based on project requirements
2. Create basic project structure
3. Initialize build system
4. Create initial tests
5. Set up CI/CD pipeline
6. Update these instructions with validated commands

### Critical Reminders

- **NEVER CANCEL** long-running builds or tests
- **ALWAYS** validate commands before including in code
- **ALWAYS** test complete user scenarios after changes
- **ALWAYS** run linting and formatting before commits
- **ALWAYS** update these instructions when adding new workflows
- Set appropriate timeouts (60+ minutes for builds, 30+ minutes for tests)

### Error Handling

**If commands fail:**
1. Document the failure in these instructions
2. Provide working alternatives
3. Include specific error messages and solutions
4. Example: "npm install fails due to firewall limitations - use npm install --registry=http://internal-registry"

**Build Troubleshooting:**
1. Check all prerequisites are installed
2. Verify correct working directory
3. Check for conflicting processes
4. Wait full timeout period before declaring failure
5. Document solutions for future reference

---

**Last Updated:** Current as of repository creation
**Technology Stack:** To be determined
**Build Status:** No build system implemented yet