<script>
  import bookCover from '$assets/book_cover.png'
  import phoneCover from '$assets/phone_cover.png'
  import Button from '$components/Button.svelte'
</script>

<section class="hero">
  <div class="hero-showcase text-center bold">
    <h1 class="purple">MOVE TO</h1>
    <h1 class="purple mb-xs">SPAIN</h1>
    <h4 class="italic semi-bold">There is no need to make the same mistakes I did.</h4>
    <img class="book-cover" src={bookCover} alt="">
    <img class="phone-cover" src={phoneCover} alt="">
  </div>
  <div class="hero-text white text-center">
    <h1>THIS EBOOK WILL</h1>
    <h1>SAVE YOU MONEY</h1>
    <h1 class="mb-m">TIME AND NERVES</h1>
    <p class="light-grey">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quae dolorum qui id, 
      repellendus vitae consequatur minus saepe animi voluptatibus voluptatum officia est, 
      eos molestiae, debitis quibusdam aliquid reiciendis sed recusandae!
    </p>
    <Button mode='light'>Purchase E-Book</Button>
  </div>
</section>

<style>
  .hero {
    display: flex;
    height: 100vh;
    overflow-y: hidden;
  }
  .hero-showcase {
    position: relative;
    width: 50%;
    padding: 100px 16px 0 16px;
    background: linear-gradient(
      135deg,
      #e2cbff,
      #e2cbff 25%,
      #deeaff 50%,
      #ece5ff 75%,
      #927bce

    );
  }
  .hero-text {
    padding: 100px 5%;
    width: 50%;
    background-color: black;
  }
  .book-cover {
    position: absolute;
    right: 2%;
    bottom: 0;
    width: 65%;
    transform: translateY(30%);
  }
  .phone-cover {
    position: absolute;
    right: 52%;
    bottom: 0;
    width: 35%;
    transform: translateY(25%);
  }
</style>