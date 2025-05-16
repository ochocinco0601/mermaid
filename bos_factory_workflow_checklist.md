# BOS Factory Workflow Checklist (VS Code + GitHub Copilot Chat)

This checklist walks through the full lifecycle of completing a Business Observability System (BOS) artifact using the structured `BO_System` repo and GitHub Copilot Chat.

---

## 👝 Step 1: Open the Workspace

* [ ] Launch VS Code
* [ ] Open `bo_system.code-workspace` from the `BO_System/` folder
* [ ] Confirm `README.md` is visible in the Explorer
* [ ] Ensure `templates/`, `prompts/`, and `outputs/` are loaded

---

## 📏 Step 2: Start a New Business Observability Template

* [ ] Open `business-observability-template.md` in the `templates/` folder
* [ ] Save a copy to `outputs/` with a relevant system or step name
  *Example: `outputs/template-loan-submission.md`*

---

## 💬 Step 3: Use Copilot Chat to Generate or Review Template Content

**For content generation:**

* [ ] Prompt: `"Use this template and generate content for the 'Loan Application Submission' step."`
* [ ] Review Copilot's output and edit inline

**For validation:**

* [ ] Prompt: `"Review this completed template for vague or missing fields."`
* [ ] Update all `Pending input –` or empty sections

---

## 📌 Step 4: Define Key Signals

* [ ] Identify all `Business Signals`, `Process Signals`, and `System Signals`
* [ ] Prompt Copilot: `"Given this business context, what are strong examples of each signal type?"`
* [ ] Confirm each signal includes owner, source, and intended dashboard use

---

## 🧪 Step 5: Generate Output Artifacts

* [ ] Prompt Copilot: `"Summarize this template into a dashboard spec."`

* [ ] Save output as:
  *Example: `outputs/dashboard-spec-loan-submission.md`*

* [ ] Optional: Prompt Copilot: `"Create a reference card version of this template for use in incident triage."`

---

## 🔄 Step 6: Review & Commit

* [ ] Save all modified and generated files in `outputs/`
* [ ] Open terminal and run:

  ```bash
  git add outputs/
  git commit -m "Add completed template and dashboard spec for loan submission"
  git push
  ```

---

## ✅ Step 7: Confirm Traceability

* [ ] All signals have clear owners
* [ ] Business outcomes are tied to metrics or logs
* [ ] Outputs are version-controlled and traceable to the template used

---

## 🧠 Optional Extensions

* [ ] Create a visual flow map or timeline for the business step
* [ ] Build a signal matrix from multiple templates
* [ ] Link template signals to actual telemetry sources (e.g., Splunk, APM)

---
