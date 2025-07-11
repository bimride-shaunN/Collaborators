# Timesheet – Google Analytics Skill: Custom Event Tracking via Google Tag Manager

## 📘 Task: Advanced Google Analytics Event Tracking  
**Skill Focus:** Setting up custom events in Google Analytics (GA4) using Google Tag Manager  
**Goal:** Capture meaningful user interactions (e.g., clicks, video plays, form submissions) that go beyond automatic tracking to deliver actionable behavioral data.

---

## 🧠 Why This Skill Matters

Standard GA tracking captures pageviews, sessions, and referrals. But to understand *how* users engage with your website, you need custom events.

Custom event tracking allows:
- Measuring conversions beyond pageviews  
- Tracking feature usage (e.g., downloads, video interactions)  
- Understanding engagement with CTAs or interactive content  
- Building custom reports and remarketing audiences

---

## 🔍 Research & Learning Process

- Watched YouTube tutorials on:
  - Creating variables and triggers in Google Tag Manager
  - Setting up GA4 tags with event parameters
  - Debugging tags using GTM Preview mode
- Followed Google Analytics Help Docs and Skillshop training
- Read blog guides from:
  - Simo Ahava (GTM/GA4 expert)
  - Analytics Mania
  - GA4 developer documentation

---

## ✍️ Practice Implementation

- Used a sample website with buttons, forms, and external links
- Set up GTM container and added GA4 tag with measurement ID
- Created click trigger for a “Sign Up” button with this configuration:
  - **Trigger Type**: Click – All Elements  
  - **Conditions**: Click Text equals "Sign Up"  
  - **Tag Type**: GA4 Event Tag  
  - **Event Name**: `sign_up_click`
  - **Parameters**: `button_location`, `page_path`

### Sample GA4 Tag Setup:

- Verified event firing using GTM’s Debug Mode  
- Confirmed event appeared in GA4 under real-time and “Events” report

---

## ⚠️ Challenges Faced

- Understanding the difference between GA4’s automatic events vs. custom events  
- Configuring GTM triggers correctly to avoid false positives  
- Debugging real-time data lag in GA4  
- Creating consistent naming conventions for event parameters

---

## 📂 GitHub Upload Plan

- Folder: `/google-analytics/custom-event-tracking/`
- Files:
  - `custom_events_ga4_gtm_notes.md` – walkthrough with screenshots
  - `gtm_event_config.json` – export of GTM container config (if needed)
  - `test_page_sample.html` – mock webpage for demo
  - `event_naming_convention_guide.md`

---

## ✅ Outcome

- Mastered event tracking via Google Tag Manager  
- Built reusable event tags for click tracking and micro-conversion analysis  
- Strengthened ability to translate business goals into measurable events  
- Ready to apply custom tracking in marketing, product analysis, or CRO work
