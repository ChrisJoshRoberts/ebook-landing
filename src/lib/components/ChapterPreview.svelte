<script>
  const chapters = [
  {
    number: 1, 
    title: 'Introduction',
    strapline: 'Understanding the Spanish system',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi dignissimos consectetur, et minus, optio commodi ullam earum incidunt quod vitae voluptates, quidem nobis sapiente deserunt nam molestiae exercitationem nostrum eveniet.',
  },
  {
    number: 2,
    title: 'History of Spain',
    strapline: 'A journey through time',
    description: 'Explore the rich and diverse history of Spain, from its ancient roots to its modern-day significance. This chapter covers key historical events, figures, and the cultural evolution of the nation.',
  },
  {
    number: 3,
    title: 'Geography and Climate',
    strapline: 'Land of contrast',
    description: 'Spain boasts a varied landscape, from the snowy peaks of the Pyrenees to the sunny beaches of the Mediterranean. Learn about the regions and climate that shape the country’s way of life.',
  },
  {
    number: 4,
    title: 'Spanish Culture',
    strapline: 'Celebrating the heritage',
    description: 'Dive into the unique cultural practices of Spain. From flamenco dancing to world-renowned festivals like La Tomatina and Running of the Bulls, discover the traditions that define Spanish identity.',
  },
  {
    number: 5,
    title: 'Cuisine and Dining',
    strapline: 'A taste of Spain',
    description: 'Spain is known for its rich culinary heritage. Explore the flavors of Spanish cuisine, from tapas and paella to churros and sangria, and the cultural significance behind each dish.',
  },
  {
    number: 6,
    title: 'Spanish Art and Architecture',
    strapline: 'Masterpieces of Spain',
    description: 'Spain is home to some of the most celebrated artists in history. This chapter delves into the works of painters like Picasso, Dalí, and Velázquez, and the architectural wonders of Gaudí and other renowned architects.',
  }
];

  let selectedChapter = $state(1);

  /**
   * @param {{ number: number; title: string; strapline: string; description: string; }} chapter
   */
  const selectChapter = (chapter) => {
    selectedChapter = chapter.number;
  }
</script>

<section class="chapter-preview default-margin">
  <h2 class="mb-l">What you are getting</h2>
  <div class="chapter-container">
    <ul>
      {#each chapters as chapter}
      <li>
        <button class="chapter-title"
          aria-controls={`chapter-info-${chapter.number}`}
          class:selected-chapter-title={selectedChapter === chapter.number}
          aria-expanded={selectedChapter === chapter.number}
          onclick={() => selectChapter(chapter)}
        >
        <h3>
          Chapter {chapter.number} : {chapter.title}
        </h3>
        </button>
      </li>
      {/each}
    </ul>
    <div class="chapter-info">
      <h3 class="chapter-strapline italic mb-s">
        Understanding the Spanish system
      </h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi dignissimos consectetur, et minus, optio commodi ullam earum incidunt quod vitae voluptates, quidem nobis sapiente deserunt nam molestiae exercitationem nostrum eveniet.</p>
    </div>
  </div>
</section>

<style>
  .chapter-preview {
    padding: 80px 0;
    margin-left: 12vw;
    margin-right: 20vw;
    max-width: 1150px;
  }
  .chapter-container {
    display: flex;
    justify-content: space-between;
  }
  .chapter-container ul {
    width: 40%;
  }
  .chapter-info {
    width: 55%;
  }
  .chapter-title {
    border-bottom: 1px solid #535353;
    width: 100%;
    display: block;
    padding: 20px 0;
    text-align: left;

  }
  .selected-chapter-title {
    background-color: black;
 
    width: 100%;
    display: block;
    padding: 20px 16px;
    text-align: left;
    border: none;
    color: white;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
  }
  
</style>