# Dailynews Social Publisher — App Review Resubmission Pack

Prepared: 2026-09-01

## Public review URLs

- Website: https://publisher.denka-seiken.shop/
- Terms of Service: https://publisher.denka-seiken.shop/terms.html
- Privacy Policy: https://publisher.denka-seiken.shop/privacy.html

The review URLs intentionally use an owned neutral subdomain and do not contain a social-platform brand name.

## Domain and rights correction

Dailynews Social Publisher is a separate social-publishing workflow. Source content may be supplied under distribution authorization from publishing partners, including idailynews.co.kr.

The service does not claim ownership or administrative control of idailynews.co.kr or of a source publisher's domain, website, editorial system, or infrastructure. The source publisher retains control of those systems.

The review site is hosted at `publisher.denka-seiken.shop`, which is separate from the source-content domain.

## DNS / GitHub Pages configuration

The review domain uses the following DNS record:

- Type: CNAME
- Host/Name: publisher
- Target: hyosung810503.github.io
- Proxy: DNS only

GitHub Pages must use `publisher.denka-seiken.shop` as the repository custom domain and HTTPS must be active before app resubmission.

## Recommended app configuration

App name:

Dailynews Social Publisher

Description:

Dailynews Social Publisher helps authorized publishing users prepare, review, and publish approved short-form video content from a controlled desktop workflow. Users connect an authorized account, review the target account and available publishing settings, and confirm the selected video before submission. Source material may be supplied under distribution authorization from publishing partners. Publication status is recorded to prevent duplicate submissions and support operational auditing.

Platform:

Desktop

Website URL:

https://publisher.denka-seiken.shop/

Terms URL:

https://publisher.denka-seiken.shop/terms.html

Privacy URL:

https://publisher.denka-seiken.shop/privacy.html

Products needed for Direct Post:

- Login Kit
- Content Posting API — Direct Post

Scopes needed for the intended Direct Post flow:

- user.info.basic
- video.publish

Remove `video.upload` unless the application actually demonstrates and uses the Upload-to-draft flow in the review video.

## App review explanation — English copy

Dailynews Social Publisher is a desktop-assisted short-form publishing service for authorized publishing users. Login Kit is used to authorize a supported account and identify the connected account in the publishing interface. The `user.info.basic` scope is used only to retrieve basic information about the account that the user has authorized.

The Content Posting API Direct Post capability is used to submit a user-approved short-form video to the authorized account. Before a publication request is submitted, the service queries creator information and available privacy options, displays the target account and publishing settings, and requires the user to confirm the selected video. The `video.publish` scope is used only for that authorized publication request.

Source content may be supplied under distribution authorization from publishing partners, including idailynews.co.kr. Dailynews Social Publisher does not claim administrative ownership or control of the source publisher's website, domain, editorial system, or infrastructure.

The service records publication identifiers and status after submission to prevent duplicate publication and support operational auditing. It does not publish to an account that has not authorized the application.

## Revision explanation — English copy

This revision addresses the previous review feedback. We replaced the prior review-oriented URL with the neutral owned service URL `publisher.denka-seiken.shop`, made the Terms of Service and Privacy Policy directly visible from the public website, and aligned the public pages with the actual content-rights model. The service may distribute source material under authorization from publishing partners, but it does not claim ownership or administrative control of a source publisher's domain or website. The website, Terms, and Privacy URLs do not contain a social-platform brand name. We also aligned the requested products, scopes, and demo flow with the intended Direct Post integration.

## Demo video script

Record one continuous end-to-end video using the same domain submitted in the developer portal.

1. Open https://publisher.denka-seiken.shop/ and show the service home page.
2. Show the visible Terms of Service and Privacy Policy links and open each page briefly.
3. Open Dailynews Social Publisher desktop application.
4. Select the account connection / login function.
5. Complete the Login Kit authorization flow using the review or sandbox account required for the current review mode.
6. Return to the publisher and show the connected account identity returned through `user.info.basic`.
7. Select one approved vertical MP4 video covered by the applicable publishing or distribution authorization.
8. Show caption/hashtags and the creator/privacy settings returned by the platform.
9. Show the target account and final publish confirmation control.
10. Confirm publication.
11. Show the successful API result / publication status in the application.
12. Show the resulting post as permitted by the review environment.

The video must visibly demonstrate every selected product and requested scope. If a product or scope is not demonstrated, remove it from the app configuration before submission.

## Final pre-submit checklist

- [ ] `publisher.denka-seiken.shop` resolves publicly.
- [ ] GitHub Pages serves the domain over valid HTTPS.
- [ ] Home page returns HTTP 200.
- [ ] Terms page returns HTTP 200.
- [ ] Privacy page returns HTTP 200.
- [ ] Website is not a login-only or review-only landing page.
- [ ] Terms link is directly visible.
- [ ] Privacy link is directly visible.
- [ ] Website, Terms, and Privacy URLs contain no social-platform brand name.
- [ ] Public pages do not claim ownership or administration of idailynews.co.kr.
- [ ] App name matches the public service name: Dailynews Social Publisher.
- [ ] Only required products are selected.
- [ ] Only required scopes are selected.
- [ ] Redirect URI is valid and matches the demonstrated integration.
- [ ] Demo domain matches the submitted website domain.
- [ ] Demo shows Login Kit end to end.
- [ ] Demo shows `user.info.basic` use.
- [ ] Demo shows Direct Post / `video.publish` end to end.
- [ ] Revision explanation explicitly addresses the previous rejection.

## After app approval

Approval for `video.publish` and any separate Content Posting API audit requirements should be handled according to the platform's current review requirements. The submitted public pages, requested scopes, and demonstrated product behavior must remain consistent with the actual integration.
