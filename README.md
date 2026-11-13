# WAHDAH subscription UI preview

[Open the deployed preview](https://ftthamr.github.io/wahdah-subscription-preview/)

A static, interactive design prototype using WAHDAH Singapore branding. The landing page links to vehicle selection, subscription plans and add-ons, customer details, approval overview, payment and a simulated confirmation.

## Run

Serve this directory with a static server, for example `python3 -m http.server 8765`, then open `http://localhost:8765/`. No build or backend is required.

## Design and data boundaries

- Existing sequence retained: vehicle -> plan and add-ons -> customer details -> review/approval -> payment.
- Original plan durations retained: 3, 6, 12, 36 and 60 months. Ioniq rates and its 36-month deposit are observed site examples. Unknown prices/deposits require a quote.
- Malaysia driving is included in every subscription price, as confirmed by the product owner. It is displayed as an included benefit, with no toggle, travel dates or separate surcharge. Cross-border terms still apply.
- Additional drivers cost SGD 10 each one-time, up to three, following the inspected site.
- Monthly and full-term payment options update the cost summary. Payment is presented after approval; payment methods and post-submission screens are proposed because the live flow could not be inspected beyond submission without creating a reservation.
- No backend, real application submission, document upload, sign-in or payment processor is connected. The guest form includes a sample-data button. Customer inputs stay in memory; only vehicle, term and add-on choices are stored in sessionStorage.
- No changes have been made to the production wahdah.sg website.

## Validation

Browser-tested plan/add-on changes, included Malaysia benefit with no surcharge, additional driver quantity, monthly/full-term totals, sample application progression, payment acknowledgement, simulated confirmation, SUV filtering and mobile continuation. Mobile 390px checks showed no horizontal overflow.

Optional child seat and Touch ’n Go card requests carry through the summary, approval and payment screens. Prices, availability, seat suitability and any TNG balance are to be confirmed. Selecting either makes the final payment amount quotation-dependent; no unconfirmed fee is assumed.
