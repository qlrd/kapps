# Security Policy

## Disclaimer

**WARNING:** This software has not yet been formally audited by a third party. Use at your own risk!

Kapps are signed applications that run on [Krux](https://github.com/selfcustody/krux) signing devices. While we take security seriously, the code handles sensitive cryptographic operations and should be treated accordingly.

## Supported versions

| Version | Supported |
|---------|-----------|
| Latest release | Yes |
| Previous releases | No |

## Reporting a vulnerability

If you discover a security vulnerability, please report it responsibly:

1. **Do not** open a public issue
2. Email the maintainers at `tadeubas@gmail.com` with:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)
3. Allow reasonable time for a fix before public disclosure

## Security considerations

- Kapps handle private keys, mnemonics, and other sensitive data
- All kapps are compiled to `.mpy` and must be signed before execution on devices
- The device verifies kapp signatures before running them
- Review kapp source code before compiling and signing

## Best practices for kapp developers

- Never log or persist private keys or mnemonics
- Clear sensitive data from memory as soon as it is no longer needed
- Use the `krux` API for cryptographic operations rather than custom implementations
- Test edge cases around key handling and data validation
