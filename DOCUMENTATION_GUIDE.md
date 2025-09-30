# Documentation Guide - Project Structure & Standards

This guide defines the documentation structure and standards for this project, designed to be transferable to other projects.

## Documentation Structure

### Root-Level Files (Required)
```
/project-root/
├── README.md          # Project gateway - setup, commands, navigation
├── ARCHITECTURE.md    # System overview with links to detailed docs
├── TESTS.md          # Testing strategy and QA framework
├── CI_CD.md          # Build and deployment processes
├── PRD.md            # Product requirements (if applicable)
├── CLAUDE.md         # AI assistant guidance (if using AI development)
└── CHANGELOG.md      # Version history and release notes
```

### `/docs/` Folder Structure
```
docs/
├── common/
│   ├── file-tree.md     # ⭐ ESSENTIAL: Complete project structure
│   └── guidelines.md    # Development guidelines
├── frontend/
│   ├── overview.md      # React/Vue/Angular architecture
│   └── components.md    # Component patterns
├── backend/
│   ├── overview.md      # API design and server logic
│   └── api.md          # Detailed API documentation
├── database/
│   ├── overview.md      # Database architecture
│   └── schema.md       # Schema documentation
└── design/
    ├── overview.md      # Design system principles
    └── components.md    # UI component specs
```

## What Goes in Each File

### README.md - Project Gateway
**Purpose**: First contact point for all users and developers.

**Must Include**:
- **Project description** (2-3 sentences)
- **Quick Start** section with setup commands
- **Tech Stack** overview with versions
- **Documentation navigation** with links to specialized docs:
  ```markdown
  ## Documentation
  - **[Architecture Overview](ARCHITECTURE.md)** - System design
  - **[Frontend Guide](docs/frontend/overview.md)** - React patterns
  - **[Backend Guide](docs/backend/overview.md)** - API design
  - **[Database Guide](docs/database/overview.md)** - Schema design
  - **[Project Structure](docs/common/file-tree.md)** - File organization
  ```
- **Key Commands** (dev, build, test, lint etc)
- **Development guidelines** (critical requirements)

**Update When**: Major features, tech stack changes, or setup changes

### ARCHITECTURE.md - System Navigation Hub
**Purpose**: High-level system overview with navigation to detailed docs.

**Must Include**:
- **Quick Navigation** section linking to all domain docs
- **System Overview** with ASCII diagram
- **Technology Stack** breakdown
- **Core Features** architecture (main systems)

### docs/common/file-tree.md - Project Structure Reference
**Purpose**: **MOST IMPORTANT** - Complete reference for project structure and file organization.

**Must Include**:
- **Navigation structure** (menu items, routes)
- **Folder organization rules** (where to place new files)
- **All main pages** with file paths, routes, and status

**Critical**: Update **immediately** when:
- Adding/removing pages or components
- Changing navigation or routes
- Moving/renaming files or directories

### Domain Overview Files (docs/frontend/overview.md, etc.)
**Must Include**:
- **Technology Stack** for the domain
- **Architecture Patterns** with code examples
- **Key Components/Features**
- **Development Guidelines**
- **Related Documentation** links

## File Linking & Navigation

### Linking Hierarchy
```
README.md (Gateway)
├── ARCHITECTURE.md → docs/domain/overview.md
├── docs/common/file-tree.md (Essential Reference)
└── Other root docs (TESTS.md, CI_CD.md, etc.)
```

### Link Maintenance Rules
1. **Always update README.md** when adding new docs to `/docs/` folder
2. **Update file-tree.md immediately** when adding/moving/renaming files
3. **Use relative links** for internal documentation: `[Frontend](docs/frontend/overview.md)`
4. **Test all links** when making structural changes

## Maintenance Procedures

### When to Update Documentation

| Trigger | Files to Update | Who Updates |
|---------|----------------|-------------|
| **New page/component** | file-tree.md, relevant overview.md | Developer |
| **Navigation changes** | README.md, file-tree.md | Developer |
| **Major feature** | README.md, ARCHITECTURE.md, domain overview | Tech Lead |
| **Tech stack change** | README.md, ARCHITECTURE.md, domain overview | Tech Lead |
| **File/directory move** | ALL affected links, file-tree.md | Developer |
| **Release** | CHANGELOG.md | Release Manager |

### Update Process
1. **Make the code change**
2. **Update file-tree.md immediately** (if structural change)
3. **Update relevant overview files** (if feature change)
4. **Check README.md navigation** (if new documentation)
5. **Test all related links**


## File Naming Conventions
- **Root files**: UPPERCASE.md (`README.md`, `ARCHITECTURE.md`)
- **Domain directories**: lowercase (`frontend/`, `backend/`)
- **Domain files**: lowercase.md (`overview.md`, `components.md`)

This structure scales from small projects to large systems while maintaining discoverability and ensuring documentation stays current with the codebase.