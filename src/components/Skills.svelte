<script>
  const skills = [
    { skill: "Cypress", level: "9" },
    { skill: "Javascript", level: "8" },
    { skill: "Agile", level: "8" },
    { skill: "Typescript", level: "7" },
    { skill: "Git", level: "7" },
    { skill: "HTML/CSS", level: "7" },
    { skill: "Ci/Cd", level: "7" },
    { skill: "StateAdapt", level: "6" },
    { skill: "Jest", level: "6" },
    { skill: "React", level: "6" },
    { skill: "Material UI", level: "6" },
    { skill: "Firebase", level: "6" },
    { skill: "Rest Api", level: "6" },
    { skill: "Svelte", level: "5" },
    { skill: "RxJS", level: "5" },
    { skill: "Docker", level: "5" },
    { skill: "Python", level: "5" },
    { skill: "Postman", level: "5" },
    { skill: "Github Actions", level: "5" },
    { skill: "Node.js", level: "4" },
    { skill: "TailwindCSS", level: "4" },
    { skill: "AWS", level: "4" },
    { skill: "OpenAi", level: "4" },
    { skill: "Angular", level: "4" },
    { skill: "SvelteKit", level: "4" },
    { skill: "MSW", level: "4" },
    { skill: "SQL", level: "4" },
    { skill: "GraphQL", level: "4" },
    { skill: "Express", level: "3" },
    { skill: "Bootstrap", level: "3" },
    { skill: "MongoDB", level: "3" },
    { skill: "Redux", level: "3" },
    { skill: "Next.js", level: "3" },
    { skill: "Scikit-learn", level: "2" },
  ];
</script>

<!-- Skills table -->
<section class="flex-col m-auto mb-6">
  <div
    class="flex-col w-full bg-slate-200 dark:bg-slate-700 shadow-lg rounded-lg"
  >
    <div
      class="flex space-x-1 p-2 dark:bg-slate-600 bg-slate-300 mb-1 rounded-lg"
    >
      <span class="w-full font-bold text-sm text-center"
        >Skill - Experience Level</span
      >
    </div>
    <div id="skillsTable" class="flex flex-wrap justify-baseline p-1">
      {#each skills as skill}
        <div
          on:keydown={(e) => {
            if (e.key === "Enter") {
              window.open(
                `https://www.google.com/search?q=${skill.skill}`,
                "_blank"
              );
            }
          }}
          on:click={() => {
            window.open(
              `https://www.google.com/search?q=${skill.skill}`,
              "_blank"
            );
          }}
          class="flex border rounded-full ring-1 ring-slate-400 dark:ring-slate-500 border-slate-400 dark:text-slate-800 bg-slate-100 mx-1 my-1 px-2 shadow-sm shadow-slate-400 hover:bg-slate-300 cursor-pointer"
        >
          <span class="text-sm m-auto">{skill.skill}</span>
          <span class="m-auto px-1">-</span>
          <span class="text-sm m-auto">{skill.level}/10</span>
        </div>
      {/each}
    </div>
  </div>
</section>
