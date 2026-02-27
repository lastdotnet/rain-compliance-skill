---
name: rain-compliance-checker
description: "Check any marketing material, landing page, blog post, video script, social copy, or UI text for compliance with Rain's partner marketing guidelines for crypto credit cards. Use this skill whenever someone asks to review content for Rain compliance, check if marketing copy is compliant, audit a page or document against Rain/Visa card rules, or needs help writing compliant copy for a crypto credit card product. Also trigger when you see mentions of Rain, Visa card compliance, crypto card marketing rules, partner marketing guidelines, or DeFi protocol integration disclaimers. Even if the user just says 'check this for compliance' or 'is this copy OK' in the context of a crypto card product, use this skill."
---

# Rain Partner Marketing Compliance Checker

## Overview

This skill checks marketing materials against Rain's Partner Marketing Guidelines, Legal Overview, DeFi Protocol Integration requirements, and Direct Solicitation rules. It is used by teams building card products powered by Rain (a Visa Principal Member) to ensure all public-facing content is compliant before submission to Rain's marketing review.

## How to Use This Skill

When the user provides content to check (text, copy, a page, a script, a document), do the following:

1. **Read the full compliance rules** in `references/rain-compliance-rules.md` before evaluating anything
2. **Scan every line** of the user's content against the rules
3. **Categorize each finding** as one of:
   - **REMOVE** — content that is explicitly prohibited and must be deleted
   - **REPHRASE** — content that is close to a violation or uses non-approved language and needs rewording
   - **ADD** — required elements (disclaimers, disclosures) that are missing
   - **FLAG TO RAIN** — content that is in a gray area and should be submitted to Rain for explicit approval
   - **OK** — content that is compliant (only mention if the user asks for a full audit)
4. **For every finding**, cite the specific rule and source document (e.g., "Partner Marketing Guidelines p.8")
5. **Provide the specific fix** — don't just say "rephrase," give the compliant alternative
6. **Ask about distribution channel** if not specified — the rules differ significantly between organic (website, organic social) and direct solicitation (paid ads, email, KOL/influencer) channels

## Important Context

- Rain requires ALL public-facing marketing materials to be submitted to marketingreview@rain.xyz at least **14 business days** before launch
- This includes websites, ads, social posts, decks, explainer videos, onboarding flows, and scripts/storyboards
- Rain continuously monitors post-launch; non-compliance may result in program pause, suspension, or termination
- Video scripts and storyboards must be approved BEFORE production
- The compliance rules in the references file are derived from Rain's official partner documentation (Nov 2025 edition)

## Output Format

Structure your response as:

1. **Summary** — quick verdict (compliant / mostly compliant with issues / significant issues)
2. **Findings** — each issue listed with: the problematic text, the rule it violates, the source, and the specific fix
3. **Missing elements** — any required disclaimers or disclosures that are absent
4. **Channel note** — if the distribution channel affects compliance (Visa branding rules differ by channel)

Keep findings actionable. The user should be able to hand your output to a copywriter and have them fix everything without needing to read the Rain docs themselves.
