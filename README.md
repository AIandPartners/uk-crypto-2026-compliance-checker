# UK Crypto 2026 Compliance Gap Checker

**A self-service compliance gap analysis tool for UK crypto firms preparing for the FSMA 2026 regulatory regime.**

⚠️ **NOT LEGAL ADVICE** - This tool provides an initial gap assessment only. Consult qualified legal counsel for compliance strategy.

---

## What This Does

Compares your internal policies against the UK's 2026 crypto regulatory requirements (FSMA Crypto SI, FCA CP25/40) and generates:
- A structured gap report identifying missing requirements
- A readiness score (0-100%)
- Specific recommendations for policy updates

---

## Prerequisites

1. **Claude Cowork** with legal plugin enabled ([more info](https://www.anthropic.com/claude-cowork))
2. Access to your internal compliance documents
3. Ability to work with local file folders

---

## Setup Instructions

### Step 1: Clone This Repository
```bash
git clone https://github.com/yourusername/uk-crypto-2026-compliance-checker.git
cd uk-crypto-2026-compliance-checker
```

### Step 2: Create Your Working Directory

Create a folder structure on your machine:
```
Compliance_Project/
├── Reg_Sources/
│   └── (copy UK_Crypto_Reg_2026_Matrix.md here)
└── My_Docs/
    └── (add your internal policies here)
```

### Step 3: Add Your Documents

Copy into `My_Docs/`:
- Governance policies
- Custody procedures
- Marketing guidelines
- Terms & Conditions
- Risk management frameworks
- AML/KYC policies
- Any crypto-specific procedures

### Step 4: Run the Analysis

Open Claude Cowork in your `Compliance_Project` folder and paste this prompt:

---

**COPY-PASTE PROMPT (the "Promoty"):**
```
Act as a Senior UK Regulatory Lawyer specializing in crypto asset regulation.

Your task:
1. Scan the local folder structure
2. Load the Regulatory Matrix from /Reg_Sources/UK_Crypto_Reg_2026_Matrix.md
3. Review all documents in /My_Docs/
4. For EACH Pillar in the Matrix:
   - Check if relevant policies exist
   - Identify whether mandatory language appears
   - Flag any red-flag patterns (e.g., outdated regulatory references)
   - Note missing requirements

5. Generate a file called COMPLIANCE_GAP_REPORT.md containing:
   - Executive Summary with overall readiness score (0-100%)
   - Gap Analysis by Pillar (table format)
   - High-priority gaps requiring immediate attention
   - Medium/low-priority gaps
   - Specific recommendations with document references

Use this scoring rubric:
- 90-100%: Substantially compliant
- 70-89%: Minor gaps, manageable remediation
- 50-69%: Significant gaps, structured action plan needed
- Below 50%: Major deficiencies, urgent legal review required

Be specific. Quote actual text from policies where relevant. Cite which Matrix requirement each gap relates to.
```

---

### Step 5: Review the Output

Claude will create `COMPLIANCE_GAP_REPORT.md` in your project folder with:
- Your readiness score
- Detailed gap analysis
- Prioritized action items

---

## What Happens Next?

This tool gives you a **first-pass assessment**. For:
- Remediation planning
- Policy drafting
- Regulatory interpretation
- FCA engagement strategy

...you should engage qualified legal counsel.

---

## Updating the Matrix

The regulatory landscape evolves. To update:
1. Edit `regulations/UK_Crypto_Reg_2026_Matrix.md`
2. Add new Pillars/Requirements as FCA publishes guidance
3. Re-run the analysis against updated standards

---

## License & Disclaimer

This repository provides regulatory intelligence only. It does not constitute legal advice. The UK crypto regulatory regime is complex and subject to interpretation. Always consult legal professionals for compliance strategy.
