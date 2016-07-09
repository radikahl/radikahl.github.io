---
layout: post
title: Tools Roundup for Migrating to Google Apps mail
excerpt_separator: <!--more-->
---
After being unhappy with Gmail’s handling of my custom email address (email@mydomain.tld) for quite some time, I came across my colleague’s newly written blog article about [transitioning from a normal Google account (@gmail.com) to a Google Apps account (@mydomain.tld)](http://www.filiwiese.com/transitioning-to-a-google-apps-account/ "Transitioning to a Google Apps account"). A few conversations later I was confident and excited enough to migrate my mails from Gmail to Google Apps. However, it was unfortunately much more cumbersome than I expected. But I succeeded at the end.
<!--more-->

The main issue was to get all my emails into the new account. The loss of mails was unacceptable for me but all the most obvious methods lost some mails during the process or were otherwise unsuitable:

*   ☹ [Apple Mail](http://en.wikipedia.org/wiki/Mail_%28application%29 "Wikipedia about Apple Mail")
My original idea was to just copy folder by folder my mails to my new account. Unfortunately, it didn’t work well with nested folders. Some weren’t copied. Or even more annoying: only half copied. It just stopped with the message that it stopped but not displaying the reason. In other cases, the Mail app blow up some attachments that much that the server refused to take them (There is a 25MB limit per mail, if I am not mistaken). At the end, the two accounts had very different mail counts and size counts.
*   ☹ [Google Email Uploader](http://code.google.com/p/google-email-uploader-mac/ "Google Email Uploader for Mac")
The Google Apps migration guide offers this application to upload your mails from your hard-drive to your account. It seemed very promising in the beginning because it managed to upload folders (mailboxes) where Apple Mail failed. However, when performing a complete upload the Email Uploader started to skip hundreds of mails.
*   ☹ [Gmail’s Mail Fetcher](https://mail.google.com/support/bin/answer.py?answer=21288 "Get mail from other accounts")
This build-in Gmail function fetches mails from any other email account that supports POP access. As Gmail itself provides POP access, I tried to copy my emails with that to my new account. It stopped it almost immediately because the associated information about folders, or respectively labels, was lost during the process.
*   ☹ [Google Apps Migration for Microsoft Exchange](https://tools.google.com/dlpage/exchangemigration "Google Apps Migration for Microsoft Exchange")
This is only for business customers. Even though, I could opt for the 30 day trial and then get access to this feature, I didn’t use it because it wouldn’t be a long-term solution for the problem. Google could stop the promotion any time.
*   ☹ [Thunderbird](http://www.mozilla.org/thunderbird/ "Mozilla Thunderbird")
Basically, I tried the same as with Apple Mail. Even though, it seemed to have uploaded more mails some of mails were suddenly badly formatted. No mail application was able to display the text of the subject, the recipient and the sender of those mails. In conclusion, Thunderbird was also useless :(
*   ☺ [Mail Carbon](http://mailcarbon.calfater.com/ "Mail Carbon")
A first ray of hope. Unfortunately, not 100% perfect but almost. As it is much easier to use than IMAPSync I recommend to give Mail Carbon a try first. In case, it missed to copy some emails, IMAPSync can do the job.
*   ☺ [IMAPSync](http://ks.lamiral.info/imapsync/ "imapsync")
A command line tool that I hoped to have discovered much earlier. It copied the few mails Mail Carbon missed. The installation and use of the tool is not designed for the average computer user. However, there is a very [straightforward step-by-step guide](http://nimal.info/blog/2011/migrating-from-google-apps-mail-back-to-gmail/ "Back to Gmail: Migrating emails from Google Apps mail to Gmail") for Windows users. It is written for migrating from Google Apps mail back to Gmail. Hence, just exchange the login details in step 4. I’ll write an adoption for Mac OS X soon as the installation is quite different.

I hope this gives a good overview on the tools available to transition your emails from one IMAP account to another.

*Happy migrating!*