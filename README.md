This is an example HTML & CSS project with a contact form hosted on Netlify.
Use it as a guidance to host your own similar project.

# How to host your project on Netlify

## Prerequisites:
1. HTML and CSS project uploaded to your personal Github space.

## Deploy website to Netlify
1. Sign up for a Netlify account at https://app.netlify.com/signup

2. Click "New site from Git" on your Netlify dashboard

3. Choose your Git provider (e.g., GitHub)

4. Select your repository

5. Configure your build settings:
  - Build command: Leave blank (for static HTML/CSS)
  - Publish directory: Leave as is (usually /)
  - Leave other thigns as is / blank

6. Click "Deploy site". It will not take a couple of minutes for the site to be available.

## Configure Form Handling 
Netlify allows 100 free form submissions per months, see pricing info here: https://www.netlify.com/pricing/?_gl=1*7wdxxu*_gcl_au*MjAxNDk3Njg4Ny4xNzMzNzM4MzY1LjkwNzA1MjM5OS4xNzMzNzM5NDY2LjE3MzM3NDAxNzY.#pricing-table

1. Go to your site's dashboard on Netlify

2. Navigate to Forms > Active forms

3. You should see your form listed (e.g., "contact" which is a value of the name attribute of the form):
```
<form name="contact" method="POST" netlify netlify-honeypot="bot-field" action="./success.html">
     <div class="input-group">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required>
     </div>
     <input type="submit" value="Send message" class="btn-success">
  </form>
```

4. Click on the form name to view submissions and set up notifications

## Test Your Form
After the form was set up, make sure to wait a couple of minutes before testing, as you may run into unexpected errors / form data not being visible in the dashboard.

1. Visit your deployed Netlify site

2. Fill out and submit the contact form

3. Check the Forms section in your Netlify dashboard to see the submission

## Redirect messages from website directly to email
1. Go to your Netlify site dashboard and navigate to Forms > Form notifications

2. Scroll down to Form submit notifications section

3. Click on "Add notification" and select "Email notification" from the options

4. Enter the email address where you want to receive form submissions

5. Customize the email subject line (optional). You can use predefined variables like %{formName}, %{siteName}, or %{submissionId} to make it more informative

7. Save your settings

If your form has an <input> with name="email" to your form to set the Reply-to value, allowing direct replies to the submitter.

## Add a Custom Domain

1. Purchase a domain from a domain registrar (e.g., Namecheap)

2. In your Netlify site dashboard, go to Domain management > Add a domain

3. Enter your domain name and click "Verify"

4. Choose between Netlify DNS or your own DNS (Domain Name System) provider (place where you bought domain):
  
  #### For Netlify DNS:

  - Click "Add domain" to use Netlify DNS

  - Update your domain's nameservers to Netlify's (provided in the instructions)

  #### For your own DNS provider:

  - Add a CNAME record pointing to your Netlify site's default domain

  - Add TXT records for verification if prompted

5. Wait for DNS propagation (can take up to 24-48 hours)






