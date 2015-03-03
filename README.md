#company e-mail aliases / forwarding

This method was chosen as it proved to be the cheapest way to create own domain
email addresses for the company without creating extra Google user accounts

##Disclaimer and next steps

This does not provide a way for tracking what emails employees send out on behalf
of the company, and e-mails do not originate from the company’s SMTP servers.

Next steps would be to add real Google accounts and potentially use Google
Vault to keep track of prevent tampering of sent and received e-mail.

##FOR DOMAIN ADMINS: Creating Alias for private e-mail addresses

- Access the Google Apps administrator account.
- Access the Groups page
- Add a new Group
  - Call it `$username private-alias` where $username is something like `jerzy`
  - Give it the same $username group email address @example.com
  - Select `Team` Access Level
  - Be sure to tick the `Also allow anyone on the internet` box
  - Do NOT add all users to the group.
  - Hit create
- Manage the group and add the person’s private e-mail as a member.

##FOR EMAIL USERS: Configuring Inbox for sending email as @example.com on G-Mail!

We will now trick gmail to send email smtp.gmail.com server.

- Go to your personal gmail account
- Access the Settings page (top-right gear on page)
- Access the *Accounts and Import* tab, note the **Send mail as** section.
- Be sure to select the “Reply from the same address” radio button for “When replying
  to a message”.
- Click the link *Add another email address you own*
  - Fill in the identify
    - Your name
    - Email alias
    - Leave “treat as alias” checked
    - Click next
  - Fill in gmail.com’s own smtp details
    - SMTP server: smtp.gmail.com
    - Username shoud be $username@gmail.com where $username is your own login, or your own GApps e-mail
    - Fill in your gmail password or app-specific password
    - Click *Add Account*
  - Confirmation email to arrive in your inbox, fill it in and hit *Verify*

If you have two step verification you will need to generate an app-specific password,
in this case you probably know how to do this... :)
