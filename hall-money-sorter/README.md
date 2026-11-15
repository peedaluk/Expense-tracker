# Hall Money Sorter

A small tool for sorting out past bank and credit card statements when hall money and personal money have been mixed in one account.

It runs **entirely on your own computer** in your web browser and works without internet. Nothing is uploaded anywhere, except when you choose the optional AI sorting (see step 3).

## How to open it

1. Download this `hall-money-sorter` folder. On GitHub: **Code → Download ZIP**, then unzip it.
2. Double-click `index.html`. It opens in Chrome, Edge or Firefox.

Keep `index.html` and the `vendor` folder together. The `vendor` folder holds the code that reads Excel files and talks to the AI.

## How to use it

1. **Import statements.** Download your bank and credit card statements from net banking as **CSV or Excel** (PDF can't be read). Drop them into the page. For each file, check the preview, then compare the "total money out / in" with your statement.
2. **It sorts automatically.** As soon as you import, it sorts what it can on its own:
   - It **recognises common shops and payment types**: caterers, decorators, printing, DJ/sound, sports shops, trophies, Swiggy/Zomato (small orders = personal, big orders = maybe hall), Netflix, recharges, pocket money, hall fund/sponsor credits, and credit card bill payments (marked as transfers so nothing is counted twice).
   - It **learns from you.** Every time you sort one, similar transactions are sorted the same way.
   - It **spots collections.** If 3 or more people send you the exact same amount, it suggests that's hall fees.
   - **Confident guesses are applied. Less certain ones show up as suggestions** you accept with one click (or Enter).
3. **Optional: let AI sort the hard ones.** Add your own Anthropic API key in **Rules & backup → AI sorting**, and write a few lines about your hall (events and dates, vendors, who paid you hall fees). Then click **🤖 Sort unsure ones with AI**. Before anything is sent, the page shows you exactly what will go. Only the date, description, amount and in/out are sent. Reference, card and account numbers are removed first, and balances and files are never sent. You pay Anthropic directly; a few hundred transactions usually costs well under a dollar.
4. **Sort one by one.** On "Sort one by one", the **Unsure** list holds what's left, and **Auto-sorted, check** lets you quickly confirm what was sorted for you. Keys: **H** Hall, **P** Personal, **T** Transfer, **S** skip, **Enter** accept the suggestion.
5. **Split** anything that was partly for the hall, such as a cash withdrawal where you spent part on the hall and kept the rest.
6. **Add cash entries** for spending or hall money that never went through your account.
7. **Where the money stands** shows:
   - **Hall money received** (hall fund, fees, sponsors, refunds)
   - **minus hall spending** (bank + credit card + cash)
   - **= hall money you should still be holding**, or, if the figure is negative, **how much the hall owes you**

   Fill in "hall money already in your account before the first statement" if there was any.
8. **Your personal money** is tracked too: personal spending by category (food delivery, shopping, travel, recharges…) and by month. The **"How much of your bank balance is yours?"** box reads your bank balance from the statement and splits it into **hall money** and **your own money**. If your balance is less than the hall money you should be holding, it tells you how much hall money went on personal spending, which is the amount you'd need to put back. Hall and personal categories can be edited in **Rules & backup**.
9. Print the summary or save it as a PDF, and download the hall transactions as CSV for your records or the warden.

## Keep your work safe

Your work is saved in the browser automatically. Clearing browser data loses it, so use **Rules & backup → Download backup** regularly.

## Try it first

The `sample` folder has made-up statements, so you can practise before using your real ones. Use **Rules & backup → Erase everything** afterwards.

## Privacy

Don't commit your real statements or backup files to this repository. Keep them only on your computer.
