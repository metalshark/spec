# Contributing to TOON Specification

Thanks for your interest in contributing to the TOON specification! Whether you're fixing a typo, proposing a new feature, or clarifying ambiguous wording, your contributions help make TOON better for everyone.

This document outlines how to propose changes and improvements to the specification.

## Table of Contents

- [Types of Contributions](#types-of-contributions)
- [Before You Contribute](#before-you-contribute)
- [Proposing Changes](#proposing-changes)
- [RFC Process for Major Changes](#rfc-process-for-major-changes)
- [Specification Principles](#specification-principles)
- [Style Guidelines](#style-guidelines)

## Types of Contributions

### Clarifications and Fixes

Small improvements that don't change behavior:

- Typo corrections
- Grammar improvements
- Clarifying ambiguous language
- Adding examples
- Fixing broken links

**Process:** Open a pull request directly.

### Minor Changes

Backward-compatible additions or clarifications that may affect implementations:

- Adding test cases
- Clarifying edge case behavior
- Adding informative appendices
- Expanding examples

**Process:** Open an issue first to discuss, then submit a pull request.

### Contributing Test Fixtures

Test fixtures are language-agnostic JSON files that validate TOON implementations. You can contribute:

- New test cases for uncovered scenarios
- Edge case and error validation tests
- Tests for spec clarifications

Add your test case to the appropriate file in `tests/fixtures/encode/` or `tests/fixtures/decode/`, validate it against `tests/fixtures.schema.json`, and submit a PR. See [tests/README.md](./tests/README.md) for complete documentation on fixture structure and guidelines.

**Process:** Open a pull request directly.

### Major Changes

Changes that affect compatibility or core behavior:

- New syntax features
- Changes to encoding/decoding rules
- Modifications to conformance requirements
- Breaking changes

**Process:** Follow the RFC process (see below).

## Before You Contribute

Before contributing, check existing issues/PRs, review [SPEC.md](./SPEC.md), and consider backward compatibility.

## Proposing Changes

### Opening an Issue

GitHub provides three issue templates: **Bug Report** (for spec errors/ambiguities), **Specification Clarification** (for interpretation questions), and **Feature Request/RFC** (for proposing changes). Select the appropriate template when creating an issue.

### Submitting a Pull Request

Fork the repository, make your changes following the style guidelines, update CHANGELOG.md, and submit a PR. Fill out the PR template completely and link related issues.

### Review Process

- Spec maintainers will review your contribution.
- There may be discussion and requests for changes.
- Once approved, maintainers will merge and assign a version number.
- For breaking changes, the PR will be held until the next major version.

## RFC Process for Major Changes

Major changes require a Request for Comments (RFC) process:

1. **Create an RFC Issue** using the Feature Request/RFC template
2. **Discussion Period** – Community provides feedback (typically 1-2 weeks minimum)
3. **Decision** – Maintainers accept, reject, or request revisions
4. **Implementation** – Create a PR referencing the RFC issue number

The RFC template and PR template will guide you through providing all necessary details.

## Specification Principles

When contributing, keep these core principles in mind. They guide every decision we make about TOON:

### 1. Token Efficiency

TOON's primary goal is reducing token usage for LLM input. Changes should maintain or improve token efficiency.

### 2. LLM-Friendly Structure

The format should be easy for LLMs to parse and generate. Explicit length markers and field declarations are features, not bugs.

### 3. Human Readability

While optimized for machines, TOON should remain reasonably readable by humans for debugging and validation.

### 4. Simplicity

Prefer simple, consistent rules over special cases. The spec should be implementable without extensive parsing libraries.

### 5. Backward Compatibility

Breaking changes require very strong justification. Prefer additive changes that maintain compatibility.

### 6. Interoperability

Multiple implementations should produce identical output for the same input. Ambiguity is not acceptable.

## Style Guidelines

### Writing Style

- Use RFC 2119 keywords (MUST, SHOULD, MAY) correctly
- Be precise and unambiguous
- Use examples to clarify complex rules
- Keep language concise but complete
- Use active voice where possible

### Formatting

- Use proper markdown formatting
- Include code blocks with language hints
- Use section numbering consistently
- Add cross-references to related sections
- Keep line length reasonable (80-120 characters)

### Examples

- Show both input and output
- Include edge cases
- Demonstrate both valid and invalid cases
- Add comments explaining non-obvious behavior

## Questions?

If you have questions about contributing:

1. Check existing issues and discussions.
2. Open a new issue with the `question` label.
3. Reach out to maintainers.

## Code of Conduct

Be respectful and constructive in all interactions. We're building this specification together, and diverse perspectives make it better.

## License

By contributing to this specification, you agree that your contributions will be licensed under the MIT License.
