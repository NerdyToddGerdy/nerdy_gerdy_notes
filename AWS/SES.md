# Amazon Simple Email Service
AWS SES is a service that allows you to send emails to anybody you want from a pre-verified email address.

## How I have used it
 - I have created a AWS Lambda to alert me when a job has been completed.

## Security
 - TXT Files
## Best Practices
 ### Email Program Success Metrics
##### Bounces 
 - Occurs when an email cannot be delivered to the intended recipient
 - Should be monitored to try to keep hard bounce rate below 5%
 - hard bounces
   - Example: email address does not exist
 - soft bounces
   - Example: inbox is full
##### Complaints
 - Example: `Mark as Spam` button
 - Keep rate below 0.1%
##### Message Quality
 - Don't get Spammy
 - Make sure your links work
### Tips and Best Practices
##### General Recommendations
 - Would you want to receive this email?
 - Don't do what they do:
   - Home mortgage
   - Credit
   - Pharmaceuticals and supplements
   - Alcohol and tobacco
   - Casinos and gambling
   - Work-from-home programs
##### Domain and "From" Address Considerations
 - "From" Address is first thing they will see
 - think about subdomains for different types of emails (marketing, support, etc.)
 - "No-reply" emails send a message that you aren't interested in customer's feedback
 - Keep WHOIS info up to date
##### Authentication
 - SPF and SenderID
   - Prove you are actually from domain you are claiming to be
 - DKIM
   - Confirms that content has not changed in transit
 - Check these through ISP-based email addresses
##### Building and Maintaining Your Lists
 - Request confirmation prior to adding user to list
 - Make sure email is well-formed and has domain with valid MX Records
 - Use caution when allowing user-defined input to be passed to Amazon SES unchecked. Forums registrations and form submissions present unique risks because the content is completely user-generated, and spammers can fill out forms with their own content. It's your responsibility to ensure that you only send email with high-quality content.
 - Keep an eye on standard aliases (such as postmaster@, abuse@, or noc@) - potentially could be malicious.
##### Compliance
 - Be aware of anti-spamming and email marketing laws to regions you are emailing to.  [wiki link here](https://en.wikipedia.org/wiki/Email_spam_legislation_by_country)
 - Always consult an attorney to obtain legal advice.


## Catches
 - G-Suite's Quarentined emails (TXT file verification)
 - Starting in a `sandbox` environment