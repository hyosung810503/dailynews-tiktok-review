# Dailynews Social Publisher — App Review Resubmission Pack

Prepared: 2026-09-01

## Proposed production URLs

- Website: https://publisher.idailynews.co.kr/
- Terms of Service: https://publisher.idailynews.co.kr/terms.html
- Privacy Policy: https://publisher.idailynews.co.kr/privacy.html
- Official Dailynews website: https://www.idailynews.co.kr/

The production URLs intentionally do not contain social-platform brand names.

## DNS / GitHub Pages requirement before merge

Create the following DNS record for `idailynews.co.kr`:

- Type: CNAME
- Host/Name: publisher
- Target: hyosung810503.github.io

Then configure GitHub Pages for this repository and confirm HTTPS is active before submitting the URLs in the developer portal.

## Recommended app configuration

App name:

Dailynews Social Publisher

Description:

Dailynews Social Publisher helps authorized newsroom and publishing users prepare, review, and publish short-form video content from a controlled desktop workflow. Users connect an authorized account, review the target account and available publishing settings, and confirm the selected video before submission. Publication status is recorded to prevent duplicate submissions and support operational auditing.

Platform:

Desktop

Website URL:

https://publisher.idailynews.co.kr/

Terms URL:

https://publisher.idailynews.co.kr/terms.html

Privacy URL:

https://publisher.idailynews.co.kr/privacy.html

Products needed for Direct Post:

- Login Kit
- Content Posting API — Direct Post

Scopes needed for the intended Direct Post flow:

- user.info.basic
- video.publish

Remove `video.upload` unless the application actually demonstrates and uses the Upload-to-draft flow in the review video.

## App review explanation — English copy

Dailynews Social Publisher is a desktop-assisted short-form publishing service for authorized newsroom and publishing users. Login Kit is used to authorize a supported account and identify the connected account in the publishing interface. The `user.info.basic` scope is used only to retrieve basic information about the account that the user has authorized.

The Content Posting API Direct Post capability is used to submit a user-approved short-form news video to the authorized account. Before a publication request is submitted, the service queries creator information and available privacy options, displays the target account and publishing settings, and requires the user to confirm the selected video. The `video.publish` scope is used only for that authorized publication request.

The service records publication identifiers and status after submission to prevent duplicate publication and support operational auditing. It does not publish to an account that has not authorized the application.

## Revision explanation — English copy

This revision addresses the previous review feedback. We replaced the prior review-oriented URL with an official Dailynews-branded service URL, updated the public website so it presents the complete Dailynews Social Publisher service rather than a review landing page, and made the Terms of Service and Privacy Policy directly visible and accessible from the website header and footer. The service URL, Terms URL, and Privacy URL no longer contain a social-platform brand name. We also aligned the public website, requested products, scopes, and demo flow with the actual Direct Post integration.

## Demo video script

Record one continuous end-to-end video using the same domain submitted in the developer portal.

1. Open https://publisher.idailynews.co.kr/ and show the service home page.
2. Show the visible Terms of Service and Privacy Policy links in the header/footer and open each page briefly.
3. Open Dailynews Social Publisher desktop application.
4. Select the account connection / login function.
5. Complete the Login Kit authorization flow using the sandbox account required for first-time review.
6. Return to the publisher and show the connected account identity returned through `user.info.basic`.
7. Select one prepared vertical MP4 video.
8. Show caption/hashtags and the creator/privacy settings returned by the platform.
9. Show the target account and final publish confirmation control.
10. Confirm publication.
11. Show the successful API result / publication status in the application.
12. Show the resulting sandbox/private post as permitted by the test environment.

The video must visibly demonstrate every selected product and requested scope. If a product or scope is not demonstrated, remove it from the app configuration before submission.

## Final pre-submit checklist

- [ ] `publisher.idailynews.co.kr` resolves publicly over HTTPS.
- [ ] Website is not a login-only or review-only landing page.
- [ ] Terms link is visible without opening a menu.
- [ ] Privacy link is visible without opening a menu.
- [ ] Website, Terms, and Privacy URLs contain no social-platform brand name.
- [ ] App name matches the public service name: Dailynews Social Publisher.
- [ ] App icon is clear and matches Dailynews branding.
- [ ] Only required products are selected.
- [ ] Only required scopes are selected.
- [ ] Redirect URI is valid and uses the production domain where applicable.
- [ ] Required URL properties are verified in Production mode.
- [ ] First-time review demo uses Sandbox as required.
- [ ] Demo domain matches the submitted website domain.
- [ ] Demo shows Login Kit end to end.
- [ ] Demo shows `user.info.basic` use.
- [ ] Demo shows Direct Post / `video.publish` end to end.
- [ ] Demo file is within portal size requirements.
- [ ] Revision explanation explicitly addresses the previous rejection.
- [ ] All public links return HTTP 200 before submission.

## After app approval

App approval for `video.publish` is separate from the Content Posting API audit needed to remove unaudited-client visibility restrictions. Complete the Direct Post audit after the integration has been tested successfully if public-by-default posting is required.
