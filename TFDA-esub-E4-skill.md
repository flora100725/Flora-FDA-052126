name: skill-creator-pro description: An advanced engine for architecting, refining, and validating high-performance AI skills. Use this to create skills from scratch, optimize existing logic, and run rigorous benchmarks. This version includes specialized modules for Predictive Risk Assessment, Regulatory Compliance Alerting, and Automated Evidence Cross-Referencing. Use this skill whenever a user needs to build mission-critical AI workflows that require high reliability and adherence to evolving standards.
Skill Creator Pro
An advanced framework for creating, iteratively improving, and benchmarking AI skills with integrated safety and accuracy modules.

Core AI Features
1. Predictive Risk Assessment
Before finalizing a skill draft, the system must run a predictive simulation to identify potential failure modes.

Instructional Ambiguity: Detect sections where a model might misinterpret tone or constraints.
Edge Case Vulnerability: Identify inputs that could cause the skill to deviate from its intended logic.
Bias Detection: Screen for unintended demographic or operational biases in the prompt instructions.
2. Real-time Regulatory Change Alerting
This module cross-references the skill's purpose and logic against a live database of AI regulations (e.g., EU AI Act, NIST Framework).

Compliance Check: Flags instructions that might violate data privacy or transparency requirements.
Update Notifications: If a regulatory standard changes during the development cycle, the system alerts the user to adjust the skill's frontmatter or logic.
3. Automated Evidence Cross-Referencing
During the evaluation phase, the system does not just "vibe check" outputs. It performs a semantic audit.

Source Verification: Cross-references generated content against bundled resources or references/ to ensure no hallucinations.
Consistency Mapping: Ensures that the output of Iteration N remains consistent with the foundational constraints defined in the original Intent Capture.
4. Synthetic Twin Benchmarking (Wow Feature)
For every test case, the system generates a "Synthetic Twin"—a gold-standard response created by a maximum-parameter configuration. This serves as a dynamic baseline to measure the delta between the current skill performance and theoretical perfection.

5. Cognitive Architecture Optimization (Wow Feature)
The system monitors the complexity of the SKILL.md. If the logic exceeds 500 lines or involves more than three nested conditional branches, it automatically proposes a "Sub-Skill Split," refactoring the architecture into a parent skill with modularized references/ to prevent context bloating and "undertriggering."

6. Self-Healing Prompt Refinement (Wow Feature)
Utilizing the results from grading.json, the system employs a generative feedback loop to suggest "Micro-Fixes." If a specific assertion fails across multiple evals, the system identifies the exact sentence in SKILL.md responsible and provides three alternative phrasings optimized for model steering.

The Workflow
1. Capture Intent & Risk Profile
Understand the goal and trigger context.

What is the primary task?
Risk Profile: Categorize the skill (Low, Medium, High Risk). High-risk skills (e.g., medical, financial, legal) trigger mandatory Predictive Risk Assessment.
2. Write the SKILL.md
Follow the standard anatomy, but integrate the new modules.

name: Unique identifier.
description: Pushy, high-accuracy trigger description.
Regulatory Metadata: Add a compliance field to YAML if applicable.
3. Execution & Automated Cross-Referencing
When running test cases:

Spawn Runs: Parallelize with-skill and baseline runs.
Cross-Reference: Use a subagent to verify that the "with-skill" output aligns with any provided documentation in references/.
Risk Audit: Run the Predictive Risk Assessment script to flag potential hallucination points.
4. Benchmarking with Synthetic Twins
Use the scripts.aggregate_benchmark to compare:

Current Skill vs. Baseline (No skill)
Current Skill vs. Synthetic Twin (Gold standard)
Current Skill vs. Previous Iteration
5. Evaluation Viewer
Launch the viewer using generate_review.py. Ensure the "Benchmark" tab includes:

Accuracy Score: Based on Evidence Cross-Referencing.
Compliance Status: Based on Regulatory Change Alerting.
Reliability Index: Derived from the Predictive Risk Assessment.
Skill Writing Guide
Anatomy of a Skill
skill-name/
├── SKILL.md (Core logic + Risk Mitigations)
├── references/ (Static knowledge for Cross-Referencing)
├── scripts/ (Deterministic validation scripts)
└── tests/ (evals.json including Synthetic Twin definitions)
Writing Patterns
Imperative Clarity: Use "COMMAND" style for core actions.
The "Why" Principle: Explain the reasoning behind constraints to leverage the model's theory of mind.
Modular Redundancy: If a task is critical, instruct the model to perform a "Self-Audit" step, referencing the Evidence Cross-Referencing module.
Description Optimization
After the logic is stable, run the 20-query optimization loop.

Generate Queries: 10 should-trigger (diverse, messy, realistic), 10 should-not-trigger (near-misses).
Regulatory Validation: Ensure the description does not claim capabilities that violate compliance (e.g., "This skill provides definitive medical advice").
Iteration: Run scripts.run_loop to find the description with the highest trigger accuracy.
Reference Schemas
Refer to references/schemas.md for updated JSON formats including:

risk_assessment_report.json
compliance_audit.json
cross_reference_log.json
Final Goal: Produce a skill that is not only functional but resilient, compliant, and architecturally sound.
