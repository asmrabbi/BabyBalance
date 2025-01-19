After completing initial data analysis and feasibility studies, the importance of the software has been realised and we started creating it in Python. Here are the key features that have been added to the software, 

## **BabyBalance Feature List**

1. **User Registration & Login**
    - **Superadmin** account (username: `superadmin`, password: `superadminpass`).
    - **Admin** and **normal** users.
    - **Admins** can manage other users’ data; **Superadmin** can promote users to admin.
2. **Multiple Babies per User**
    - Each user can manage **any number of babies**.
    - Data is stored as `data[username]["babies"][baby_name]`, allowing separate feeding/sleep records for each baby.
3. **Data Entry**
    - **Enter** feeding hours, sleeping hours, and (optionally) a date for each record.
    - **Console prompts** guide the user to pick which baby and input the day’s details.
4. **Viewing & Editing Records**
    - **List** all entries for a selected baby in chronological order.
    - **Edit** or **delete** specific entries by selecting them from the console list.
    - **Monthly Calendar** view, marking days with data and listing daily feeding/sleep totals.
5. **Advanced Analytics (NumPy + pandas)**
    - Summaries of **daily** feeding/sleep (totals per day).
    - **Mean** and **standard deviation (std)**, with a user-friendly explanation for how to interpret std.
    - Weekly aggregation (show total feeding/sleep each calendar week).
    - Helps parents see how consistent or variable the baby’s schedule is.
6. **Exporting Monthly Reports**
    - **CSV** or **PDF** (PDF requires the **ReportLab** library).
    - Summarize daily feeding/sleep with a comment (below/within/above ideal ranges).
    - Includes disclaimers about data sources and that admins do not alter user data.
7. **User Roles & Permissions**
    - **Superadmin** can create/promote admins, view or delete any user’s data, and fully remove users.
    - **Admins** can also view/edit/delete data for other users, but cannot create new admins.
    - **Normal Users** can only manage their own babies’ data.
8. **Notifications (Optional Interval)**
    - Users can set a **notification interval** (in minutes).
    - The application simulates “reminders” in the console every X minutes (printing a prompt to check baby data).
    - **Disable** by setting the interval to 0; the system stops notifications.
9. **Ideal Ranges for Feeding & Sleeping**
    - Default “ideal” intervals: **2.5–4 hours** feeding, **10–12 hours** sleeping per day.
    - Each day’s total is classified as below, within, or above these ranges (with helpful comments).
10. **Console-Based Interface**
- Straightforward menus for registering, logging in, selecting babies, analytics, exporting, etc.

---

### **Technology Requirements**

- **Python 3.7+**
- **Mandatory** libraries: **NumPy, pandas** (for daily/weekly grouping, advanced stats).
- **Optional** library: **ReportLab** (for PDF export).

With these features, **BabyBalance** can support **multiple children** per user, provide **robust analytics**, enforce **admin/superadmin** workflows, and offer **basic notifications** in a console environment.
