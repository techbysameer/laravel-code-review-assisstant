# Laravel Code Review Assistant

A simple, interactive tool to speed up Laravel code reviews with consistent feedback and comprehensive checklists.

## 🚀 Features

- **Framework-Specific Checks**: Laravel best practices, security patterns, and common gotchas
- **Multiple Review Types**: General, Controllers, Models, Security, Testing
- **Interactive Interface**: Click-to-mark status with visual feedback
- **Instant Summary Generation**: Copy-paste ready feedback for PRs
- **Severity Indicators**: High/Medium/Low priority items
- **Custom Notes**: Add specific feedback for issues and improvements
- **Zero Dependencies**: Pure HTML, CSS, and JavaScript

## 📸 Screenshot

![image](https://github.com/user-attachments/assets/f0f61337-8ea1-45f2-9f6b-85de4fbbb917)


## 🎯 Why This Tool?

Code reviews are crucial but can be time-consuming and inconsistent. This tool helps you:

- ✅ **Never miss common Laravel issues** (N+1 queries, mass assignment, CSRF protection)
- ✅ **Maintain consistent review quality** across your team
- ✅ **Speed up the review process** from 30+ minutes to 10 minutes
- ✅ **Generate professional feedback** that's constructive and specific
- ✅ **Focus on what matters** with severity-based prioritization

## 🛠️ Installation

### Option 1: Download and Use Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/laravel-code-review-assistant.git
   ```
2. Open `index.html` in your browser
3. Start reviewing code!

### Option 2: Use Online
Visit the live version: [Laravel Code Review Assistant](https://your-github-pages-url.github.io/laravel-code-review-assistant/)

## 📖 How to Use

### Step 1: Choose Review Focus
Select the type of code you're reviewing:
- **General Laravel** - For any Laravel code
- **Controllers** - When reviewing controller files
- **Models & Database** - For Eloquent models and migrations
- **Security** - Focused security review
- **Testing** - For test files

### Step 2: Review Your Code
Open the Laravel code you want to review alongside this tool. Go through each checklist item:

- ✅ **Green checkmark** = "This looks good in the code"
- ⚠️ **Yellow warning** = "Could be improved"
- 🔴 **Red issue** = "This is a problem"

### Step 3: Add Specific Feedback
When you mark items as warning or issue, add specific notes:
- "Controller has 15 methods - consider splitting"
- "Missing eager loading on line 42: `User::with('posts')`"
- "No CSRF token in contact form"

### Step 4: Generate Review
Click "Copy Summary" to get formatted feedback ready for:
- GitHub PR comments
- GitLab merge request reviews
- Team communication tools
- Internal documentation

## 🔍 What It Checks

### General Laravel (8 items)
- PSR-4 autoloading standards
- Naming conventions
- PHPDoc documentation
- Dependency injection
- Facade usage
- Configuration management
- Exception handling
- Input validation

### Controllers (7 items)
- Single responsibility principle
- Resource controllers
- Form Request classes
- Response methods
- Middleware application
- Fat controller prevention
- Return type declarations

### Models & Database (8 items)
- Mass assignment protection
- Eloquent relationships
- Query scopes
- Accessors/mutators
- N+1 query prevention
- Migration structure
- Database indexes
- Soft deletes

### Security (7 items)
- CSRF protection
- SQL injection prevention
- XSS protection
- Authorization (Gates/Policies)
- File upload security
- Rate limiting
- HTTPS enforcement

### Testing (5 items)
- Feature tests
- Unit tests
- Test database separation
- Model factories
- Test coverage

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Add new check items**: Submit PRs with additional Laravel best practices
2. **Improve the interface**: Enhance UX/UI for better usability
3. **Add new review types**: API reviews, Package reviews, etc.
4. **Bug fixes**: Report issues or submit fixes

### Adding New Check Items

Edit the `reviewData` object in `index.html`:

```javascript
severity_name: {
    name: 'Category Name',
    items: [
        { 
            id: 'unique_id', 
            text: 'Description of what to check', 
            severity: 'high|medium|low' 
        }
    ]
}
```

## 📝 Example Output

```markdown
## Laravel Code Review Summary - Controllers

### 🚨 Issues Found (2)
- **Single responsibility principle followed**: UserController handles both authentication and profile management
- **Controllers not too fat (business logic in services)**: 200+ lines of business logic should be moved to services

### ⚠️ Improvements Suggested (1)
- **Form Request classes for complex validation**: Consider using FormRequest for the registration validation

### ✅ Good Practices Found (4)
- Resource controllers used where appropriate
- Proper response methods (json, view, redirect)
- Middleware applied correctly
- Consistent return types declared
```

## 🎨 Customization

### Styling
Modify the CSS in `index.html` to match your team's preferences or brand colors.

### Check Items
Add your team-specific checks by editing the `reviewData` object.

### Severity Levels
Customize severity colors and meanings in the CSS section.

## 📄 License

MIT License - feel free to use this in your projects, modify it, or contribute back to the community.

## 🙏 Acknowledgments

- Inspired by real Laravel code review experiences
- Built for the Laravel community
- Thanks to all contributors and users providing feedback

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/laravel-code-review-assistant/issues)
- **Feature Requests**: Open an issue with the "enhancement" label
- **Questions**: Start a discussion in the Issues tab

---

**Made with ❤️ for the Laravel community**

⭐ If this tool helps you, please star the repository to help others discover it!
