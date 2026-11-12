# Contributing to AZ-305 Study Notes

Thanks for helping keep these notes accurate. They cover **Microsoft Exam AZ-305: Designing Microsoft Azure Infrastructure Solutions**, and Azure changes fast: services get renamed or retired, SKU tiers and SLAs move, and the study guide is revised from time to time. Reports from people studying with the notes are the best way to catch that.

> [!IMPORTANT]
> **This repo accepts issues, not pull requests.** Pull requests are turned off: I write every change myself and check it against the official documentation, so the notes keep one voice and stay consistent from page to page. If you know exactly how something should read, put your proposed wording in the issue. It's just as useful.

---

## Contents

- [Ways to Help](#-ways-to-help)
- [Before You Open an Issue](#-before-you-open-an-issue)
- [Opening an Issue](#-opening-an-issue)
- [Out of Scope](#-out-of-scope)
- [What Happens Next](#-what-happens-next)
- [Code of Conduct](#-code-of-conduct)
- [Security](#-security)

## 🙌 Ways to Help

Every report fits one of the five types in the issue template:

| Type | What it covers | For example |
| --- | --- | --- |
| 🐛 **Bug** | Broken links, search, navigation or Mermaid diagrams | A decision-tree diagram shows as plain text instead of a chart, search finds nothing for a term that's on a page, or a Microsoft Learn link returns 404 |
| ❌ **Wrong content** | An incorrect fact, number or exam tip | A composite SLA calculation doesn't add up, a SKU comparison puts a feature in the wrong tier, or an exam tip recommends the wrong service for its scenario |
| 🕰️ **Outdated content** | Azure or the exam has changed since this was written | A service or tier was renamed or retired, or the study guide's domain weights or skills have changed since the revision the notes follow |
| 📱 **Device issue** | The page looks or behaves wrong on a device or browser | A wide comparison table can't be scrolled on a phone in portrait, or the sidebar menu won't open on a tablet |
| 💬 **Something else** | Anything the other four don't cover | A topic that would be clearer as a decision table or a diagram, or an exam trap the cheatsheet is missing |

## 🔎 Before You Open an Issue

- **Search the existing issues**, [open and closed](https://github.com/marcogrimaldi29/az-305-study-notes/issues?q=is%3Aissue). If yours is already there, add a 👍 reaction or a comment with anything new rather than opening a duplicate.
- **Check the date.** The notes are written against the study guide as it stood in **October 2024**, which is where the domain weights in the README come from. If the "Skills measured as of" heading in the [study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-305) shows a newer date, say so in the issue. It tells me which revision to compare against.
- **Check the current docs.** A quick look at the [Azure documentation](https://learn.microsoft.com/en-us/azure/) or the [Azure Architecture Center](https://learn.microsoft.com/en-us/azure/architecture/) usually confirms whether something has changed, and gives you the link the issue asks for.
- **One problem per issue.** Separate issues are easier to track, fix and close. Several typos on the same page can go in one issue.
- **For a site bug, hard-refresh first** (Ctrl+F5, or Cmd+Shift+R on a Mac) in case your browser is showing an older copy of the page.

## 📝 Opening an Issue

1. Open a new issue with the [🐞 Report a problem](https://github.com/marcogrimaldi29/az-305-study-notes/issues/new?template=ISSUE_TEMPLATE.md) template.
2. Give it a title that names the page and the problem, for example *"03 Business Continuity: wrong RPO in the Azure Site Recovery section"* rather than *"Mistake on page"*.
3. Fill in the template's sections and delete any that don't apply.

> [!TIP]
> To link straight to a section, point to its heading on the site and click the link icon that appears next to it, then copy the address from your browser.

### What Makes a Report Easy to Fix

- **A link to the exact section**, not just the page
- **The text as the notes have it**, quoted, so it can be found even if the page has moved on
- **An official source** for any content change. Microsoft Learn is best. A report without one may take longer, because every change has to be checked against the documentation before it goes in
- **For bugs and device issues:** the steps to reproduce it, what you expected and what happened instead, the device, operating system and browser, and a screenshot if it shows the problem
- **Your proposed wording**, if you have it. With pull requests turned off, this is the closest thing to suggesting an edit directly

## 🚫 Out of Scope

To keep the notes accurate and the issue tracker useful, please don't open issues for:

- **Live exam content.** Questions, answers, case studies or topics remembered from a real exam break [Microsoft's exam security policy](https://learn.microsoft.com/en-us/credentials/support/exam-and-assessment-lab-security-policies) and the Candidate Agreement every candidate accepts before the exam. Issues or comments that include them will be closed and the content removed.
- **Exam booking, scores, retakes or renewals.** [Microsoft Credentials support](https://learn.microsoft.com/en-us/credentials/support/help) can help with those, including questions about the Azure Solutions Architect Expert certification and its AZ-104 prerequisite.
- **Help with your own Azure environment.** For troubleshooting your own subscription, tenant or deployment, or a review of your own architecture, ask on [Microsoft Q&A](https://learn.microsoft.com/en-us/answers/) or open an Azure support request.
- **Anything private.** Issues are public, so leave out subscription and tenant IDs, resource names, IP addresses, connection strings, keys and customer details, including in screenshots of the Azure portal.
- **Unofficial sources.** Exam dump sites, third-party practice tests and AI chat answers aren't accepted as the source for a content change.
- **Promotion.** Links to courses, products or services, affiliate links and paid placements won't be added.
- **Security vulnerabilities.** Please [report these privately](https://github.com/marcogrimaldi29/az-305-study-notes/security/advisories/new), as described in the [security policy](SECURITY.md), not in a public issue.

## 🔄 What Happens Next

- I maintain the notes on my own, in my spare time, so replies are best effort and there's no fixed response time.
- I check each report against the official documentation. If something needs clarifying, I'll ask on the issue, so keep an eye on your GitHub notifications.
- When a fix goes in, the issue is closed with a note or a link to the change. The live site updates shortly after.
- If nothing changes, the issue is closed with the reason, such as out of scope, can't be verified, or working as intended.
- An issue waiting on a reply may be closed after a while. Comment with the missing details and it can be reopened.

## 🤝 Code of Conduct

By opening, commenting on or reacting to issues here, you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md). Comments that are abusive, spam or share live exam content may be hidden, edited or locked.

## 🔒 Security

Found a security problem with the site or this repo? Please don't report it in a public issue. Use [Report a vulnerability](https://github.com/marcogrimaldi29/az-305-study-notes/security/advisories/new) instead, so only you and I can see it. The [security policy](SECURITY.md) has the details.

---

If the notes helped you, the README's [💚 Support](https://github.com/marcogrimaldi29/az-305-study-notes#-support) section has a couple of ways to show it. Thanks for helping make them better for the next AZ-305 candidate.
