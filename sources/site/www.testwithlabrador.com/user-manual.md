# Source: https://www.testwithlabrador.com/user-manual

# User Manual

Accessibility Auditing  ·  WCAG 2.1 & 2.2  ·  Levels A & AA  ·  VPAT 2.5

Labrador helps you evaluate websites and UI components against WCAG 2.1 and 2.2 standards at Levels A and AA. All auditing takes place through your browser at [testwithlabrador.com](https://testwithlabrador.com).

## Getting Started

### Create Your First Project

1. Log in at [testwithlabrador.com](https://testwithlabrador.com).
2. On the Projects dashboard, click **\+ Create Project**.
3. Enter a **Project Title** and a brief description.
4. Select a **Testing Methodology** from the dropdown (e.g., _WCAG 2.2 AA Testing_ or _VPAT® 2.5 – WCAG 2.2_).
5. Click **Create Project**.

**Note:** If you need a `.docx` output, select the applicable VPAT methodology. The project type setting cannot be changed after the project is created.

### Managing Pages & Components

A project is made up of the specific URLs or UI elements you need to test.

#### Add an Item to Test

1. Open your project and click **\+ Add Page / Component**.
2. Enter a **Name** (e.g., _Homepage_ or _Navigation Header_).
3. Provide the **URL** for the page.
4. (Optional) Upload a **Screenshot** to help identify the item.
5. Click **Create**.

### Customizing Your Audit

Add project-specific data points to issue reports using custom fields.

#### Set Up Custom Fields

1. In the project view, expand the **Custom Fields** section.
2. Click **\+ Add Field**.
3. Enter a **Field Name** (e.g., _Browser Version_).
4. Choose a **Type**: Single Line Text, Number, Dropdown, etc.
5. Check **Required** if the field must be completed for every issue.
6. Click **Add Field**.

**Note:** To save time on future projects, use the **Load Template** button to reuse a saved set of custom fields instead of recreating them manually.

## The Auditing Process

Each Page & Component is evaluated against applicable WCAG criteria.

### Evaluate a Criterion

1. Click on a Page or Component to open the **Criteria Overview**.
2. Use the filters to sort by Level, Severity, or Status.
3. Select a criterion (e.g., _1.1.1 Non-text Content_).
4. Review the **Testing Tip** for guidance.

Mark the Test Status as:

- **Pass:** The item meets the requirement.
- **Fail:** The item does not meet the requirement.
- **N/A:** The criterion does not apply to this item.
- **Untested:** Evaluation has not yet started.

### Log an Issue

When a criterion fails, document the specific problem:

1. Under the failing criterion, scroll to **Add New Issue**.
2. Write a clear **Issue Description**.
3. Add **Remediation Help** to explain how the problem can be fixed.
4. Select a **Severity**: Advisory, Minor, Moderate, Serious, or Critical.
5. Set the **Remediation Status**: Reported, In Progress, Fixed for Retesting, or Closed.
6. Attach supporting files by dragging and dropping screenshots or video recordings.
7. Click **Submit Issue**.

## Collaboration

Labrador is designed for team-based auditing.

- **Invite Members:** Click the **Teammates** button to add colleagues to a project.
- **Leave Comments:** Use the Comments section at the bottom of any issue to discuss findings.
- **Plan Limits:** The number of team members allowed depends on your subscription tier: Trial, Core, Pro, or Enterprise.

## Exporting Results

Once testing is complete, generate a professional report.

### Generate a Report

1. Click the **Export** dropdown in your project.
2. Select your preferred format:

- **HTML:** A live, interactive web-based report.
- **CSV Export:** A flat list of all logged issues.
- **Jira CSV Export:** A file formatted for direct import into Jira.
- **PDF / Word:** Project summaries or official VPAT® 2.5 documents (only available for VPAT projects).

**Note:** HTML, CSV, and Jira CSV exports are available for all project types.

## Audit Versions & Retests

Every project starts at **v1.0**. When your client fixes issues and you need to verify the remediation — or you want to audit the same site again from scratch — create a new version instead of overwriting your results. The **Audit version** bar at the top of the project view shows which version you are working in and holds the version controls.

### Create a Retest Version

A retest is for verifying fixes. It bumps the minor version (v1.0 → v1.1) and carries your entire audit forward so you can check each finding without re-documenting it.

1. Open the project and find the **Audit version** bar.
2. Click **Version actions** and choose **Create retest version**.
3. Labrador copies your pages, criterion statuses, notes, and every logged issue into the new version. Carried issues keep their original numbers and are marked _Carried forward_ from the source version.
4. Retest each finding. When a fix is verified, set the issue's remediation status to **Closed**.

**Note:** When every carried-forward issue on a criterion is closed, the criterion's status updates automatically — and reopening an issue restores it. Your original version is never modified by a retest.

### Start a New Audit

A new audit bumps the major version (v1.x → v2.0) for a fresh top-to-bottom evaluation. From **Version actions**, choose either:

- **Start new audit and keep pages:** your page/component list (with URLs and testing environment details) is copied over, but statuses and issues start clean.
- **Start new blank audit:** nothing is carried over — an empty version of the project.

### Switch & Delete Versions

- **Switch:** use the version dropdown in the Audit version bar. When you are viewing anything other than the latest version, a _Viewing vX_ badge reminds you.
- **Delete:** open **Version actions** and choose **Delete v…**. A confirmation dialog spells out exactly what will be removed before anything happens, and you are moved to another version afterwards. Deleting is only available while the project has more than one version, and it cannot be undone.

## Jira Integration

Connect a project to Jira Cloud and the issues you log are created on your Jira board automatically — no copy-paste handoff — with status and priority changes syncing in both directions. Available on any paid plan (Core, Plus, or Enterprise); connecting requires edit access to the project. On the Free plan, use the Jira-ready CSV export instead (see _Exporting Results_).

### Connect Your Project

1. Open the project and expand the **JIRA Integration** section.
2. Click **Connect to JIRA** and sign in with your Atlassian account, granting access to your Jira Cloud site.
3. Back in Labrador, choose the **JIRA Project** and **Issue Type** new issues should be created as.
4. Click **Save JIRA Mapping**.

### Mappings & Templates

Before saving, you can tune how Labrador issues translate into Jira issues:

- **Severity → JIRA Priority:** map each Labrador severity level (advisory through critical) to one of your Jira priorities.
- **Custom Field Mapping:** if the project uses custom fields, send each one to a matching field in Jira.
- **Summary & Description Templates:** control how the Jira issue's title and body are composed using variables such as `{{page}}`, `{{criterion}}`, and `{{criterionName}}` — use the insert buttons under each field to add them.

### How Syncing Works

- Once mapped, **new issues you log are pushed to Jira automatically** as they are created.
- Status and priority changes flow both ways: closing or reprioritizing in either tool updates the other. The integration card shows _Reverse sync active_ when Jira-to-Labrador updates are enabled.
- Use the **Open in JIRA** link on the integration card to jump to the connected board.
- **Disconnect** unlinks the project at any time. Issues already created in Jira stay in Jira; they simply stop syncing.

## Chrome Extension

The Labrador Chrome extension lets you capture HTML directly from a live page and attach it to an issue.

### Installation

1. Go to the Chrome Web Store.
2. Download [**Labrador AI Accessibility Assistant** (opens in new tab)](https://chromewebstore.google.com/detail/labrador-ai-accessibility/lndpalafhngglhpdjejhelccebmngoho).

### Usage

1. Create an issue with a clear description.
2. Click **Generate Recommendation**.
3. Navigate to the target page and click the specific element you are auditing.
4. The element's code and suggested fix will automatically be appended to the issue description under **Remediation Help**.

## Filtering & Navigation

The filtering system helps you manage long lists of WCAG criteria and focus on what matters most. Filters are located at the top of the Criteria Overview for any Page or Component.

### Keyword Search

Type a criterion name (e.g., _Non-text Content_) or number (e.g., _1.1.1_) into the **Search criteria** box. The list filters automatically as you type.

### Filter by Status

- **Pass** — Criteria that have met the requirement.
- **Fail** — Criteria where an issue was identified.
- **N/A** — Criteria marked as not applicable.
- **Untested** — Criteria not yet evaluated.
- **Bookmarked** — Criteria you have flagged for quick access.

### Filter by Conformance Level

Click the **All Levels** dropdown to filter by WCAG conformance level: Level A (basic requirements) or Level AA (standard enterprise requirements).

### Filter by Issue Details

- **Severity:** Advisory · Minor · Moderate · Serious · Critical
- **Remediation:** Reported · In Progress · Fixed for Retesting · Closed

### Testing View Modes

Use the toggle beside **Filter by Status** to switch between **Side by side** and **Pop-up**. Side by side is the default and keeps the criterion list visible while testing. Pop-up opens the same testing panel in a dialog.

## Progress Tracking

Labrador provides visual progress feedback so you can gauge audit completion at a glance.

- **Overall Progress Bar:** Displayed in the Criteria Overview header; shows the total percentage of criteria tested for the current page.
- **Progress by Level:** Dedicated sub-bars track completion rates for Level A and Level AA requirements separately.
- **Status Tally:** A live count at the top of the Criteria Overview shows the total number of items marked Pass, Fail, N/A, or Untested.

## Reference & Educational Tools

Each criterion includes built-in guidance to support accurate testing decisions.

- **Why This Matters:** Provides context on how a specific accessibility barrier impacts users with disabilities.
- **Testing Tips & Key Points:** Offers actionable steps and summarized takeaways for evaluating a rule.
- **Official Documentation:** Click the **View on W3C** button to open the official WCAG documentation for the criterion in a new tab.

### Sub-Criteria Auditing

Complex WCAG rules are broken into smaller, manageable parts for more precise auditing.

- **Expandable Sub-Groups:** Certain criteria (e.g., 1.3.1 Info and Relationships) include a Sub-Criteria Testing section that expands to show specific elements such as Headings, Lists, and Tables.
- **Individual Status Marking:** Each sub-item can be marked Pass, Fail, or N/A independently.

### Efficiency Features

- **Custom Field Templates:** Click **Load Template** in the Custom Fields section to apply a saved field set to any new project.
- **Criteria Bookmarking:** Click the Bookmark button on any criterion to flag it for quick access later.

### Interactive HTML Reports

When you export results as an HTML report, the document remains interactive for readers.

- **Show Failures Only:** A button that hides passing and N/A criteria so developers can focus exclusively on issues.
- **Expand All / Collapse All:** Quickly manage visibility across long criteria lists.
- **Automatic Metadata:** Reports automatically include the auditor's name, WCAG version, and the exact date and time the report was generated.

### AI Remediation (Beta)

Labrador includes an AI-assisted remediation feature, currently in beta, that drafts developer-ready guidance from the HTML of the element you are reporting. It uses the [**Labrador Chrome extension** (opens in new tab)](https://chromewebstore.google.com/detail/labrador-ai-accessibility/lndpalafhngglhpdjejhelccebmngoho) to capture that HTML from the live page, so install it first (see the [Chrome Extension](https://www.testwithlabrador.com/user-manual#chrome-extension) section above) before using this feature.

- When creating the Page or Component, provide a valid **URL** — the AI uses it to open the exact page being tested.
- The feature lives in the issue form. You must first add a clear **issue description**, and then click **“Generate Recommendations”** below the **“Remediation help”** field. This will, using the Chrome extension, bring you to the page being tested.
- Visually select the context (if applicable) and then select the problem element. You will be brought back to Labrador, where a remediation recommendation will be generated based on your issue description, HTML selection, and the success criterion you are testing.