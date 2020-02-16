---
author: "Chris Walz"
date: 2020-02-16
linktitle: How to Download Robinhood Transaction History as a TSV
title: How to Download Robinhood Transaction History as a TSV
weight: 10
---

# How to Download Robinhood Transaction History as a TSV

I wanted to download a nicely formatted list of all my stock transactions (including dividends and cancelled transactions) but noticed there was no way doing that. I wrote up a little JavaScript code to quickly download the transaction list from Robinhood's website. 

Here's how to do it yourself: 

1. go to https://robinhood.com/account/history using Chrome

2. Scroll down to the bottom to where it says "Show more items" and click that button (so that all transactions are shown)

3. Open the Chrome Dev Tools window (Windows - Ctrl + Shift + I)

4. Paste this code into the console

   let csv = "Date\tType\tTotal\tTotal for Shares\tPrice per share\n"
   const sections = document.querySelectorAll('section')
   for (let i = 0; i < sections.length; i++) {
       ```const transactions = sections[i].querySelectorAll(':scope > div') // get direct children?
       for (let j = 0; j < transactions.length; j++) {
           const transaction = transactions[j].children[0].children[0];
           const date = transaction.children[0].innerText.split('\n')[1]
           const name = transaction.children[0].children[0].textContent
           const total = transaction.children[1].textContent.replace("+","");
           const pps = total.includes('shares') ? total.split(' shares at ')[0] : '';
           const numberOfShares = total.includes('shares') ? total.split(' shares at ')[1] : ''
           csv += ${date}\t${name}\t${total}\t${pps}\t${numberOfShares}\n
       }
   }
   console.log(csv);

   function download(content, fileName, contentType) {
       var a = document.createElement("a");
       var file = new Blob([content], {
           type: contentType
       });
       a.href = URL.createObjectURL(file);
       a.download = fileName;
       a.click();
   }
   download(csv, 'transactions.tsv', 'text/plain');```

   

5. Press ENTER

6. Your TSV should now download!

7. Then open in Google Sheets, Excel etc. 



# Concluding Thoughts

It was nice using my coding experience in the wild. Keep in the minds in generally not a good idea to copy and paste code into Dev Tools from strangers. 

If you're having trouble, you can use https://robinhood.com/contact to ask Robinhood directly for a spreadsheet of your transactions and they send one to you fairly promptly. 

