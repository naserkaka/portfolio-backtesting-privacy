---
layout: default
---

# Privacy Policy — Portfolio Backtesting

Last updated: 16 August 2026

## The short version

Portfolio Backtesting does not collect, transmit, store remotely, or sell any of your
data. It has no analytics and no accounts.

Your symbols, your scan results and everything read from a TradingView page
stay on your computer and are never transmitted anywhere. The extension makes
exactly one kind of network request, and only if you buy: it asks the payment
provider whether this installation has an active purchase. Nothing else is ever
sent, and a free installation never makes a request at all.

## What the extension does

Portfolio Backtesting reads the Strategy Tester report that TradingView renders in
your own browser tab, for each symbol in a list you provide, and shows those
numbers back to you as a table and a pooled summary.

## What is stored, and where

Everything the extension keeps is written to your browser's local extension
storage (`chrome.storage.local`) on your own machine:

- the symbol list you typed or imported
- the per-symbol backtest figures read from the Strategy Tester
- any runs you explicitly saved, and your scan settings
- if you bought: an identifier issued by the payment provider that links this
  installation to your purchase, and the email address you bought with

None of it leaves your computer, with the single exception described below.
Removing the extension deletes all of it, and "Clear results" empties the
results at any time.

## Network requests

**Free installs make no network requests at all.** The extension reads the page
TradingView has already rendered in your tab; it does not contact TradingView's
servers, or ours, or anyone else's. There is no remote code — everything that
runs is in the package you installed.

This is not a promise about intent — it is how the code behaves. Until an
installation has bought something it holds no purchase identifier, and the
check returns "not paid" without contacting anyone.

**If you buy**, the extension contacts the payment provider (ExtensionPay,
`extensionpay.com`) to confirm the purchase is current. That request contains:

- the identifier the provider issued for this installation when you bought
- unavoidably, as with any web request, your IP address and user agent, which
  the provider receives and handles under its own privacy policy

That request is made when you buy, when the dashboard is opened, and when you
press Refresh in the Licence card. **It never contains a symbol, a backtest
figure, a strategy name, a saved run, or anything read from a TradingView
page.** If the provider cannot be reached, your purchase keeps working for 30
days before the extension asks again.

**Payment itself happens outside the extension.** Upgrading opens
ExtensionPay's own checkout page in a normal browser tab. Card details are
entered there, handled by Stripe, and never pass through — or become visible
to — this extension.

If you use the CSV or Markdown export, the file is generated in your browser
and saved by your browser. It is not uploaded anywhere.

## Permissions, and why each is needed

| Permission | Why |
| --- | --- |
| `storage` | Keep your symbol list, results and saved runs on your machine between sessions |
| `tabs` | Find which of your open tabs are TradingView charts and screeners, so you can pick which one the scan drives |
| `scripting` | Load the extension's reader into a TradingView tab that was already open before the extension started |
| `*://*.tradingview.com/*` | Read the Strategy Tester panel and switch the chart's symbol. The extension runs on no other site |
| `https://extensionpay.com/*` | Confirm a purchase. This is a content script on the checkout page only — it is how that page tells the extension a payment succeeded. Never contacted by a free installation |

## Third parties

Two, and only once you buy:

**ExtensionPay** (<https://extensionpay.com/privacy>) hosts the checkout and
answers whether this installation has an active purchase. It receives the
installation's purchase identifier, the email you bought with, and the IP
address the request came from. It is handed no symbols, no results and nothing
read from a TradingView page.

**Stripe** (<https://stripe.com/privacy>) processes the payment itself on
ExtensionPay's checkout page and receives your payment details directly. Those
details never pass through this extension.

Nothing is sold to, or shared with, anyone else.

## Your TradingView account

The extension works inside your existing logged-in TradingView session in your
own browser, the same way you would by clicking through symbols yourself. It
does not read, store or transmit your TradingView credentials, and it has no
access to your account beyond the chart page you have open.

## Changes

Any change to this policy will be published here, and the "Last updated" date
above will change with it.

## Contact

Questions about this policy, or about what the extension does with your data:
naser.kakadost@hotmail.com

This is also the support address for the extension itself, including refunds
and purchases that didn't register.
