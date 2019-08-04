<template>
  <div>
    <section class="section is-paddingless-x">
      <div class="container grid">
        <nav class="breadcrumb" aria-label="breadcrumbs">
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Blog</a></li>
            <li class="is-active" aria-current="page"><a href="#">How to use CSS grid?</a></li>
          </ul>
        </nav>
      </div>
    </section>

    <section class="section is-paddingless-x" style="padding-top: 0;">
      <div class="container grid">
        <article class="media center">
          <figure class="media-left">
            <p class="image is-64x64">
              <img class="is-rounded" src="https://bulma.io/images/placeholders/64x64.png">
            </p>
          </figure>
          <div class="media-content">
            <div class="content">
              <p>
                <strong>Samora </strong>
                <a href="#">@samoraa </a><br>
                <span class="has-text-grey">Self-taught, inspired to learn, code OCD patient</span><br>
                <span class="has-text-grey is-size-7"><time datetime="2019-05-10">20 May</time> &middot; 30 min ago</span>
              </p>
            </div>
          </div>
        </article>

        <div class="section is-paddingless-x">
          <h1 class="title">H ow to use CSS grid?</h1>
          <h1 class="subtitle">Lorem ipsum dolor sit amet, consectetur adipisicing.</h1>
        </div>

        <figure class="columns grid-xl is-mobile is-variable is-0 is-marginless">
          <div class="column">
            <div class="image card">
                <a href="#"><img src="./assets/images/dusk.png"></a>
            </div>
          </div>
          <div class="column">
            <div class="image card">
                <a href="#"><img src="./assets/images/desert.jpg"></a>
            </div>
          </div>
          <div class="column">
            <div class="image card">
                <a href="#"><img src="./assets/images/dusk.png"></a>
            </div>
          </div>
        </figure>

        <caption class="section is-paddingless-x" style="padding-top: 0;">
          <small class="has-text-grey">
            Nature is Allah SWT creation.
          </small>
        </caption>

        <div class="content is-medium">
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem dolores aliquam ex amet commodi! Reprehenderit voluptas dolores nesciunt soluta culpa!
					<ul>
						<li>In fermentum leo eu lectus mollis, quis dictum mi aliquet.</li>
						<li>Morbi eu nulla lobortis, lobortis est in, fringilla felis.</li>
						<li>Aliquam nec felis in sapien venenatis viverra fermentum nec lectus.</li>
						<li>Ut non enim metus.</li>
					</ul>
					<h3>The level</h3>
					<p>Quisque ante lacus, malesuada ac auctor vitae, congue <a href="#">non ante</a>. Phasellus lacus ex, semper ac tortor nec, fringilla condimentum orci. Fusce eu rutrum tellus.</p>
					<ol>
						<li>Donec blandit a lorem id convallis.</li>
						<li>Cras gravida arcu at diam gravida gravida.</li>
						<li>Integer in volutpat libero.</li>
						<li>Donec a diam tellus.</li>
						<li>Aenean nec tortor orci.</li>
						<li>Quisque aliquam cursus urna, non bibendum massa viverra eget.</li>
						<li>Vivamus maximus ultricies pulvinar.</li>
					</ol>
					<blockquote>Ut venenatis, nisl scelerisque sollicitudin fermentum, quam libero hendrerit ipsum, ut blandit est tellus sit amet turpis.</blockquote>
					<p>Quisque at semper enim, eu hendrerit odio. Etiam auctor nisl et <em>justo sodales</em> elementum. Maecenas ultrices lacus quis neque consectetur, et lobortis nisi molestie.</p>
					<p>Sed sagittis enim ac tortor maximus rutrum. Nulla facilisi. Donec mattis vulputate risus in luctus. Maecenas vestibulum interdum commodo.</p>
					<p>Suspendisse egestas sapien non felis placerat elementum. Morbi tortor nisl, suscipit sed mi sit amet, mollis malesuada nulla. Nulla facilisi. Nullam ac erat ante.</p>
        </div>
        
      </div>
    </section>

  </div>
</template>

<style>
/* 1fr is 1 fraction */
/* minmax() specify the min and max width of a column, making it responsive */
/* [md-start] and [xl-start] is an identifier */
.grid {
  display: grid;
  grid-template-columns: [xl-start] 1fr 1.5rem [md-start] minmax(0, 624px) [md-end] 1.5rem 1fr [xl-end];
}
/* The * is like a selector */
/* specify grid-column to the second '1fr' using 'grid-column: 2 / 3;', orrrrrr if 
we use an identifier like 'md-start', update it with just 'md' */
.grid * { grid-column: md; }
.grid-xl { grid-column: xl; }

.is-paddingless-x {
  padding-left: 0 !important;
  padding-right: 0 !important;
}

.center {
  display: flex !important;
  justify-content: center !important;
  align-items: center !important;
}

/* 624px + 1.5rem + 1.5rem = 672px */
@media (max-width: 672px) {
  :root {
    font-size: 90%;
  }
}

</style>
