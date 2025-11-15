# 🤖 AI Agent Instructions

This document contains instructions and guidelines for AI agents working on the CRM Team Dashboard project.

## 📊 Reporting System

The project uses a structured reporting system to track all changes and improvements. There are two types of reports:

### MI Reports (Maintenance Incidents)
- **Location**: `mi-reports/`
- **Purpose**: Track bugs, fixes, and maintenance tasks
- **Naming Convention**: `MI-YYYY-XXX-[description].md`
- **Template**: Use existing reports like `MI-2024-001-delete-member-bug.md` as examples
- **Status Values**: IDENTIFIED, IN_PROGRESS, RESOLVED, DEPLOYED

### Upgrade Reports (Feature Enhancements)
- **Location**: `upgrade-reports/`
- **Purpose**: Track feature upgrades, improvements, and new functionality
- **Naming Convention**: `UG-YYYY-XXX-[description].md`
- **Template**: Use `upgrade-reports/TEMPLATE.md` for new reports
- **Status Values**: PROPOSED, IN_PROGRESS, COMPLETED, CANCELLED

## 🔧 When to Create Reports

### Create MI Reports When:
- **Bug Fixes**: Correcting errors or unexpected behavior
- **Performance Issues**: Addressing slow performance or memory leaks
- **Security Vulnerabilities**: Fixing security holes or vulnerabilities
- **Code Maintenance**: Refactoring, cleanup, or dependency updates
- **Data Issues**: Fixing data corruption or storage problems
- **UI/UX Bugs**: Fixing layout, styling, or interaction issues

### Create Upgrade Reports When:
- **New Features**: Implementing completely new functionality
- **UI/UX Improvements**: Enhancing user interface or experience
- **Performance Enhancements**: Optimizing speed, efficiency, or resource usage
- **User-Requested Features**: Implementing features requested by stakeholders
- **Integration**: Adding new integrations or connections
- **Accessibility**: Improving accessibility features

## 📝 Report Creation Process

### Step 1: Identify Report Type
Determine if the work is a **maintenance incident** (fixing something broken) or an **upgrade** (adding something new).

### Step 2: Create Report File
- Use appropriate naming convention
- Place in correct directory (`mi-reports/` or `upgrade-reports/`)
- Use existing template or similar report as starting point

### Step 3: Fill Report Sections
Complete all required sections:
- Executive Summary
- Technical Details
- Action Plan
- Success Criteria
- Testing Strategy
- Implementation Checklist

### Step 4: Update Status Progress
- Set initial status appropriately
- Update status as work progresses
- Complete checklist items as tasks are finished

## 🎯 Working Guidelines

### Before Making Changes
1. **Read Existing Reports**: Review similar reports for context
2. **Understand Codebase**: Examine relevant code sections
3. **Check Dependencies**: Identify any dependencies or impacts
4. **Plan Approach**: Create clear implementation strategy

### During Implementation
1. **Follow Patterns**: Use existing code patterns and conventions
2. **Update Report**: Document progress in real-time
3. **Test Thoroughly**: Verify functionality works as expected
4. **Document Changes**: Update code comments and documentation

### After Implementation
1. **Complete Report**: Finalize all report sections
2. **Update Status**: Set appropriate final status
3. **Verify Integration**: Ensure changes work with existing features
4. **Clean Up**: Remove any temporary code or files

## 📁 File Structure Context

```
gemini-agent-dashboard/
├── index.html                 # Main application file
├── README.md                  # Project documentation
├── agents.md                  # This file - AI agent instructions
├── mi-reports/               # Maintenance incident reports
│   └── MI-YYYY-XXX-[desc].md
└── upgrade-reports/          # Upgrade feature reports
    ├── README.md             # Upgrade reports documentation
    ├── TEMPLATE.md           # Upgrade report template
    └── UG-YYYY-XXX-[desc].md
```

## 🛠️ Technical Context

### Application Architecture
- **Single Page Application**: All code in `index.html`
- **Vanilla JavaScript**: No frameworks, pure JS implementation
- **Tailwind CSS**: Utility-first CSS framework via CDN
- **LocalStorage**: Client-side data persistence
- **Component-Based**: Modular functions for UI components

### Key Code Patterns
- **Data Management**: CRUD operations with `teamData` array
- **Modal System**: Reusable modal infrastructure
- **Event Handling**: Delegated event listeners for dynamic content
- **Rendering Functions**: Separate functions for different UI components
- **Utility Functions**: Helper functions for time calculations, formatting

### Common Tasks
- **Adding New Metrics**: Update `BLANK_AGENT` object and rendering functions
- **Modifying UI**: Update HTML templates and CSS classes
- **Adding Features**: Create new modal modes and corresponding handlers
- **Fixing Bugs**: Identify root cause and implement targeted fixes

## 📋 Quality Standards

### Code Quality
- **Clear Naming**: Use descriptive function and variable names
- **Single Responsibility**: Each function should have one clear purpose
- **Error Handling**: Include try-catch blocks for data operations
- **Comments**: Document complex logic and business rules

### Testing Requirements
- **Functional Testing**: Verify features work as expected
- **Edge Cases**: Test with empty data, maximum values, etc.
- **Browser Compatibility**: Test on target browsers
- **Responsive Design**: Verify mobile and desktop layouts

### Documentation Standards
- **Complete Reports**: Fill all sections in MI/UG reports
- **Clear Descriptions**: Explain technical concepts clearly
- **Update Status**: Keep report status current
- **Track Progress**: Use checklists to track completion

## 🚨 Emergency Procedures

### Critical Bugs
1. **Immediate Action**: Create MI report with HIGH priority
2. **Root Cause**: Identify and document the issue quickly
3. **Fix Implementation**: Apply targeted fix
4. **Testing**: Verify fix resolves issue without side effects
5. **Documentation**: Complete MI report with resolution details

### Feature Requests
1. **Analysis**: Create UG report with detailed proposal
2. **Planning**: Break down into implementation phases
3. **Development**: Implement following technical proposal
4. **Testing**: Comprehensive testing of new functionality
5. **Documentation**: Complete UG report with implementation details

## 📞 Getting Help

### For Questions About:
- **Report Format**: Check existing reports and templates
- **Code Structure**: Review `index.html` and comments
- **Technical Issues**: Examine browser console and error messages
- **Best Practices**: Follow patterns in existing code

### Resources Available:
- **Existing Reports**: Examples in `mi-reports/` and `upgrade-reports/`
- **Code Comments**: Inline documentation in `index.html`
- **README.md**: Project overview and technical details
- **Template Files**: Standardized formats for new reports

---

## 🔄 Workflow Example

### Example: Fixing a Bug
1. **Identify Issue**: User reports delete functionality not working
2. **Create MI Report**: `MI-2024-002-delete-bug-fix.md`
3. **Root Cause Analysis**: Find typo in `handleDeleteMember()` function
4. **Implement Fix**: Correct `fiter` to `filter`
5. **Test**: Verify delete functionality works
6. **Complete Report**: Update status to RESOLVED, complete checklist

### Example: Adding a Feature
1. **User Request**: "I want to export team data to CSV"
2. **Create UG Report**: `UG-2024-002-csv-export.md`
3. **Technical Proposal**: Plan export function implementation
4. **Development**: Add export button and CSV generation
5. **Testing**: Verify export works with various data sets
6. **Complete Report**: Update status to COMPLETED, document usage

## 🤖 Available Specialist Agents

### **CRM Dashboard Specialist**
- **File**: `crm-dashboard-specialist.md`
- **Purpose**: Expert in application design, development, and enhancement
- **Specialization**: Customer support team performance management systems
- **When to Use**: 
  - Feature implementation and enhancement
  - Performance optimization
  - Bug fixes and maintenance
  - UI/UX improvements
  - Code quality improvements
  - Technical guidance and best practices

### **How to Invoke Specialist Agent**
When working on this project, you can reference the CRM Dashboard Specialist for:
- **Architecture Decisions**: Component structure and design patterns
- **Implementation Guidance**: Best practices for new features
- **Code Review**: Quality assessment and improvement suggestions
- **Problem Solving**: Technical challenges and optimization
- **Standards Compliance**: Ensuring consistency with existing patterns

### **GitHub Specialist**
- **File**: `github-specialist.md`
- **Purpose**: Automated Git repository management and PR creation
- **Specialization**: Version control, collaboration workflows, and deployment
- **Automatic Invocation**: Triggered when MI/Upgrade reports are marked complete
- **Core Functions**:
  - Branch creation with proper naming conventions
  - Detailed pull request creation with templates
  - Tag management and release automation
  - Team collaboration and review workflows
  - Repository configuration and protection rules

### **How GitHub Specialist Works**
The GitHub Specialist is **automatically invoked** when:
1. **MI Report Status** changes to `RESOLVED` or `DEPLOYED`
2. **Upgrade Report Status** changes to `COMPLETED`
3. **Implementation Checklist** is fully checked
4. **All testing criteria** are marked as complete

**Automated Actions Performed:**
- Creates feature/fix branches with proper naming
- Stages and commits changes with detailed messages
- Generates comprehensive pull requests with templates
- Adds appropriate labels and assigns reviewers
- Manages tags and releases for deployments

---

*Last Updated: 2025-11-15*  
*Maintained by: AI Development Team*