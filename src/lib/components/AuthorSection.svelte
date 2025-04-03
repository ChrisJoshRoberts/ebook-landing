<script>
  import authorImage from '$assets/profile_pic.jpg';
</script>
<section class="author-section">
  <h2>Author</h2> 
  <div class="author-container">
    <div class="author-detials">
      <h4 class="mb-m">Exploring Spain Through the Eyes of an Expert Author</h4>
      <p class="author-details">This author is a seasoned travel writer and cultural enthusiast with a deep, lifelong fascination for Spain. Having spent years immersing themselves in the country’s history, art, and traditions, the author brings a unique perspective to their work. Their keen understanding of Spanish culture is evident in every page, offering readers an authentic and insightful exploration of the country's rich heritage. Through engaging storytelling, they delve into Spain's diverse landscapes, its remarkable past, and its vibrant, ever-evolving culture. Whether it's unraveling the secrets of its culinary delights or tracing the steps of legendary artists, the author’s passion for Spain shines through, making their books a must-read for anyone eager to truly understand this captivating nation.</p>
    </div>
    <div class="img-container">
      <img src={authorImage} alt="">
    </div>
  </div>
</section>

<style>
  .author-section {
    padding: 80px 0;
    margin: 0 auto;
    max-width: 1200px;
  }
  
  .author-container {
    display: flex;
    justify-content: space-around;
  }
  .img-container {

    padding-right: 10%;
  }
  img {
    border: 4px solid #000;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .author-details {
    padding-right: 15%;
  }
</style>