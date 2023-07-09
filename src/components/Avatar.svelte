<script>
  import AvatarImage from "./AvatarImage.svelte";
  import InlineLink from "./InlineLink.svelte";
  import imgUrl from "../assets/me.png";

  const today = document.lastModified.split(" ")[0];
</script>

<section class="flex flex-col mb-6">
  <div class="w-full bg-slate-200 dark:bg-slate-700 shadow-lg rounded-lg">
    <div class="w-full flex items-center justify-between p-3 space-x-6">
      <div class="flex items-center">
        <AvatarImage src={imgUrl} alt="Joshua Pearson" />
        <div class="flex flex-col">
          <span class="font-bold ml-2 border-b-2 border-slate-400 mb-1">
            Joshua Keith Pearson
          </span>
          <span class="text-xs ml-2">Full Stack Developer</span>
        </div>
      </div>
    </div>
    <div
      class="flex items-center justify-between px-3 py-2 dark:bg-slate-600 bg-slate-300"
    >
      <span class="text-sm font-bold">Last Updated</span>
      <span class="text-sm font-bold">{today}</span>
    </div>
    <div class="p-3">
      <p class="text-sm">
        Nice to meet you. I am a self-taught professionally experienced full
        stack engineer. I have a passion for learning and building. I am
        currently working on a few personal projects, I am a quick learner and
        can adapt to any environment. I appreciate a team that is passionate
        about their work and encourages growth. I enjoy collaborating on
        important projects and enjoy working with others. I am a problem solver
        and enjoy the challenge of finding solutions. I enjoy keeping up to date
        on new technologies and am always looking for ways to improve my skills.
      </p>
      <p class="text-sm pt-2">
        Welcome to my webpage resume. You'll find all my skills on this page.
        <InlineLink href="/portfolio">Portfolio</InlineLink> will show my highlighted
        personal projects and descriptions of work experiences. You'll be able to
        send me an email from the <InlineLink href="/contact"
          >contact</InlineLink
        > page, alongside links to professional pages such as github and linkedin
        and more information about myself as well. If you have opportunities for
        me to review, contact me via Linkedin. Thank you. This site is built with
        Svelte and TailwindCSS.
      </p>
    </div>
  </div>
</section>
