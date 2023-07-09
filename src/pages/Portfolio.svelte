<script>
  import Card from "../components/Card.svelte";
  import workExperiences from "../assets/data/WorkExperiences";
  import InlineLink from "../components/InlineLink.svelte";
</script>

<div class="mb-1">
  <section class="md:flex md:flex-wrap justify-center mx-auto">
    <Card className="max-w-xl md:w-4xl  h-64" arrow>
      <p slot="subtitle">Work Experience</p>
      <p slot="title">Portfolio</p>
      <div slot="accent1">2017</div>
      <div slot="accent2">Current</div>
      <p slot="content">
        You'll find links to github, codepen, and my passion project here. I've
        also included a description for each of my work experiences. Thank you
        for taking the time to look at my portfolio.
      </p>
    </Card>
    <Card className="max-w-xl md:w-4xl  h-64">
      <p slot="title">Links</p>
      <div slot="accent1">Check these out to see my work</div>
      <div slot="content" class="flex-col">
        <p class="pt-2">
          <InlineLink href="https://www.github.com/wurby" external
            >Github</InlineLink
          >
        </p>
        <p class="pt-2">
          <InlineLink href="https://www.codepen.io/wurby" external
            >Codepen</InlineLink
          >
        </p>
        <p class="pt-2">
          <InlineLink
            href="https://www.linkedin.com/in/joshuakeithpearson"
            external>LinkedIn</InlineLink
          >
        </p>
        <p class="pt-2">
          <InlineLink href="https://www.savemypast.com" external
            >SaveMyPast.com</InlineLink
          >
        </p>
      </div>
    </Card>
  </section>

  <div class="md:flex md:flex-wrap justify-center">
    {#each workExperiences as workExperience}
      <Card className="max-w-xl  h-64" arrow>
        <p slot="subtitle">{workExperience.title}</p>
        <p slot="title">{workExperience.subtitle}</p>
        <p slot="accent1">{workExperience.accent1}</p>
        <p slot="accent2">{workExperience.accent2}</p>
        <p slot="content">{workExperience.content}</p>
      </Card>
    {/each}
  </div>
</div>
