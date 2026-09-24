<a href="https://batastankovic.com/"><img src="media/cover.jpg" alt="Bata Stanković PR, home page on a laptop and a phone" width="100%"></a>

# Bata Stanković PR

Site for a bookkeeping agency in Lebane, with verifiable company data, a contact form that really delivers and pages by type of client.

**[batastankovic.com](https://batastankovic.com/)** · [Case study (in Serbian)](https://svilenkovic.com/radovi/bata-stankovic) · [Srpski](README.sr.md)

> [!NOTE]
> Client project. The source code belongs to the client and stays in a private repository. This page describes what I built and how.

<table>
  <tr><td><b>Client</b></td><td>Bata Stanković PR</td></tr>
  <tr><td><b>Industry</b></td><td>Bookkeeping and accounting</td></tr>
  <tr><td><b>Location</b></td><td>Lebane, Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Multi-page website</td></tr>
  <tr><td><b>My role</b></td><td>Design, development, SEO, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>PHP 8.3, nginx, PHPMailer, Consent Mode v2</td></tr>
</table>

## About the project

Bata Stanković PR has kept the books for sole traders, flat-rate entrepreneurs and small companies around Lebane since 2014. Someone looking for a bookkeeper wants proof that the firm exists, a phone number and a way to ask one question. In the Jablanica district almost no agency has a proper website, only a line in a directory someone else filled in, so the site leads with registry data a client can check.

The most important find was a contact form that had not sent a single message for months. The required consent checkbox was hidden with `display: none`, so when validation failed the browser could not focus it and cancelled the submit. There was no network request and no visible error, only one line in a console nobody opens. The field now stays in the layout, invisible but focusable, and the path to the mailbox got its own fixes: raw values for the reply-to address, a spam gate that fails closed and a real error message when a send does not go through.

## What I built

- From three URLs to twelve: a services overview, five pages by client type, a price page, a Leskovac page and a 20-question FAQ
- About ninety comments in the code tying each claim about a deadline, rate or limit to the regulation and the date it was checked
- A price page without invented figures: it explains what the price depends on and reports no prices to search engines until the owner sets them
- Audit removed from the services, since in Serbia only licensed audit firms may offer it
- 'Knjigovodja' corrected to 'knjigovođa' in 18 places, and structured data given the real company name and the right VAT and registration fields
- The script cut from 31 to 20 KB, with static files cached for a year behind versioned URLs

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 96 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, September 2026. Security headers: 6 of 6. HTML validator: no errors. axe accessibility check: no violations. Structured data: `AccountingService`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Bata Stanković PR, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Bata Stanković PR, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="The &quot;Naše usluge&quot; (Our services) section: six services, each with a list of items">
<sub>The "Naše usluge" (Our services) section: six services, each with a list of items</sub>

<img src="media/inner-2.webp" alt="The &quot;Zašto odabrati nas&quot; (Why choose us) section: available weekdays 08-16, matching the structured data">
<sub>The "Zašto odabrati nas" (Why choose us) section: available weekdays 08-16, matching the structured data</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
