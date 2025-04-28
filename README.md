# AI-Agent-Tool: Website and LinkedIn Summarization with Ollama (Mistral Model)

This project scrapes a company's website and a LinkedIn profile, then summarizes both contents using a local LLM (Mistral) via Ollama.

---

## Final Results

### Website Summary:

> Loopio is an RFP automation platform that simplifies and streamlines the response management process, offering a secure content library and AI-powered features to help teams respond quickly and accurately to RFPs, RFIs, DDQs, and security questionnaires. With Loopio, teams can efficiently collaborate, ensure consistency across responses, and easily scale their approach. Loopio integrates with popular tools such as CRM systems, file drives, web browsers, Google, and Slack for seamless collaboration. The platform offers flexible pricing options to cater to organizations of all sizes and comes with a dedicated support team for technical help and strategic advice. Loopio's AI capabilities prioritize control in the hands of users and are guided by three main pillars: data-driven insights, human review, and quality control.

---

### LinkedIn Summary:

**1. Major Topics:**
- Machine Learning opportunities at Loopio
- Employee Appreciation Day at Loopio and reflection on the company's journey over 11 years

**2. Client News / Company Updates (Loopio):**
- Hiring for a Senior Machine Learning Engineer position based in Toronto, Canada (Remote)
- Celebrating the team and Employee Appreciation Day
- Discussing the company's growth and resilience through economic chaos and technological disruption

**3. Blog Posts:**
- No explicitly written blog posts. The posts appear more like internal messages or updates shared with team members.

**4. Important Announcements (Loopio):**
- No significant or explicit announcements made; content focused on company culture, team appreciation, and job opportunities.

---

## Technology Stack

- **Node.js** backend with **Express**
- **Puppeteer / Playwright** for website and LinkedIn scraping
- **Ollama** local server with **Mistral** model for LLM summarization
- **Typescript** based clean architecture

---

## Notes

- LinkedIn scraping works using authenticated cookies.
- Summarization uses prompts carefully designed for LLM to output structured, short summaries.
- No external APIs required (fully local using Ollama).

---

## How to Run

1. Start your Ollama server and ensure Mistral model is downloaded (`ollama run mistral`).
2. Start the backend server (`npm run dev` or equivalent).
3. Use CURL or Postman to POST to `/api/scrape`:
   ```bash
   curl -X POST http://localhost:3000/api/scrape \
   -H "Content-Type: application/json" \
   -d '{"companyUrl":"https://loopio.com/","linkedinUrl":"https://www.linkedin.com/in/myork/"}'
   ```
4. Receive website and LinkedIn summaries in JSON format.

---

## Status: 📅 Project Working Successfully!

---

# Thank you! 🚀
