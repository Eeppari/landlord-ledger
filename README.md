# Landlord Ledger

A small bookkeeping tool for people who rent out one to five properties. It keeps track of who pays what, which rent is late, what the property costs, and what the year looks like before tax.

Status: working prototype (MVP). It runs as a single web page with example data. There are no accounts yet, and nothing leaves your browser.

## What it does

**Overview**
- Rent received this month, overdue amounts, costs so far this year, and rent minus costs.
- A "Needs attention" list of unpaid or part-paid months, with buttons to write a reminder or record a payment.
- Reminder messages in English or Finnish, ready to copy.

**Rent**
- A grid of the last six months per property, with status: Paid, Late, Part paid or Due.
- A form to record a payment (property, month, amount, date received).
- A "Payments received" list with filters for property and month, and sorting by date or amount.

**Costs**
- Costs so far this year, per property.
- Monthly maintenance charge (hoitovastike): enter each property's amount once, then add a month with one click, or add it for all properties at once.
- A form for other costs (repairs, insurance, water charge, loan interest, cleaning, other) and a list of them.

**Properties**
- Searchable cards, filterable by building type.
- Building types: apartment, studio, row house, detached house, semi-detached house, cottage, commercial space, garage or parking, other.
- Each property has a name, address, tenant, monthly rent, due day (1 to 28) and deposit.
- Open a card to see that property's status, rent history, payments, costs and details.

**Tenants**
- Searchable tenant profiles: name, phone, email, lease start date, reminder language and notes.
- Create tenants first, then choose them from the "Who lives here" list inside a property.
- A tenant profile shows which property they are in.

**Tax summary**
- Rent received and costs by category for a chosen year.
- Profit before tax and an estimate of tax at a rate you set (default 30%).
- A plain-text summary you can copy.

## How to use it

1. Open the page. It starts with example data, marked with an "Example data" badge.
2. Click "Start empty" at the bottom to clear the examples.
3. Add your tenants in the Tenants tab.
4. Add your properties in the Properties tab and choose a tenant for each.
5. Record rent as it arrives in the Rent tab, and add costs in the Costs tab.
6. Check the Overview for anything late, and the Tax summary at the end of the year.

"Load example data" brings the examples back at any time. It replaces what is currently in the page.

## Where your data is stored

Everything is saved in your own browser (local storage) on the device you are using. This means:
- Another device or another browser starts empty.
- Clearing your browser data deletes your records.
- There is no backup. Do not rely on this version as your only record.

## Good to know

- The tax figure is a rough estimate. Payments are counted by the date you received them. Which costs are deductible, and the right rate, depend on your situation. Check with the tax authority or an accountant before filing.
- Amounts are in euros.
- The example data is invented. Names, addresses, phone numbers and emails in it are fictional.
- Reminder messages still end with a placeholder for your name ("[Your name]" or "[Nimesi]"), which you replace by hand.

## Upcoming features

Planned, not built yet. The first two are the next priorities.

1. **User accounts and sign-in.** Create an account and sign in, with sign-in methods that can be linked to the same account. Your properties, tenants, payments and costs are linked to your account instead of one browser, so they follow you across devices.
2. **Your name in reminders, applied automatically.** Reminders use the name on your account as the sender, so the "[Your name]" and "[Nimesi]" placeholders go away. Possibly also your phone number or email as contact details.
3. Sync and backup across devices, with an export of all your data.
4. Bank statement import that matches incoming payments to the right property and month.
5. Reminders sent by email or text message directly from the tool.
6. A tax report in the format the tax authority expects, and a yearly summary per property.
7. Storing documents per property and tenant, such as the lease and the deposit receipt.
8. Rent increases: a reminder when an increase is due and a record of past rents.

## Technical notes

- One self-contained HTML file with plain JavaScript. No framework and no build step.
- Fonts are loaded from Google Fonts. Everything else is inline.
- Data is kept in local storage under one key, with a version number so older saved data is converted when the structure changes.
- Light and dark themes follow the device setting.

## Disclaimer

This is a prototype for testing the idea. It is not accounting, legal or tax advice.
