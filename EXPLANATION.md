# Hisaab Saathi: project explanation

Use this for your report, viva or presentation. Read it aloud once and it will sound natural.

## 1. The problem

India has millions of small businesses: kirana shops, tailors, freelancers, small traders, cloud kitchens. Most of them must deal with GST, income tax and TDS, and all of it now happens online. The owner usually has no accounting background, so three things go wrong:

- They do not know which returns apply to them.
- They miss due dates and pay late fees and interest.
- They reach the filing portal without the right papers and have to stop halfway.

## 2. Our idea

Hisaab Saathi ("hisaab" means accounts, "saathi" means companion) is a simple website that answers three questions in plain language:

1. What do I need to file?
2. When is it due?
3. What papers do I need first?

It does not file returns. The government portals do that. Our site prepares the owner so filing is quick and stress-free.

## 3. The website, section by section

**Hero with a live GST invoice.** The first thing a visitor sees is a tax invoice they can edit. They type a price, pick a GST rate, say whether the customer is in the same state, and enter the GST they paid on purchases. The page shows the CGST and SGST split (or IGST for another state), the total the customer pays, and how much the owner actually pays the government after input tax credit. This explains GST by doing it, which is more convincing than a paragraph.

**Find my filings.** Four questions: kind of business, yearly turnover, whether they have a GST number, and whether they pay salaries or contractors. The page builds a personal list of filings such as GSTR-1 and GSTR-3B, ITR-4 or ITR-3, advance tax and TDS, each with a one-line reason. It uses rules for registration limits, presumptive taxation and audit limits.

**What is due next.** A countdown list of the usual statutory due dates, sorted by how soon they arrive, with filters for GST, TDS and Income tax. Anything within seven days is highlighted. The dates are calculated from today's date, so the list is always current.

**Paper to gather.** A checklist of sales, purchase, bank, login and payroll documents. A progress bar fills as the owner ticks items, the ticks are saved in the browser, and a red "Ready to file" stamp appears when everything is done.

**Questions owners ask.** Short answers about whether the site files returns, whether a Chartered Accountant is needed, what input tax credit means, whether UPI sales count, and what happens when a date is missed.

## 4. Why the design looks like this

The design borrows from the Indian *khata* (paper ledger) and the GST invoice. The invoice and results use ruled lines with a red margin line, like a ledger page. Navy is the ink, marigold is the highlight and teal means "done". The memorable element is the invoice in the hero. The rest of the page stays quiet so the content is easy to read for a busy shop owner. The layout works on a phone, because many owners will open it there.

## 5. Technology

- **HTML** for structure, with proper headings, labels and ARIA attributes for accessibility.
- **CSS** for the design, including a responsive layout and support for reduced-motion settings.
- **JavaScript** (no libraries) for the calculator, the finder logic, the date maths and the checklist. The checklist uses the browser's `localStorage`.
- **Render static site** for public hosting, deployed straight from a GitHub repository. No server is needed, so it is free and fast.

## 6. Who benefits

Small shop owners, freelancers and new entrepreneurs, and also family members who help with the books. It reduces missed deadlines and unnecessary visits to an accountant.

## 7. Limits and future work

- It gives guidance, not legal or tax advice. A Chartered Accountant should confirm edge cases.
- Rates, limits and due dates change, so they must be rechecked regularly. They are kept in one place in the script block of `index.html` for easy updating.
- Future work: Hindi and regional-language versions, reminders by WhatsApp or email, and downloadable checklists.

## 7a. Likely viva questions

**Why a static site?** The site needs no user accounts or stored data, so a static site is cheaper, faster and safer.

**Where does the data come from?** From the public rules on gst.gov.in and incometax.gov.in, written into the script as clear rules.

**Is user data stored?** No. Everything stays in the visitor's browser. Only the checklist ticks are saved, on their own device.

**How is it different from the government portal?** The portals let you file. Hisaab Saathi tells you what to file and prepares you for it, in simple words.
