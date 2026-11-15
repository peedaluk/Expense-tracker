# Hall Money Sorter

A small tool for sorting out past bank and credit card statements when hall money and personal money have been mixed in one account.

It runs **entirely on your own computer** in your web browser. Nothing is uploaded or sent anywhere, and it works without internet.

## How to open it

1. Download this `hall-money-sorter` folder. On GitHub: **Code → Download ZIP**, then unzip it.
2. Double-click `index.html`. It opens in Chrome, Edge or Firefox.

Keep `index.html` and the `vendor` folder together. The `vendor` folder holds the code that reads Excel files.

## How to use it

1. **Import statements.** Download your bank and credit card statements from net banking as **CSV or Excel** (PDF can't be read). Drop them into the page. For each file, check the preview, then compare the "total money out / in" with your statement.
2. **Sort one by one.** For each transaction, press:
   - **H** for hall money or hall spending
   - **P** for personal
   - **T** for a transfer, such as paying your credit card bill from your bank account (this stops the same spending being counted twice)
   - **S** to skip it for now

   Keep **"Remember"** ticked and every similar transaction (for example all "swiggy" ones) is sorted for you, including in files you import later.
3. **Split** anything that was partly for the hall, such as a cash withdrawal where you spent part on the hall and kept the rest.
4. **Add cash entries** for spending or hall money that never went through your account.
5. **Where the money stands** shows:
   - **Hall money received** (hall fund, fees, sponsors, refunds)
   - **minus hall spending** (bank + credit card + cash)
   - **= hall money you should still be holding**, or, if the figure is negative, **how much the hall owes you**

   Fill in "hall money already in your account before the first statement" if there was any.
6. Print the summary or save it as a PDF, and download the hall transactions as CSV for your records or the warden.

## Keep your work safe

Your work is saved in the browser automatically. Clearing browser data loses it, so use **Rules & backup → Download backup** regularly.

## Try it first

The `sample` folder has made-up statements, so you can practise before using your real ones. Use **Rules & backup → Erase everything** afterwards.

## Privacy

Don't commit your real statements or backup files to this repository. Keep them only on your computer.
