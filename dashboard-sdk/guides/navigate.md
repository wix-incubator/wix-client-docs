# navigate

> **Deprecated**:
>
> This function will continue to work, but a [newer version](https://dev.wix.com/docs/sdk/api-reference/dashboard/navigate) is available in the `@wix/dashboard` module.

Navigates the user to another page in the dashboard.

If an invalid `pageId` value is passed to this function, a "Page Not Found" message is displayed in the dashboard.

## Syntax

```ts
navigate(pageId)| void
```

## Parameters

| Name     | Type   | Description                                                                                    |
| :------- | :----- | :--------------------------------------------------------------------------------------------- |
| `pageId` | string | ID of the page to navigate to. Use the [Page IDs](#page-ids) table to find the appropriate ID. |

## Returns

void

## Examples

**Navigate to the dashboard home page**

```ts
import { navigate } from '@wix/dashboard-sdk';

navigate(`home`);
```

## Page IDs

This table lists the IDs for the pages in the dashboard that you can navigate to. If you can't the ID for the page you need, please reach out to [Dashboard SDK Support](https://devforum.wix.com/kb/en/contact) for assistance.

| Page Name                                           | Page ID                                                      |
| --------------------------------------------------- | ------------------------------------------------------------ |
| Challenges                                          | `challenges-web-business-manager`                            |
| Home                                                | `home`                                                       |
| BusinessOverview                                    | `business-overview`                                          |
| Settings                                            | `settings-lazy-module`                                       |
| SiteSettings                                        | `site-settings-lazy-module`                                  |
| DeprecatedSiteSettings                              | `site-settings-lazy-module-old`                              |
| Gdpr                                                | `gdpr-users-client-page-component`                           |
| Engage                                              | `engage`                                                     |
| InboxSettings                                       | `inbox-settings`                                             |
| ChatDashboard                                       | `chat-dashboard`                                             |
| ChatDashboardInstallationEntry                      | `chat-dashboard-installation-entry`                          |
| Notes                                               | `notes.lazy-component`                                       |
| PriceQuotes                                         | `price-quotes`                                               |
| Invoices                                            | `invoices`                                                   |
| RecurringInvoices                                   | `CRM_FINANCIAL_RECURRING_INVOICES.pages.index`               |
| RecurringInvoicesForm                               | `CRM_FINANCIAL_RECURRING_INVOICES.pages.form.index`          |
| PartnersRecurringInvoicesForm                       | `CRM_FINANCIAL_RECURRING_INVOICES.pages.partners-form.index` |
| Integrations                                        | `integrations`                                               |
| InvoicesSettings                                    | `invoices-settings`                                          |
| Stores                                              | `ecom`                                                       |
| StoresTax                                           | `stores.tax`                                                 |
| StoresOrdersManager                                 | `stores-orders-manager`                                      |
| EcomGiftCards                                       | `rise-client-dashboard.pages.index`                          |
| EcomGiftCardsManagment                              | `rise-client-dashboard.pages.gift-card-sales`                |
| StoresFulfillmentServices                           | `stores-fulfillment-services`                                |
| StoresAbandonedCarts                                | `stores.abandoned-carts`                                     |
| StoresProductList                                   | `wixstores-dashboard-product-list.pages.index`               |
| StoresSalesChannels                                 | `stores.sales-channels`                                      |
| StoresInkfrog                                       | `stores.inkfrog`                                             |
| StoresAmazon                                        | `stores.amazon`                                              |
| StoresWish                                          | `STORES_CHANNELS_UI.pages.index`                             |
| StoresInventory                                     | `wixstores-dashboard-inventory.pages.index`                  |
| StoresPos                                           | `stores.pos`                                                 |
| StoresShipping                                      | `stores.shipping`                                            |
| StoresBackInStock                                   | `WIXSTORES_DASHBOARD_BACK_IN_STOCK.pages.index`              |
| StoresManualOrder                                   | `wixstores-dashboard-create-manual-order-pages-index`        |
| Shoutout                                            | `shoutout`                                                   |
| ShoutoutCompliance                                  | `shoutout-compliance`                                        |
| PromoteSeo                                          | `PromoteSeoLazyComponent`                                    |
| Cashier                                             | `cashier-merchant-settings`                                  |
| CashierPaymentsDashboard                            | `cashier-payments-dashboard`                                 |
| AppMarket                                           | `app-market-lazy-page-component`                             |
| AppMarketMyApps                                     | `app-market-my-apps-component`                               |
| Bookings                                            | `bookings-lazy-module`                                       |
| BookingsStaffList                                   | `bookings-staff-list-lazy-component-id`                      |
| BookingsStaffDetails                                | `bookings-staff-details-lazy-component-id`                   |
| BookingsBookingPolicyDetails                        | `bookings.bookings-policy-lazy`                              |
| BookingsSessionDetails                              | `bookings-session-details-lazy-component-id`                 |
| BookingsCourseDetails                               | `bookings-course-details-lazy-component-id`                  |
| BookingsManageParticipants                          | `bookings-calendar-modals-statics-pages-manage-participants` |
| BookingsCalendar                                    | `bookings-calendar-lazy-component-id`                        |
| BookingsFormSettings                                | `bookings.bookings-form-lazy`                                |
| BookingsFormSettingsPage                            | `bookings.bookings-form-page`                                |
| BookingsServiceForm                                 | `bookings.bookings-service-form-lazy`                        |
| BookingsSettingsPage                                | `bookings.bookings-settings-page-lazy`                       |
| BookingsRWGPage                                     | `bookings.bookings-reserve-with-google-lazy`                 |
| BookingsAnywhereSchedulingPage                      | `bookings-anywhere-scheduling-page-lazy-component-id`        |
| ContactBookings                                     | `bookings.contact-bookings-lazy`                             |
| Contacts                                            | `contacts-page-component`                                    |
| ContactsSegments                                    | `contacts-segments-page`                                     |
| MemberPermissions                                   | `member-permissions`                                         |
| WixForms                                            | `form-builder-component`                                     |
| Seo                                                 | `seo-page-component`                                         |
| SocialBlog                                          | `social-blog`                                                |
| Blog                                                | `blog-page-component`                                        |
| OldBlogUpdate                                       | `old-blog-update`                                            |
| Triggers                                            | `triggers-page-component`                                    |
| AutomationWizard                                    | `triggers-wizard-page-component`                             |
| Example_React                                       | `demo-react-lazy`                                            |
| Example_Angular                                     | `demo-angular-lazy`                                          |
| Etpa_Container                                      | `etpa-container-lazy-module`                                 |
| Coupons                                             | `coupons`                                                    |
| DiscountRules                                       | `discount-rules.pages.index`                                 |
| DiscountRule                                        | `discount-rules.pages.rule.id`                               |
| DiscountNewRule                                     | `discount-rules.pages.new-rule`                              |
| Restaurants                                         | `restaurants`                                                |
| CodeEmbed                                           | `code-embed-lazy-page-component`                             |
| Events                                              | `events`                                                     |
| MusicManagerMyAlbums                                | `music-manager.my-albums`                                    |
| VideoLibrary                                        | `video.video-library-lazy-page`                              |
| VideoMaker                                          | `video-editor.videos`                                        |
| PhotoAlbums                                         | `photography-albums-id`                                      |
| ArtStoreMain                                        | `ART_STORE_MAIN`                                             |
| ArtStoreChooseProvider                              | `ART_STORE_CHOOSE_PROVIDER_COMPONENT`                        |
| Multilingual                                        | `multilingual-homepage`                                      |
| MarketingIntegration                                | `MarketingIntegrationLazyComponent`                          |
| WixCodeDatabase                                     | `wix-databases-lazy-page-component-id`                       |
| WixPaymentsTransactions                             | `wix-payments-transactions`                                  |
| WixPaymentsAccount                                  | `wix-payments-account`                                       |
| WixPaymentsPayouts                                  | `wix-payments-payouts`                                       |
| WixPaymentsPayables                                 | `wix-payments-payables`                                      |
| WixPaymentsTaxDocs                                  | `wix-payments-tax-docs`                                      |
| AdminPage                                           | `admin-pages`                                                |
| TasksWeb                                            | `tasks-web`                                                  |
| TransactionalEmails                                 | `transactional-emails`                                       |
| TransactionalEmailsComposer                         | `transactional-emails-composer`                              |
| TeSmartActionsWidget                                | `te-smart-actions-widget`                                    |
| Membership                                          | `membership-lazy-component`                                  |
| StaffManagement                                     | `staff-management.pages.index`                               |
| MembershipSettings                                  | `membership-settings-lazy-component`                         |
| BadgeDefinitions                                    | `members-badges-bm-client-pages-index`                       |
| MembersAccountBm                                    | `MEMBERS_ACCOUNT_BM.pages.index`                             |
| ShareitWeb                                          | `share-it-web-lazy-component`                                |
| LogoBuilderLandingPage                              | `logo-builder-landing-page-lazy-component-id`                |
| Workflow                                            | `workflow-component`                                         |
| Platforms101Workshop                                | `platforms-workshop-page-id`                                 |
| PromoteHome                                         | `PromoteHomeLazyComponent`                                   |
| MyCampaigns                                         | `ascend-pages.my-campaigns`                                  |
| PingSettingsPageComponent                           | `ping-settings-lazy-page-component-id`                       |
| PingCustomerSettingsPageComponent                   | `ping-customer-notifications-lazy-page-component-id`         |
| SiteSubscriptions                                   | `site-subscriptions-lazy-component`                          |
| VideoMakerHome                                      | `video-maker-home`                                           |
| ReleaseManagerHome                                  | `release-manager-client-lazy-component-id`                   |
| WixCodeSiteMonitoringSettings                       | `wix-code-site-monitoring-lazy-component-id`                 |
| WixCodeSecretsManagerHome                           | `wix-code-secrets-manager`                                   |
| WixCodeSiteBranches                                 | `wix-code-site-branches`                                     |
| WixCodePlatformVisibilityHome                       | `wix-code-platform-visibility-bm.pages.index`                |
| PromotePaidAds                                      | `PromoteCampaignsLazyComponent`                              |
| GoogleMyBusiness                                    | `GoogleMyBusiness`                                           |
| ContactsImport                                      | `contacts-import-page`                                       |
| ContactFullPage                                     | `contact-full-page`                                          |
| WixPhotoAlbumsMain                                  | `albums-business-manager`                                    |
| WixExpertsDashboardMain                             | `experts-dashboard-news`                                     |
| WixExpertsDashboardBetas                            | `experts-dashboard-betas`                                    |
| WixExpertsResources                                 | `experts-resources`                                          |
| WixPartnerDealsPageComponent                        | `partner-deals`                                              |
| WixExpertsStudioHome                                | `experts-studio-home`                                        |
| WixExpertsSettings                                  | `experts-settings.pages.index`                               |
| WixExpertsClientBillingOverview                     | `experts-client-billing.pages.index`                         |
| WixExpertsProposals                                 | `partner-proposals`                                          |
| WixExpertsLoyaltyHome                               | `experts-loyalty-business-manager`                           |
| WixExpertsPartnerProgramEarnPoints                  | `experts-loyalty-ng.pages.earn-points`                       |
| WixExpertsPartnerProgramBenefits                    | `experts-loyalty-ng.pages.benefits`                          |
| WixExpertsPartnerProgramPointsHistory               | `experts-loyalty-ng.pages.points-history`                    |
| WixExpertsPartnerProgramRevenueShare                | `experts-loyalty-ng.pages.revenue-share`                     |
| WixExpertsPartnerProgramRevenueSharePaymentMethod   | `experts-loyalty-ng.pages.payment-method`                    |
| WixExpertsPartnerProgramRevenueShareNG              | `experts-rev-share.pages.index`                              |
| WixExpertsPartnerProgramRevenueSharePaymentMethodNG | `experts-rev-share.pages.payment-method`                     |
| AscendZeroStateInBizMgr                             | `ascend-zero-state-in-biz-mgr`                               |
| Analytics                                           | `analytics.analytics-lazy-page`                              |
| AnalyticsStats                                      | `analytics.analytics-stats-lazy-page`                        |
| AnalyticsReports                                    | `analytics.analytics-reports-lazy-page`                      |
| PromoteSeoPatterns                                  | `promote-seo-patterns`                                       |
| PromoteSeoTools                                     | `promote-seo-tools`                                          |
| LogoBuilder                                         | `logo-builder-biz-mgr`                                       |
| PrintShop                                           | `print-shop-biz-mgr`                                         |
| RicosPlayground                                     | `RICOS_PLAYGROUND.pages.index`                               |
| MobileTab                                           | `mobile_tab_bm`                                              |
| MobileTabNew                                        | `new-mobile-tab`                                             |
| SocialGroupsDashboard                               | `social-groups-dashboard`                                    |
| MarketplaceContainer                                | `app-market-lazy-page-component`                             |
| RestaurantsCallCenter                               | `restaurants-call-center`                                    |
| VirtualNumbers                                      | `virtual-numbers`                                            |
| Forum                                               | `communities-forum`                                          |
| ForumSettings                                       | `communities-forum-settings`                                 |
| ForumCategories                                     | `communities-forum-categories`                               |
| RolesAndPermissions                                 | `site-roles-and-permissions`                                 |
| WixPartnersTeam                                     | `partners-team`                                              |
| CoBranding                                          | `co-branding`                                                |
| Subscriptions                                       | `subscriptions-bm`                                           |
| StoresExploreProducts                               | `stores-explore-products`                                    |
| Arena                                               | `arena-biz-manager`                                          |
| ManageInstalledApps                                 | `app-market-my-apps-component`                               |
| AnalyticsNgBm                                       | `analytics-ng-bm`                                            |
| AnalyticsNgTools                                    | `analytics-ng-tools`                                         |
| AnalyticsNgPerformance                              | `analytics-ng-performance`                                   |
| AnalyticsNgCustomReports                            | `analytics-ng-custom-reports`                                |
| AnalyticsNgNativeOverviews                          | `analytics-ng-native-overviews`                              |
| AnalyticsNgNativeOverviewsBehavior                  | `analytics-ng-bm.pages.overviews.behavior`                   |
| SiteHistory                                         | `site-history-client`                                        |
| RestaurantsSocialBar                                | `restaurants_social_bar`                                     |
| RestaurantsReservations                             | `restaurants_reservations`                                   |
| RestaurantsOrders                                   | `restaurants_orders`                                         |
| RestaurantsIntegrations                             | `restaurants-integrations`                                   |
| RestaurantsReservationsSettings                     | `restaurants-reservations-settings-v2`                       |
| RestaurantsTableReservations                        | `table-reservations-bm-pages-table-reservations`             |
| RestaurantsTableReservationsSettings                | `table-reservations-bm-pages-table-reservations-settings`    |
| RestaurantsTableReservationsAdvancedSettings        | `table-reservations-bm-pages-advanced-settings`              |
| CookieConsentBannerSettings                         | `cookie-consent-settings-app`                                |
| ConsentLog                                          | `consent-log-page`                                           |
| CrmHome                                             | `crm-home`                                                   |
| FedataIndex                                         | `yoshi-flow-bm-demo.pages.index`                             |
| SettingsLobby                                       | `settings-lobby`                                             |
| FedataContacts                                      | `yoshi-flow-bm-demo.pages.contacts`                          |
| LanguageAndRegion                                   | `language-and-region-lazy`                                   |
| WebsiteSettings                                     | `website-settings-lazy`                                      |
| BusinessInfo                                        | `business-info-lazy`                                         |
| LiveVideo                                           | `LIVE_VIDEO.pages.index`                                     |
| PartnersPackage                                     | `partners-package-lazy-component`                            |
| Loyalty                                             | `loyalty-bm-pages-index`                                     |
| LoyaltyManage                                       | `loyalty-bm-pages-manage`                                    |
| LoyaltyWizard                                       | `loyalty-bm-pages-wizard`                                    |
| LoyaltyEmailAutomations                             | `loyalty-bm-pages-email-automations`                         |
| FAQPage                                             | `faq-page-bm.pages.index`                                    |
| MyMailboxes                                         | `MY_MAILBOXES_SITE_LEVEL.pages.index`                        |
| BrandedApps                                         | `BRANDED_APPS.pages.welcome`                                 |
| WebsiteChannel                                      | `website-channel-page`                                       |
| NewMobileTab                                        | `new-mobile-tab.pages.index`                                 |
| MyDomains                                           | `MY_DOMAINS_IFRAME_WRAPPER.pages.index`                      |
| SsoSettings                                         | `sso-settings-client.pages.index`                            |
| CryptoNft                                           | `crypto-nft-dashboard.pages.index`                           |
| DinersModeration                                    | `diners-moderation-bm.pages.index`                           |
| DinersModerationDetails                             | `diners-moderation-bm.pages.details`                         |
| DiscoveryModeration                                 | `discovery-moderation-bm.pages.index`                        |
| DiscoveryModerationDetails                          | `discovery-moderation-bm.pages.details`                      |
| Portfolio                                           | `portfolio.pages.index`                                      |
| Reviews                                             | `wix-reviews.pages.index`                                    |
| SitesList                                           | `sites-list-client`                                          |
| ApesPmFlow                                          | `crm-automations-apes-pm-flow.pages.index`                   |
| WixAnywhereWebsiteWidgets                           | `wix-anywhere-bm.widgets-list`                               |
| WixAnywhereEditDesign                               | `wix-anywhere-bm.edit-design`                                |
