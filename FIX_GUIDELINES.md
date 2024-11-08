# Fix Branch Guidelines

## Fix Branch Types
1. **Critical Fixes** (fix/critical-*)
   - Security issues
   - App crashes
   - Data corruption issues
   - Naming pattern: fix/critical-[issue]

2. **Feature Fixes** (fix/feature-*)
   - Behavioral issues
   - UI/UX improvements
   - Performance optimizations
   - Naming pattern: fix/feature-[component]-[issue]

3. **Technical Fixes** (fix/tech-*)
   - Code refactoring
   - Technical debt
   - Build system issues
   - Naming pattern: fix/tech-[area]-[issue]

## Fix Branch Flow
```
main
 ├── fix/critical-auth-crash
 │   └── Merges directly to main after testing
 ├── fix/feature-timer-precision
 │   └── Merges to feature branch or main
 └── fix/tech-build-optimization
     └── Merges to main after review
```

## Fix Commit Convention
```bash
# Critical fix
git commit -m "fix(critical): resolve app crash on timer overflow"

# Feature fix
git commit -m "fix(timer): improve precision for sub-second intervals"

# Technical fix
git commit -m "fix(build): optimize asset compilation time"
```

## Fix Testing Requirements
1. **Critical Fixes**
   - Must have unit tests
   - Must have integration tests
   - Requires immediate review
   - Must update security documentation if applicable

2. **Feature Fixes**
   - Must have related feature tests
   - Requires normal review cycle
   - Must update feature documentation

3. **Technical Fixes**
   - Must have performance metrics if applicable
   - Requires technical review
   - Must update technical documentation

## Fix Template
```
## Fix Description
[What does this fix address?]

## Root Cause
[What caused the issue?]

## Solution
[How does this fix resolve the issue?]

## Testing
- [ ] Unit tests
- [ ] Integration tests
- [ ] Manual verification

## Documentation
- [ ] Updated relevant docs
- [ ] Added comments
- [ ] Updated changelog
```

## Fix Branch Lifecycle
1. **Creation**
   ```bash
   git checkout main
   git pull origin main
   git checkout -b fix/type-description
   ```

2. **Development**
   ```bash
   # Make changes
   git add .
   git commit -m "fix(scope): description"
   ```

3. **Testing**
   ```bash
   # Run tests
   xcodebuild test
   ```

4. **Review**
   ```bash
   # Push for review
   git push origin fix/type-description
   # Create Pull Request
   ```

5. **Merge**
   ```bash
   git checkout main
   git pull origin main
   git merge --no-ff fix/type-description
   git push origin main
   ```

6. **Cleanup**
   ```bash
   git branch -d fix/type-description
   git push origin --delete fix/type-description
   ```

## Fix Priority Levels
1. **P0: Critical**
   - Security vulnerabilities
   - Data loss
   - App crashes
   - 24-hour resolution

2. **P1: High**
   - Major functionality broken
   - Performance issues
   - 72-hour resolution

3. **P2: Medium**
   - Minor functionality issues
   - UI/UX problems
   - 1-week resolution

4. **P3: Low**
   - Non-critical improvements
   - Technical debt
   - 2-week resolution
