# Mark Ridley’s Comedy Castle — Guest List Formatter

## Open the bookmarked link:

**GUEST LIST FORMATTER URL GOES HERE**

It opens in Chrome or Edge. No install needed.

Your guest list never leaves your computer. The page does all the work inside the browser and does not upload the file anywhere.

---

## What this does

This tool takes the eTix guest list CSV and makes a clean printout for the door, ticket, and showroom teams. 

It automatically adds the horizontal lines between guest parties, so no one has to draw them by hand.

---

## Quick start

1. Export the guest list from eTix as a **CSV**
2. Open the **Guest List Formatter** bookmark
3. Click **Choose File**
4. Select the CSV file you just downloaded
5. Make your selections at the top of the tool
6. Check the preview
7. Click **Print**

That’s it.

---

## Important first note

If the tool is not working and a show is coming up, stop troubleshooting and use the old guest-list process for that show.

Come back to the tool later when there is time.

---

## What the buttons mean

**Sort by Last Name**  

**Sort by Table Number**  

**Display Text Size**  
Normal or Larger
This effects the preview and the paper print out 

Need bigger text?
Use the Text Size option in the tool first.

If it still feels too small, click Print and adjust Scale in the print settings on your computer.

**Clear**  
Clears the current list so you can start fresh and upload again.

---

## Step 1 — Export the guest list from eTix

1. Sign in to eTix.
2. Open the correct event.
3. Go to the guest list screen.
4. Click **Export As** near the gray print button.
5. Choose **CSV**.  The first option.
6. Save the file somewhere easy to find, like **Downloads** or **Desktop**.

Important:

Do **not** open or edit the CSV before uploading it.

Just download it from eTix and upload it directly into this tool.

If your computer wants you to choose an application Excel and Notepad work.  

If you open the file in Excel do not ever change the formatting. 

This tool needs the standard order number data. 

---

## Step 2 — Open the formatter

1. Click the **Guest List Formatter** bookmark (or type the URL).
2. It should open in Chrome or Edge.
3. If it looks out of date, press **Ctrl+F5** to refresh.

---

## Step 3 — Upload the guest list

1. Click **Choose File**.
2. Select the eTix CSV file.
3. The formatted guest list will appear on the screen.

If you see an error, you may have uploaded the wrong file. Re-export the guest list from eTix as CSV and try again.

---

## Step 4 — Print

1. Click **Print**.
2. Select the correct printer.
3. Paper size should be **Letter**.
4. Turn off browser **Headers and footers** if extra browser text appears on the page.
5. Click **Print**.

---

## What the printout includes

The printout keeps the familiar eTix-style layout.

It includes:

- Show name
- Performance date and time
- Report created time
- Formatted by tool time
- Name, Section, Seat, and Order ID columns
- Divider lines between guest parties
- Page numbers

---

## Troubleshooting

### The file did not load

Make sure you uploaded the **guest list CSV** from eTix.

Do not upload a sales report, scan log, or other report.

---

### The printout has extra browser text at the top or bottom

In the print window, click **More settings** and turn off:

**Headers and footers**

---

### The page looks squeezed or spaced strangely

Make sure the paper size is set to:

**Letter**

---

### I opened the CSV by mistake

That is okay.

Do not edit it. Do not save it.

Go back to the formatter and upload the original CSV.

---

### PDF files

Use CSV.

PDF support is not the normal workflow and may not work reliably.

We can build it in later if desired. 

---

## For whoever maintains this (not needed for daily use)

The live site is everything in the `public/` folder. Nothing else gets published.

- `public/index.html`: the tool itself (one file, no build step)
- `vercel.json`: tells Vercel to serve `public/` and sets the security and caching headers
- `.vercelignore`: keeps `samples/` and any CSV from ever being uploaded to Vercel
- `public/robots.txt`: keeps search engines out
- `samples/`: real test exports. **Contains customer names. Never publish or commit it.** (`.gitignore` blocks it.)

To publish a change: edit `public/index.html`, test it by opening the file locally with a sample CSV, then push to git (Vercel redeploys automatically) or run `vercel --prod` from this folder.

If the site is down before a show, open `public/index.html` straight from this folder. It works offline the same way.

---

## Best rule to remember

Download the CSV from eTix.

Do not edit it.

Upload it into the tool.

Print.
