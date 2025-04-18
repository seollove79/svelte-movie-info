<script>

  let textRed = "color: red";

  const data = [
    {
      title: "고질라 X 콩: 뉴 엠파이어",
      year: 2024,
      category: "어드벤처, 액션, SF",
      likeCount: 0,
    },
    {
      title: "듄: 파트2",
      year: 2024,
      category: "액션",
      likeCount: 0,
    }
  ];

  const handleLike = (index) => {
    data[index].likeCount++;
  };
</script>

<main>
  {#each data as item, index}
  <div>
    <h3 class="bg-yellow" style={textRed}>{item.title}</h3>
    <p>개봉: {item.year}</p>
    <p>장르: {item.category}</p>
    <button on:click={() => handleLike(index)}>좋아요 {item.likeCount}</button>
  </div>
  {/each}
</main>

<style>
  .bg-yellow {
    background-color: gold;
  }
</style>
