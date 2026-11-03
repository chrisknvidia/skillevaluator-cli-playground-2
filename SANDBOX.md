# Try SkillEvaluator onboarding

This personal test repository starts with skills and no CI setup. Use the locally prepared SkillEvaluator preview from this repository:

```bash
skillevaluator ci init
```

Choose folder `1` for two small sample skills, or `1,2` to also include the 19 upstream skills. Review the choices, select `pr`, and confirm. The wizard configures report hosting and opens a setup PR; review and merge it on GitHub.

After merging setup, you can ask the CLI to create a small test PR:

```bash
skillevaluator ci demo
```

It asks before creating the PR. Inspect **Checks**, the bot comment under **Conversation**, and its **Open full report** link. Close the test PR afterward; merging it is unnecessary. Existing skill issues may produce a failed check even when onboarding succeeds.

## Preview scope

The locally installed preview includes onboarding. The published PyPI 0.7.0 package does not contain the `ci` commands. The scanner image is the official static CI release; the publisher is pinned to the review candidate in NVIDIA/SkillEvaluator#326. No model key is used. This public repository publishes reports publicly if you enable hosting.

This is a fresh copy of the original playground before onboarding, with upstream skills from anthropics/skills and their original licenses retained. The two `sandbox-skills` samples come from NVIDIA/SkillEvaluator public smoke-test fixtures at commit e4cda13a85f34fa7a112b3529feaf24cfe587caf; their manifests declare MIT licensing. No upstream repository was changed.
