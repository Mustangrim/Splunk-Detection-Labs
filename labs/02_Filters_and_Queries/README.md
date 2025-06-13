# 🔍 Lab 02: Filters & Queries

## Goal

Understand how to filter events in Splunk using various time selectors and query techniques. Learn how to extract specific data using time filters, field filters, and metadata.

---

## Scenario

You're a SOC Analyst at **Buttercup Games**, using Splunk to monitor security events, web traffic, and application logs. This lab focuses on refining your ability to query and filter results effectively.

---

## Tools Used

- Splunk Time Picker
- Search Bar
- Event Timeline
- Field Sidebar

---

## Tasks & Concepts

### 1. Filtering by Time Range

<p align="center">
  <img src="../../assets/screenshots/time_picker_all_time.png" alt="All Time Picker">
  <br>
  <em>Setting Splunk to All Time for full event range</em>
</p>

<p align="center">
  <img src="../../assets/screenshots/search_failed_password_root.png" alt="Failed Password Search">
  <br>
  <em>Searching for 'failed password for root'</em>
</p>

---

### 2. Filtering by Date Range

- `"failed tomcat"` → before May 15, 2020  
- `"sshd session opened"` → May 17–23, 2020

<p align="center">
  <img src="../../assets/screenshots/date_range_filter_tomcat.png" alt="Tomcat Date Range Filter">
  <br>
  <em>Filtering failed tomcat logins before May 15</em>
</p>

<p align="center">
  <img src="../../assets/screenshots/sshd_session_opened_range.png" alt="SSHD Session Range">
  <br>
  <em>Filtering SSHD sessions from May 17 to 23</em>
</p>

---

### 3. Filtering by Date & Time Range

- `"Googlebot"` → between `May 1, 17:00` and `May 4, 08:00`  
- `"category.screen"` between `April 29, 14:00` to `14:30`

<p align="center">
  <img src="../../assets/screenshots/googlebot_search_result.png" alt="Googlebot Result">
  <br>
  <em>Result of Googlebot query in specific date-time range</em>
</p>

<p align="center">
  <img src="../../assets/screenshots/category_screen_april29.png" alt="Category Screen Results">
  <br>
  <em>Finding 'category.screen' activity on April 29</em>
</p>

---

### 4. Using Fields for Queries

- `sourcetype=access_combined_wcookie`  
- Refine by:
  - `action=purchase`
  - `referer_domain="http://www.google.com"`  
  - Time filter for May 18+

<p align="center">
  <img src="../../assets/screenshots/access_combined_wcookie_all.png" alt="Sourcetype All">
  <br>
  <em>Searching all access_combined_wcookie events</em>
</p>

<p align="center">
  <img src="../../assets/screenshots/action_purchase_filter.png" alt="Action Purchase">
  <br>
  <em>Filtering by action=purchase</em>
</p>

<p align="center">
  <img src="../../assets/screenshots/referer_google_filter.png" alt="Google Referer">
  <br>
  <em>Filtering purchases with Google referrer</em>
</p>

---

### 5. Exploring All Fields Panel

<p align="center">
  <img src="../../assets/screenshots/all_fields_panel_view.png" alt="All Fields Panel">
  <br>
  <em>Exploring All Fields in Splunk results</em>
</p>

---

## Summary

| Task                       | Covered |
|----------------------------|---------|
| Time filtering             | ✅      |
| Date range & exact time    | ✅      |
| Field-level queries        | ✅      |
| Search by metadata         | ✅      |
| All Fields panel usage     | ✅      |

---

## Reflection

Time and metadata filtering in Splunk lets analysts pinpoint relevant events in a sea of log noise. These techniques are the backbone of precise event analysis in any SOC.

---

**Next Lab →** [03 Fields & Transforms](../03_Fields_and_Transforms/README.md)
