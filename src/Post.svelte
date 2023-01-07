<script>
  export let title;
  export let date;
  export let src;
</script>

<article class="post">
  <div class="post-title-date">
    <h1 class="post-title">
        {title}
    </h1>
    <p class="date">
      {date}
    </p>
  </div>
  <img class="img" {src} alt="">
</article>

<style>
.post {
  display: flex;
  border: 1px solid black;
  background-color: rgb(196, 173, 142);
  border-radius: 10px;
  margin: 15px;
  padding: 15px;
  width: fit-content;
}
.post-title-date {
  display: grid;
  grid-template-columns: auto;
}
.post-title {
  flex: 1;
}
.date {
  flex: 1;
  text-align: right;
}
.img {
    display: flex;
    align-content: center;
    margin-left: auto;
    margin-right: auto;
    object-fit: fill;
    border-radius: 10px;
}
</style>