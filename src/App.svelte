<script>
  import Card from "./card.svelte";
  import Widget from "./widget.svelte";
</script>

<Widget>
  <h1 slot="header">Hello</h1>
  <svelte:fragment slot="footer">
    <p>All rights reserved.</p>
    <p>Copyright (c) 2019 Svelte Industries</p>
  </svelte:fragment>
</Widget>

<br />

<Card>
  <span slot="name">
    한교동
  </span>

  <span slot="address">
    산리오시티<br>
    헬로키티네 집
  </span>

  <span slot="email">
    mymelody@gmail.com
  </span>
</Card>