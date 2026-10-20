# Contributing to LEAK

Thanks for taking the time to help improve LEAK.

The goal is to keep this project useful, understandable, and honest about what a browser can expose. A small fix with a clear explanation is more valuable than a large change that adds complexity without improving the result.

## Before you start

- Search existing issues and pull requests to avoid duplicating work.
- For a substantial change, open an issue first so the approach can be discussed.
- Keep the project dependency-free at runtime and preserve its single-file website format unless the change clearly justifies otherwise.
- Never include your personal IP address, full browser fingerprint, or private scan report in a public issue.

## Making a change

1. Fork the repository and create a focused branch.
2. Make the smallest change that solves the problem.
3. Test `index.html` in a browser, including the relevant behavior.
4. Check the browser console for errors.
5. Explain what changed, why it was needed, and how you tested it in your pull request.

For changes to browser-signal checks, describe the API being read and any known limitations. Do not present heuristics as definitive measurements.

## Pull request checklist

- [ ] The change has a clear purpose.
- [ ] Existing layout and interactions still work.
- [ ] No unnecessary runtime dependencies were added.
- [ ] Privacy claims in the page and documentation remain accurate.
- [ ] Testing and known limitations are described.
- [ ] No personal or sensitive scan output is included.

By participating, you agree to follow the project's [Code of Conduct](CODE_OF_CONDUCT.md).
