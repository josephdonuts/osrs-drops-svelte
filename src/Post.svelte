<script>
  export let title;
  export let date;
  export let src;
</script>

<article class="post">
  <h1 class="post-title">
      <span class="title">{title}</span>
  </h1>
  <p class="date">
      <span class="date">{date}</span>
  </p>
  <img class="img" {src} alt="">
</article>