# Tools: Brian Campbell

## Tool Usage

### Connected Services

#### Calendar, Email and Personal Workspace

- **Google Calendar** (`google-calendar-api`): Primary calendar at brian.campbell@Finthesiss.ai. Custody handoffs, Gavin's school events, soccer games, the morning-run blocks, the standing 8:30 PM call with Yvette. Confirm CDT or CST before any new event.
- **Gmail** (`gmail-api`): Personal correspondence at brian.campbell@Finthesiss.ai. Drafts only unless Brian has approved a send. School, doctor bookings, retailers, and her birthday-dinner thread with Keisha.
- **Google Drive** (`google-drive-api`): Personal documents. Divorce decree PDF, school enrollment forms, the running Gulf Shores rental shortlist, scanned receipts she might want at tax time.
- **Outlook** (`outlook-api`): Read-only awareness for shared invites from the firm or Gavin's school when they arrive in non-Google format. Never linked to the work address.
- **Microsoft Teams** (`microsoft-teams-api`): Awareness only. Used by Ozark Legal for some external co-counsel meetings, accessed from the work computer.

#### Messaging, Calls and Notifications

- **Slack** (`slack-api`): Not used personally. Read-only awareness in case Keisha forwards a non-confidential thread from a vendor Brian is comparing.
- **WhatsApp** (`whatsapp-api`): The thread with Yvette and Marcus. Casual, short, no preamble. Photos of Gavin land here.
- **Discord** (`discord-api`): Not used by Brian. Available for monitoring the youth-soccer parents server Marcus joined to help coordinate carpools.
- **Telegram** (`telegram-api`): On standby if a contact migrates over from another platform.
- **Twilio** (`twilio-api`): Outbound SMS scaffolding for one-off reminders to Yvette about pickup times. Confirm before sending.
- **SendGrid** (`sendgrid-api`): Transactional email plumbing for any personal RSVP form or invite Brian runs. Low use.
- **Mailgun** (`mailgun-api`): Backup transactional sender for the same case. Low use.
- **Zoom** (`zoom-api`): The occasional virtual school meeting with Gavin's teacher, and the long-distance check-in with a cousin in Memphis. Never used for firm work.

#### Family Logistics, Home and Local

- **Google Maps** (`google-maps-api`): Routes between Hillcrest, downtown Little Rock, Pulaski Heights Elementary, Burns Park, and Pine Bluff. Custody-window drive times calculated in the active CT label.
- **Uber** (`uber-api`): Backup transportation when the RAV4 is at the shop. Confirm before booking; any ride above $30 stacks against the threshold for the day.
- **DoorDash** (`doordash-api`): Tacos from Taqueria Karina on a late-deadline night. Confirm if the total clears $30.
- **Instacart** (`instacart-api`): Kroger grocery runs the weeks the schedule will not allow a Sunday store trip. Confirm any order at or above the threshold.
- **OpenWeather** (`openweather-api`): Saturday hike go or no-go at Pinnacle, run cancellation calls on icy mornings, severe-weather alerts during custody handoffs.
- **Yelp** (`yelp-api`): Vetting a new restaurant before the monthly girls' night. Filter to small rooms and quieter back patios.
- **Zillow** (`zillow-api`): Casual watching of two-bedroom rentals in Hillcrest in case the next lease renewal goes the wrong direction. Not actively shopping.
- **Ring** (`ring-api`): No camera installed at the Hillcrest apartment. Awareness for the doorbell at Yvette's place in Pine Bluff when Gavin is staying there.

#### Health, Fitness, Reading and Entertainment

- **MyFitnessPal** (`myfitnesspal-api`): Light logging during TMJ flare weeks to track whether harder or chewier foods correlate. No calorie pressure; pattern-spotting only.
- **Strava** (`strava-api`): Morning-run mileage and pace. Three runs a week is the cadence to protect.
- **OpenLibrary** (`openlibrary-api`): Holds and queue management at the Central Arkansas Library System. Legal thrillers stay near the top.
- **Spotify** (`spotify-api`): The neo-soul, R&B, and hip-hop core, plus Gavin's Disney-soundtrack contamination. Morning-run playlist and the bedtime wind-down list.
- **YouTube** (`youtube-api`): Yoga videos for the at-home practice. Soccer clips Gavin asks to watch after dinner.
- **TMDB** (`tmdb-api`): What to add to the Netflix queue for the nights Gavin is at Derek's. Filter by limited series.
- **Vimeo** (`vimeo-api`): Continuing-legal-education videos from paralegal associations when the Ozark Legal benefits portal points at one.
- **Twitch** (`twitch-api`): On standby for any youth-streaming guidance Brian may want once Gavin is older.

#### Banking, Payments and Investments

- **Stripe** (`stripe-api`): Read-only awareness for any one-off invoice Brian may issue if she ever picks up paralegal contract work on the side. Not active.
- **Plaid** (`plaid-api`): Account-linking backbone behind any budgeting view that crosses Arvest, Ally, and Chase. Never authorizes a transfer without Brian's explicit go-ahead.
- **PayPal** (`paypal-api`): Splitting the birthday-dinner check with Keisha and the others. Confirm any send.
- **Square** (`square-api`): Awareness only. Used by the Mylo Coffee Co. counter she frequents.
- **QuickBooks** (`quickbooks-api`): On hand if she ever revisits the side-contract idea. Not active today.
- **Xero** (`xero-api`): Stands by as the alternative to QuickBooks for the same use case.
- **Coinbase** (`coinbase-api`): No crypto holdings. Disabled by default; do not initiate.
- **Alpaca** (`alpaca-api`): No brokerage activity outside the Ozark Legal 401(k). Disabled by default.
- **Binance** (`binance-api`): No holdings. Disabled by default.
- **Kraken** (`kraken-api`): No holdings. Disabled by default.

#### Shopping, Travel and Tickets

- **Amazon Seller** (`amazon-seller-api`): Awareness of seller-side data when comparing a third-party listing against the direct brand on a Gavin-clothing restock. Brian buys, never sells.
- **Etsy** (`etsy-api`): Birthday and Christmas gifts for Yvette, small-batch sellers. Confirm at threshold.
- **Pinterest** (`pinterest-api`): The someday Gulf-Shores beach-house board, the apartment-organization board, the meal-prep board she dips into on Sundays.
- **Instagram** (`instagram-api`): Following Keisha, Marcus, a handful of local Little Rock spots, and the youth-soccer league account. Read-only.
- **Amadeus** (`amadeus-api`): Drive-only is the default, so flight search stays quiet. Stands by for the rare Pine Bluff to Memphis route if a family event requires it.
- **Airbnb** (`airbnb-api`): The Gulf Shores and Destin beach-rental shortlist. Compare-only until PTO dates are confirmed.
- **Ticketmaster** (`ticketmaster-api`): Live-music nights at The Rev Room and the occasional larger show downtown. Confirm at threshold.
- **Eventbrite** (`eventbrite-api`): Local Black-business pop-ups and small-room shows Brian follows on weekends without Gavin.

#### Files, Notes and Signing

- **Dropbox** (`dropbox-api`): Backup of the divorce-decree PDF and Gavin's school-enrollment scans. Read-only by default.
- **Box** (`box-api`): On hand if a healthcare provider sends records through a Box link.
- **Notion** (`notion-api`): The personal life-admin workspace. Budget tracker, beach-trip plan, monthly girls'-night ideas, the running "things to teach Gavin" list.
- **Obsidian** (`obsidian-api`): Local-only vault with case-prep templates Brian has built for herself over the years. Never synced to the cloud.
- **Airtable** (`airtable-api`): The contact-sheet view of the stored Contacts when she wants to sort by birthday or last-contact date.
- **DocuSign** (`docusign-api`): Lease renewal, school permission slips, the occasional rental-car contract at the airport. Confirm every signature.
- **Contentful** (`contentful-api`): Stands by if Marcus's freelance client work needs a quick lookup.

#### Project, Office and Forms

- **Figma** (`figma-api`): Awareness only. Marcus uses it for a side project he occasionally asks Brian to proofread copy for.
- **Calendly** (`calendly-api`): Booking with Dr. Tran, Dr. Warren, and Dr. Hayes when their portals offer it. Never expose Brian's schedule publicly.
- **Typeform** (`typeform-api`): School photo forms, Burns Park soccer registration questions, the occasional client-intake form Julia asks Brian to test.
- **Monday** (`monday-api`): Awareness only. Not used personally; appears occasionally in vendor communication.
- **Asana** (`asana-api`): The personal-project board for the savings-cushion rebuild milestones.
- **Trello** (`trello-api`): The packing list and house-prep board for the Thanksgiving Pine Bluff trip.
- **Jira** (`jira-api`): Marcus's world, not Brian's, so the project tracker stays quiet here.
- **Linear** (`linear-api`): Same posture as Jira. Stays untouched because Brian's work is paper-based at the firm.
- **Confluence** (`confluence-api`): Read-only awareness of any wiki page Marcus links Brian to when she asks about his work.
- **Mailchimp** (`mailchimp-api`): Subscriptions to the Central Arkansas Library newsletter and the Hillcrest neighborhood association list. Manage preferences only.

#### CRM, Support and Marketing

- **HubSpot** (`hubspot-api`): Awareness only. Some firms in the personal-injury space use it; Brian may need to recognize the lead-form format.
- **Salesforce** (`salesforce-api`): Awareness only. Same recognition role across opposing-counsel intake.
- **Zendesk** (`zendesk-api`): Customer-support tickets when a streaming service or retailer disputes a charge. Confirm any refund request above threshold.
- **Intercom** (`intercom-api`): Same role as Zendesk for vendors that use it.
- **Freshdesk** (`freshdesk-api`): Same role as Zendesk for vendors that use it.
- **Klaviyo** (`klaviyo-api`): Read-only. Most of her retailer email lives behind a Klaviyo flow.
- **ActiveCampaign** (`activecampaign-api`): Same as Klaviyo. Subscription management only.

#### Engineering, Analytics and Web

- **GitHub** (`github-api`): Read-only. Watching Marcus's two side-project repos so Brian has something specific to ask about at Sunday dinner.
- **GitLab** (`gitlab-api`): Read-only. Same role for the one repo Marcus mirrors there.
- **Sentry** (`sentry-api`): Stays quiet here. Recognition only if Marcus mentions an alert he is chasing.
- **Datadog** (`datadog-api`): Same recognition posture as Sentry. Stays quiet because Brian is not on call.
- **PagerDuty** (`pagerduty-api`): On hand for awareness of Marcus's on-call weeks so Brian does not over-book family time.
- **Okta** (`okta-api`): Awareness only. Ozark Legal moves through a single-sign-on portal Brian touches from the work computer.
- **Cloudflare** (`cloudflare-api`): Stands by if her personal email domain ever needs DNS changes.
- **Kubernetes** (`kubernetes-api`): Marcus's world, not Brian's, so the cluster admin layer stays untouched.
- **Segment** (`segment-api`): Could handle analytics routing, but Brian runs no personal site that needs it.
- **Amplitude** (`amplitude-api`): Same posture as Segment. Stays quiet because there is no product to instrument.
- **PostHog** (`posthog-api`): Same posture as Segment. Stays quiet for the same reason.
- **Mixpanel** (`mixpanel-api`): Same posture as Segment. Stays quiet for the same reason.
- **Google Analytics** (`google-analytics-api`): Read-only awareness if Marcus shares a dashboard from his freelance client work.
- **Algolia** (`algolia-api`): Configured for any paralegal-association site Brian uses that runs Algolia search.
- **Webflow** (`webflow-api`): Stands by if Marcus's freelance work needs proofreading.
- **WordPress** (`wordpress-api`): Read-only. The Hillcrest neighborhood news site runs on it.

#### HR, Education, Public Knowledge and Social

- **BambooHR** (`bamboohr-api`): Read-only access to the Ozark Legal HR portal for PTO balance, benefits enrollment, and W-2 download.
- **Gusto** (`gusto-api`): Pay-stub history. Confirm before any direct-deposit change.
- **Greenhouse** (`greenhouse-api`): Stands by if Brian ever decides to look at the senior-paralegal market in central Arkansas.
- **ServiceNow** (`servicenow-api`): Awareness only. Some larger opposing firms route discovery requests through it.
- **Google Classroom** (`google-classroom-api`): Pulaski Heights Elementary uses it for second-grade assignments. Read-only, to keep an eye on Gavin's reading-log streak.
- **NASA** (`nasa-api`): The Astronomy Picture of the Day Gavin gets shown over breakfast on slow Saturdays. He likes the rover photos.
- **Twitter** (`twitter-api`): Read-only. Following a handful of central Arkansas reporters and the Pulaski Heights school account.
- **LinkedIn** (`linkedin-api`): Updated for visibility, not for active job hunting. Connections to paralegal-association contacts only.
- **Reddit** (`reddit-api`): r/Parenting and r/LittleRock for the occasional question Yvette is too far from the city to answer.

#### Storefront and Shipping

- **BigCommerce** (`bigcommerce-api`): Awareness only. Some Little Rock small-business storefronts run on it.
- **WooCommerce** (`woocommerce-api`): Same recognition role.
- **FedEx** (`fedex-api`): Tracking Yvette's birthday packages and the occasional case-file overnight to opposing counsel that Brian initiates from the work computer.
- **UPS** (`ups-api`): Tracking for Amazon and Target orders that ship to the apartment.
- **Shippo** (`shippo-api`): On hand if Brian returns a misordered item that needs a label printed.

#### Not Connected

- Live web search, web browsing, and deep internet research are not available. The agent works only from the connected services listed above and from stored memory.
- `bcampbell@ozarklegalsolutions.com`. The work email is locked to the firm's machine and stays out of OpenClaw entirely.
- Ozark Legal Solutions internal systems. The case-management database, the document-management vault, and the firm's billing system are firm-side only, regardless of session context.
- OurFamilyWizard. The co-parenting app stays phone-only. Drafts for Derek are prepared as plain text for Brian to paste in herself.
- Banking apps. Arvest Bank, Ally, and Chase are handled on Brian's phone. OpenClaw never authorizes a transfer.
- Derek's accounts of any kind. He sits outside the data perimeter, full stop.
- Gavin's accounts. School logins, doctor portals, and any future personal accounts of his stay with Brian directly.
- Pulaski Heights Elementary parent portal. Read-only awareness through Google Classroom only; no direct portal connection.
