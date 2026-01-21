![https---dev-to-uploads s3 amazonaws com-uploads-articles-dpcjtoy18f7zi8t8f82m png](https://github.com/user-attachments/assets/9dda6727-00f2-4173-ae27-a0e47bf41320)

# SwiftUI Best Practices Agent Skill

Expert guidance for any AI coding tool that supports the [Agent Skills open format](https://agentskills.io/home) — clean architecture, optimal performance, and proper state management in SwiftUI.

Actionable, concise references for AI agents covering SwiftUI data flow, view composition, and performance optimization patterns.

## Who this is for
- Teams building SwiftUI applications who need reliable patterns and best practices.
- Developers struggling with state management, property wrappers, or view performance issues.
- Anyone wanting to write clean, performant SwiftUI code with proper data flow patterns.

## How to Use This Skill

### Option A: Using OpenSkills (recommended)
1) Install OpenSkills:
   ```bash
   npm i -g openskills
   ```
2) `cd` into your project directory.
3) Install this skill:
   ```bash
   openskills install AvdLee/SwiftUI-Best-Practices-Agent-Skill
   ```
4) Sync into your `AGENTS.md`:
   ```bash
   openskills sync
   ```
5) Use the skill in your AI agent, for example:
   > Use the swiftui best practices skill and review the current project for SwiftUI improvements

### Option B: Claude Code Plugin

#### Personal Usage

To install this Skill for your personal use in Claude Code:

1. Add the marketplace:
   ```bash
   /plugin marketplace add AvdLee/SwiftUI-Best-Practices-Agent-Skill
   ```

2. Install the Skill:
   ```bash
   /plugin install swiftui-best-practices@swiftui-best-practices-agent-skill
   ```

#### Project Configuration

To automatically provide this Skill to everyone working in a repository, configure the repository's `.claude/settings.json`:

```json
{
  "enabledPlugins": {
    "swiftui-best-practices@swiftui-best-practices-agent-skill": true
  },
  "extraKnownMarketplaces": {
    "swiftui-best-practices-agent-skill": {
      "source": {
        "source": "github",
        "repo": "AvdLee/SwiftUI-Best-Practices-Agent-Skill"
      }
    }
  }
}
```

When team members open the project, Claude Code will prompt them to install the Skill.

### Option C: Manual install
1) **Clone** this repository.
2) **Install or symlink** the skill file following your tool's official skills installation docs (see links below).
3) **Use your AI tool** as usual and ask it to use the "swiftui-best-practices" skill for SwiftUI tasks.

#### Where to Save Skills

Follow your tool's official documentation, here are a few popular ones:
- **Codex:** [Where to save skills](https://developers.openai.com/codex/skills/#where-to-save-skills)
- **Claude:** [Using Skills](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview#using-skills)
- **Cursor:** [Enabling Skills](https://cursor.com/docs/context/skills#enabling-skills)

**How to verify**:

Your agent should reference the best practices in `swiftui-best-practices.md` and apply them when writing or reviewing SwiftUI code.

## What This Skill Offers

This skill gives your AI coding tool comprehensive SwiftUI guidance. It can:

### Guide Your State Management Decisions
- Choose the right property wrapper for every situation (`@State`, `@Binding`, `@StateObject`, `@ObservedObject`, `@Bindable`)
- Understand when to use `let` vs `var` for passed values
- Navigate iOS 17+ `@Observable` patterns correctly
- Apply proper ownership semantics for observable objects

### Write Clean View Architecture
- Extract subviews properly for better performance and readability
- Understand when `@ViewBuilder` functions are appropriate vs separate structs
- Follow the 100-line rule for view extraction
- Structure parent-child relationships correctly

### Optimize SwiftUI Performance
- Avoid redundant state updates that trigger unnecessary re-renders
- Use proper content property patterns (avoiding closure-based content)
- Optimize hot paths like scroll handlers and preference changes
- Minimize view body re-executions through proper composition

### Review Code Effectively
- Apply a comprehensive checklist for SwiftUI code review
- Identify common anti-patterns and their solutions
- Ensure consistent best practices across your codebase

## What Makes This Skill Different

**Practical Focus**: Covers the most common SwiftUI patterns and pitfalls developers encounter daily, with clear code examples for every pattern.

**Non-Opinionated**: Focuses on Apple's recommended patterns and performance best practices, not architectural preferences. Works with any SwiftUI project structure.

**iOS 17+ Ready**: Includes modern patterns for `@Observable` and `@Bindable`, alongside pre-iOS 17 patterns for broader compatibility.

**Performance-Minded**: Emphasizes view composition and state management patterns that prevent unnecessary re-renders and keep your app responsive.

**Concise & Actionable**: Assumes your AI agent is already smart. Focuses on what developers need to know with direct comparisons of good vs bad patterns.

## Skill Structure

```
skills/
└── swiftui-best-practices.md       # Main skill file with best practices
    ├── Data Flow and State Management
    │   ├── Property Wrapper Selection Guide
    │   ├── @State Rules
    │   ├── @Binding Rules
    │   ├── @StateObject vs @ObservedObject
    │   ├── @Bindable (iOS 17+)
    │   └── let vs var for Passed Values
    ├── View Structure and Composition
    │   ├── Extract Subviews, Not Computed Properties
    │   ├── When to Use @ViewBuilder Functions
    │   └── Rule of Thumb
    ├── Performance Optimization
    │   ├── Avoid Redundant State Updates
    │   ├── Avoid Closure-Based Content Properties
    │   └── Optimize Hot Paths
    └── Quick Reference Checklist
```

## Contributing

Found an issue or have a suggestion? Feel free to open a PR. This skill is maintained to reflect the latest SwiftUI best practices and will be updated as the framework evolves.

## About the Authors

Created by [Omar Elsayed](https://www.swiftdifferently.com/about) and [Antoine van der Lee](https://www.avanderlee.com). 
Antoine is a Swift expert and creator of the [Swift Concurrency Course](https://www.swiftconcurrencycourse.com) with years of experience in Swift development. 
He has [published numerous articles on Swift](https://www.avanderlee.com) on his blog called SwiftLee.

## License

This skill is open-source and available under the MIT License. See [LICENSE](LICENSE) for details.
