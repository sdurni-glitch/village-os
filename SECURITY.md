# Security Best Practices

## Protecting Sensitive Information

This project follows security best practices to prevent accidental exposure of sensitive data.

### What's Protected by .gitignore:

- **Environment Variables**: `.env`, `.env.local`, `.env.*.local`
- **Credentials & Keys**: `.key`, `.pem`, `.p12`, `.pfx` files
- **API Keys & Secrets**: credentials/ directory
- **IDE Settings**: `.vscode/`, `.idea/` directories
- **Dependencies**: `node_modules/`, `venv/`, `env/`, `__pycache__/`
- **Local Configuration**: `config.local.json`, `settings.local.json`

### Guidelines:

1. **Never commit sensitive data** to version control
2. **Use environment variables** for configuration
3. **Keep secrets local** using `.env` files (not tracked by git)
4. **Review changes** before committing with `git diff`
5. **Enable branch protection** to require code reviews

### If You Accidentally Committed Secrets:

1. Rotate/revoke the exposed credentials immediately
2. Use `git filter-branch` or GitHub's secret scanning to remove history
3. Force push to remove sensitive commits

For more info: [GitHub Security Best Practices](https://docs.github.com/en/code-security)
