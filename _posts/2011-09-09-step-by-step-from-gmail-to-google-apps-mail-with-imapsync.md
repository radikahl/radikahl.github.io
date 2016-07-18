---
layout: post
title: Step-by-Step from Gmail to Google Apps mail with IMAPSync
excerpt_separator: <!--more-->
permalink: 2011/09/09/step-by-step-from-gmail-to-google-apps-mail-with-imapsync.html
---
As mentioned in [my last post](http://kahl.in/2011/08/07/tools-roundup-for-migrating-google-apps-mail.html "Tools Roundup for Migrating To Google Apps Mail"), it is not too easy to migrate from a normal Gmail account to a Google Apps account. Lots of tools do not bring satisfying results. The only tool that brought the best results was imapsync. Being a command-line tool, it is not easy to use for most. Hence, I want to ease the usage by providing this step by step tutorial. It is tailored for Mac OS X users. However, there is a [very straightforward guide for Windows](http://nimal.info/blog/2011/migrating-from-google-apps-mail-back-to-gmail/ "Back to Gmail: Migrating emails from Google Apps mail to Gmail") as well. In fact, my short tutorial is based on that one :)
<!--more-->

## Step 1: Download & Installation
1.   Imapsync used to be for free. Unfortunately, the programmer recently decided to charge $45. A little heafty for a (hopefully) one time usage. Luckily, the older versions work just fine and can still be [downloaded without charge](https://s3.amazonaws.com/imapsync/imapsync-1.350.tar.gz "Free Download of Version 1.350").
2.   Download the following modules:
[Mail::IMAPClient](http://search.cpan.org/~plobbes/Mail-IMAPClient-3.29/lib/Mail/IMAPClient.pod)
[Digest::MD5](http://search.cpan.org/~gaas/Digest-MD5-2.51/MD5.pm)
[Term::ReadKey](http://search.cpan.org/dist/TermReadKey/ReadKey.pm)
[IO::Socket::SSL](http://search.cpan.org/~sullr/IO-Socket-SSL-1.44/SSL.pm)
[Date::Manip](http://search.cpan.org/~sbeck/Date-Manip-6.25/lib/Date/Manip.pod)
[File::Spec](http://search.cpan.org/~smueller/PathTools-3.33/lib/File/Spec.pm)
[Digest::HMAC_MD5](http://search.cpan.org/~gaas/Digest-HMAC-1.03/lib/Digest/HMAC_MD5.pm)
[PAR::Packer](http://search.cpan.org/~rschupp/PAR-Packer-1.010/lib/PAR/Packer.pm)
3.   Unpack the modules to */Library/Perl/Updates/5.10.0/*. If you don’t know how to get to that folder, press ⇧ + ⌘ + G while being in the Finder and paste the path in the box. Please note, that the packages Mail::IMAPClient and Date::Manip need some more love. You have to move the Mail folder from inside the *lib* folder of the unpacked package to */Library/Perl/Updates/5.10.0/*.
4.   Open Terminal. If the following statement does not produce an error message you have installed the modules successful:\r\n<pre>perl -mMail::IMAPClient -mDigest::MD5 -mTerm::ReadKey -mIO::Socket::SSL -mDate::Manip -mFile::Spec -mDigest::HMAC_MD5 -e ''<\/pre>
5.   Download Imapsync; the [old version for free](https://s3.amazonaws.com/imapsync/imapsync-1.350.tar.gz) or [buy the most recent version](http://ks.lamiral.info/imapsync/).
6.   Extract the tar.gz file. You might need to [install the Unarchiver](http://wakaba.c3.cx/s/apps/unarchiver.html) to be able to unpack the file.

## Step 2: Sync your Email
1.   Open Terminal.
2.   Change your directory to your imapsync folder. Probably you achieve it by typing *cd ~/Downloads/imapsync-1.350/* into the command line.
3.   Use the following command to sync (in our case rather, copy) the mail from your Gmail account to your new Google Apps mail account. Of course, adjust the account details to your accounts.
<pre>./imapsync ^
--host1 imap.gmail.com --port1 993 --ssl1 --authmech1 LOGIN ^
--user1 user&#64;gmail.com --password1 password4gmail ^
--host2 imap.gmail.com --port1 993 --ssl2 --authmech2 LOGIN ^
--user2 user&#64;yourdomain.com --password2 password4user2 ^
--split1 100 --split2 100 ^
--reconnectretry1 30 --reconnectretry2 30 ^
--noauthmd5 --noreleasecheck ^
--timeout 1200  --allowsizemismatch
</pre>
4.   The process will probably take quite a while now. Took hours for me.
5.   Set up a *forward rule* in your Gmail account to your new account. So that all mail gets automatically send to the right place :)

I hope this helps. And I hope that Google will provide a much easier and acceptable solution in the future.