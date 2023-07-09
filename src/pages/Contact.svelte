<script>
  import Card from "../components/Card.svelte";
  import InlineLink from "../components/InlineLink.svelte";
</script>

<section class="flex-col h-screen w-full">
  <Card className="md:max-w-2xl m-auto">
    <div slot="title">Contact</div>
    <div slot="subtitle">Get in touch</div>

    <div slot="content">
      <p>
        Please contact me through <InlineLink
          external
          href="https://linkedin.com/in/joshuakeithpearson"
        >
          LinkedIn</InlineLink
        > if you have any opportunities. Otherwise, submit your email below and I
        will reach out to you. Using the contact form below will result in a delay
        of up to one month or more.
      </p>
    </div>
  </Card>

  <Card className="md:max-w-2xl m-auto">
    <p slot="title">Be Contacted</p>
    <p slot="subtitle">I'll be in touch</p>
    <p slot="accent1">Name</p>
    <p slot="accent2">Email</p>
    <div slot="content">
      <form
        action="https://gmail.us9.list-manage.com/subscribe/post?u=6ce8c5ac52f282324a340d632&amp;id=b60c6e9954&amp;f_id=00bd27e1f0"
        method="post"
        id="mc-embedded-subscribe-form"
        name="mc-embedded-subscribe-form"
        class="validate"
        target="_blank"
      >
        <div class="flex flex-wrap pt-1">
          <div class="relative my-4">
            <label for="mce-FNAME" class="absolute -top-5 left-4"
              >Name <span class="text-red-500">*</span></label
            ><input
              type="text"
              name="FNAME"
              class="bg-slate-300 dark:bg-slate-700 rounded-full p-2 ml-2 placeholder:text-slate-700 placeholder:dark:text-slate-400"
              id="mce-FNAME"
              required
              placeholder="John Doe"
              value=""
            />
          </div>
          <div class="relative my-4">
            <label for="mce-EMAIL" class="absolute -top-5 left-4"
              >Email Address <span class="text-red-500">*</span></label
            ><input
              type="email"
              name="EMAIL"
              class="bg-slate-300 dark:bg-slate-700 rounded-full p-2 ml-2 placeholder:text-slate-700 placeholder:dark:text-slate-400"
              id="mce-EMAIL"
              placeholder="email@domain.com"
              required
              value=""
            />
          </div>
          <div id="mce-responses" class="">
            <div
              class="text-red-500"
              id="mce-error-response"
              style="display: none;"
            />
            <div
              class="text-green-500"
              id="mce-success-response"
              style="display: none;"
            />
          </div>
          <div aria-hidden="true" style="position: absolute; left: -5000px;">
            /* real people should not fill this in and expect good things - do
            not remove this or risk form bot signups */
            <input
              type="text"
              name="b_6ce8c5ac52f282324a340d632_b60c6e9954"
              tabindex="-1"
              value=""
            />
          </div>
          <div class="my-auto m-2">
            <input
              type="submit"
              name="subscribe"
              id="mc-embedded-subscribe"
              class="p-2 bg-slate-300 dark:bg-slate-700 rounded-full m-2 hover:bg-slate-400 dark:hover:bg-slate-600 cursor-pointer"
              value="Get in Touch"
            />
          </div>
        </div>
      </form>
      <script
        type="text/javascript"
        src="//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js"
      ></script><script type="text/javascript">
(function($) {window.fnames = new Array(); window.ftypes = new Array();fnames[1]=FNAME;ftypes[1]=merge;,fnames[0]=EMAIL;ftypes[0]=merge;,fnames[2]=LNAME;ftypes[2]=merge;,fnames[3]=ADDRESS;ftypes[3]=merge;,fnames[4]=PHONE;ftypes[4]=merge;,fnames[5]=BIRTHDAY;ftypes[5]=merge;false}(jQuery));var $mcj = jQuery.noConflict(true);
      </script>
    </div>
  </Card>
</section>
