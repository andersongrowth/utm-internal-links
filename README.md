# UTM Internal Links

Automatically appends UTM parameters to all internal links via JavaScript — keeping your HTML clean for Googlebots while enabling full click tracking in GA4.

---

## How it works

The plugin intercepts clicks on internal links and appends UTM parameters to the URL before navigation occurs. The HTML source remains untouched, so search engine crawlers always see clean canonical URLs. UTMs are only added at the moment a real user clicks a link.

## Features

- UTM parameters applied via JavaScript — invisible to Googlebots
- Works across all internal links: navigation menus, post content, widgets, and dynamically added links
- Supports `utm_source`, `utm_medium`, `utm_campaign`, and `utm_content`
- `utm_content` auto-fills with the link's anchor text if left empty
- Does not overwrite UTM parameters already present on a link
- Handles `target="_blank"` links correctly
- MutationObserver support for AJAX-loaded content and infinite scroll
- Interactive admin panel with a live browser preview — hover over links to see the UTM in real time, no need to save first

## Installation

1. Download the latest `.zip` from the [Releases](../../releases) page
2. In your WordPress admin, go to **Plugins → Add New → Upload Plugin**
3. Upload the `.zip` file and activate the plugin
4. Go to **Settings → UTM Internal Links** to configure your parameters

## Configuration

| Parameter | Description | Default |
|---|---|---|
| `utm_source` | Traffic source | `site` |
| `utm_medium` | Media channel | `internal` |
| `utm_campaign` | Campaign name | `navegacao` |
| `utm_content` | Link identifier — leave empty to use anchor text automatically | *(auto)* |

## Why this matters for GA4

Without UTMs on internal links, GA4 cannot distinguish which specific link drove a user to a page. With this plugin, you can:

- Isolate internal traffic as its own channel in acquisition reports
- Compare performance across different CTAs using `utm_content`
- Build internal funnels to understand which posts lead users toward conversion pages
- Optimize anchor text and link placement based on real click data

## Requirements

- WordPress 5.8 or higher
- PHP 7.4 or higher

## License

[GPL v2 or later](https://www.gnu.org/licenses/gpl-2.0.html)

---

Made by [Anderson Porangaba](https://www.linkedin.com/in/anderson-porangaba)
