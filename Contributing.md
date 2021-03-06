# Contributing and Forking This Tool

We have designed not just for oursleves but for other groups to use as well. To adapt this tool to your use, edit the file `./src/bg/background.js` for your use. Here's what you need to do:

1. Create your own Google Form.  You can copy [ours](https://docs.google.com/forms/d/1kuwxu2lXYSRpkwBj4o9kwjURZL3hgk-mSFoK4qkC4ZI/edit), or create your own from scratch
    * Once you've created a form, Google will automagically create a spreadsheet in which to store the responses. You can also use the fancy response visualizations tool to get some basic information about submissions.
  * Make note of the form URL. In `src/background.js`, update the `GOOGLE_FORMS_URL` variable with the new URL, taking care to **replace the final `edit` with `/formResponse?ifq`**. 

2. For each field name, you will have to identify the corresponding field entry id and update the various field-relate variables. In your browser's developer tools pane, inspect element on the input field. There will be `entry.[integer]` in the highlighted code. That is the value for the entry field ID. 

3. We have added the **event name** and **government agencies** to the form submission as constants, but the code to allow them to be entered (in the case of the event name) or selected (in the case of the agency) is simply commented out in the code.  We suggest filtering the long agency list to a subset appropriate for your event.  See the HTML source of [the official nomination form](http://digital2.library.unt.edu/nomination/eth2016/url/https%3A//www3.epa.gov/) for the full list, and just make the appropriate substition in the `#agency` form field in `popup.html`. 

Small events can uncomment the "notificationToolUrl"-related lines -- this will permit users to add seeds directly to the nomination tool database. However, there is some worry that large numbers of users could crash the nomination tool server; so for large events, we've ocmmented this out.  

Contact us for further information!

