# Print jobs stuck in the queue

**For:** Service desk · **Applies to:** Windows 10/11, domain PCs

## Symptoms
- Nothing prints.
- Jobs sit in the print queue.
- Some jobs may be marked **Error**.

## Cause
A stuck job blocks everything behind it. Sometimes the printer itself is the problem: offline, out of paper, or jammed.

## Steps
1. **Check the printer** is on, online, and has paper.
2. **Check whether one user or several are affected.** If several, go to the **print server** and run the steps below there.
3. **Open the queue:** **Settings → Printers & scanners →** the printer **→ Open print queue** (on a print server, use **Print Management**). If one job is stuck at the top, cancel it.
4. Open `services.msc`, right-click **Print Spooler**, and choose **Restart**.
5. **If jobs are still stuck:**
   1. Stop **Print Spooler**.
   2. Delete all files in `C:\Windows\System32\spool\PRINTERS`. *This removes **every** waiting job, so let users know they'll need to print again.*
   3. Start **Print Spooler** again.
6. **Send a test print**, and confirm with the affected users that printing works.
7. **Document the ticket:** who was affected, the cause, and what you did.

## If that doesn't work
Check the **printer driver**; update or reinstall it if needed.

For **hardware errors** (jams, error lights), contact the printer supplier. Include:
- the printer name
- any **error code** shown on the printer's display
- what you've tried
