<script>
  export let title;
  export let date;
  export let image;
</script>

  <div class="post-title-date">
    <p class="post-title">
        {title}
    </p>
    <p class="date">
      {date}
    </p>
  </div>
  <div class="img-container">
    <img class="img" src={image} alt="">
  </div>

<style>
.post-title-date {
  color: white;
  display: grid;
  grid-template-columns: 1fr 1fr;
  font-size: 1.5em;
  font-family:system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.post-title {
  flex: 1;
  text-align: right;
  padding-right: 50px;
  font-weight: bold;
}
.date {
  flex: 1;
  text-align: left;
  padding-left: 50px;
}
.img-container {
  display: flex;
  justify-content: center;
  align-items: center;
}
.img {
  object-fit: scale-down;
  border-radius: 10px;
  padding-bottom: 50px;
}
</style>