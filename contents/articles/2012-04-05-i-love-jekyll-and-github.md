---
title: "I Love Jekyll and Github"
tags: development, introductions, writing
date: 2012-04-05 20:37
---

I love <a href='http://jekyllbootstrap.com'>Jekyll Bootstrap</a> and
<a href='http://pages.github.com'>GitHub</a> as a blog platform &mdash; so much so
that I&rsquo;m sure I&rsquo;ll write posts more often than once a year. Really.
As a frontend developer and pixel-pusher, it might be the most pleasurable way to
blog that I&rsquo;ve tried yet. Not that I&rsquo;ve tried much, but hear me out.

<h2>The Tools</h2>

<p>
  A month after my last blog post in late 2010, I got a new job with a dating
  startup named <a href="http://www.howaboutwe.com">HowAboutWe</a>. It&rsquo;s
  been an incredible and intense experience so far that &mdash; in addition to partly
  yanking me away from paying any attention to this blog &mdash; has introduced
  me to many things. Chief among those with regards to this post are
  <a href="http://github.com">Github</a> for source control, <a href="http://vim.org">
  Vim</a> for code editing (and writing text in general), and <a href="http://compass-style.org">
  Compass</a> and <a href="http://sass-lang.com">Sass</a> for writing CSS.
</p>

<figure class="right">
  <div class="curledShadow">
    <a href="https://plus.google.com/photos/101625155591132408533/albums/5728262585017161025/5728262600833254258">
      <img src="https://lh4.googleusercontent.com/-goxxb-nwgBM/T37gfF7SQ3I/AAAAAAAAGRE/lMUqVoHdLN8/s757/P1163394.JPG"
        alt="Photo of auto parts from Bangkok's Chinatown" />
    </a>
  </div>
  <figcaption>Wordpress theme components. Or&hellip;auto parts from Bangkok's Chinatown.</figcaption>
</figure>

<p>
  I now have a flow at work that is a cinch to me. When the scales finally tipped,
  oh, maybe a year ago, and I set out to redesign this blog, it made sense to
  incorporate as much of this new beloved workflow as I could. It started with a new
  theme for my original <a href="http://www.wordpress.org">Wordpress</a> install.
  I worked on converting the stylesheets into <a href="http://sass-lang.com/docs/yardoc/file.SASS_CHANGELOG.html#3-0-0">
  *.scss</a> partials for use with <a href="http://compass-style.org">Compass</a>.
  Vim was the editor, and I kept all my changes on Github. But it still didn&rsquo;t
  sit completely right with me. Free time was short, and the once humble task of
  Wordpress theming and uploading via ftp to my web host felt intimidating.
</p>

<h2>Blogs are static beasts.</h2>

<p>
  HowAboutWe used to have ad modules for third-party sites that would make
  complex queries to conjure seemingly timely and location-relevant content.
  In retrospect, this was silly for a couple of reasons &mdash; not the least of
  which being that trusting user-generated content for the purpose of
  advertising is extremely risky. (One that always brought smiles
  involved a user suggesting that he and his date join OkCupid rather
  than pay for our site.)
</p>

<p>
  Instead, it made complete sense to curate the content, and just serve up quick
  and fast static HTML that would be browser cached practically to infinity. A day later,
  we replaced nearly all of these ads with the static content, and the elegance of the
  solution had big payoffs in both performance, and code maintenance. It was silly
  we didn&rsquo;t do it that way from the start.
</p>

<figure class="midParagraph">
  <div class="curledShadow">
    <a href="https://plus.google.com/photos/101625155591132408533/albums/5728262585017161025/5728269955431190658">
      <img src="https://lh3.googleusercontent.com/-NOW4NhzORck/T37nLL8E0II/AAAAAAAAGRU/W48f9ivEqVs/s727/truck-in-chiang-mai.jpg"
        alt="Photo of a truck at a highway stop in Chiang Mai Province" />
    </a>
  </div>
  <figcaption>Keep it simple!</figcaption>
</figure>

<p>
  It wasn&rsquo;t much of a leap to reach the same conclusions about blogs.
  I&rsquo;d heard of static site generators like
  <a href="https://github.com/mojombo/jekyll">Jekyll</a> before &mdash; years ago,
  in fact &mdash; but I never considered them useful for a blog. The thought of
  static HTML that I&rsquo;d have to compile and upload after every post&hellip;
  It just sounded cumbersome. And then I realized that I wasn&rsquo;t exactly
  producing a daily newspaper&rsquo;s worth of content. Also, there are times when
  I&rsquo;d want to do a good bit of custom layout for a given post. So, my post
  content would be peppered with HTML.
</p>

<p>
  Writing HTML into Wordpress <code>textarea</code>s always felt awkward to me.
  I would tend to hash out the layout in a text editor and separate HTML file
  before pasting it in to Wordpress.
</p>

<p>
  <a href="https://github.com/mojombo/jekyll">Jekyll</a>, and more specifically
  <a href="http://jekyllbootstrap.com/"> Jekyll Bootstrap</a>, solve this problem.
  Jekyll works by pointing it to some template HTML, writing your content as either
  <a href="http://daringfireball.net/projects/markdown/">Markdown</a> (*.md files)
  or HTML, and then running it. It mashes the content to the template and spits out
  a fully rendered website that you can then upload. And
  <a href="http://jekyllbootstrap.com/">Jekyll Bootstrap</a> adds some nice
  config setup, themes, and other great stuff that make blogging with Jekyll a
  near no-brainer.
</p>

<p>
  So, using Jekyll, my posts <em>are</em> HTML files. And I could use Vim once
  again to author all of my content. When you install Jekyll Bootstrap (which
  installs Jekyll), it provides a server that you can run that will listen to
  a <code>_posts</code> folder for updates. The instant you save something in
  there, it does its template compilation, and your new content is instantly
  viewable at <code>http://localhost:4000</code>. Really awesome.
</p>

<h2>Deployment</h2>

<p>
  I&rsquo;d learned a while back that people use <a href="http://pages.github.com/">
  Github Pages</a> &mdash; basically, a Github repo that will automatically
  be served to YOURNAME.github.com &mdash; for blogging. I&rsquo;d also learned, much
  more recently, that it supports Jekyll. Since I was already accustomed to
  source-controlling my work and some of my personal stuff with Github,
  deploying my blog simply by committing to a specific repo as normal sounded
  beyond perfect. Code, push, deploy became simply code and push.
</p>

<p>
  I was concerned at first that I wouldn&rsquo;t be able to push up drafts of
  posts without them being published automatically, until I had the &ldquo;duh&rdquo;
  realization that I could cut a branch (<code>$ git checkout -b "2012-04-06-my-post.html"</code>),
  write my post and push it in draft state to my hearts content. I could publish
  it when ready by merging the branch to master. Another fairly exact mirror of
  my normal workflow, and it feels great.
</p>

<p>
  Github Pages is really what seals the deal with Jekyll. Ftp is out of my life
  now, and it&rsquo;s bliss. Another important step was pointing my domain,
  marcocarag.com, to jazzcrazed.github.com. Hopefully, your registrar gives you
  this capability, but it&rsquo;s simply a matter of pointing an A record and
  a CNAME record to Github; the <a href="http://help.github.com/pages/">Github
  Pages Help</a> instructions are pretty accurate in this regard.
</p>

<h2>Resiliency</h2>

<p>
  I think it&rsquo;s hard to overstate the awesomeness of removing the overhead
  of something as complex as Wordpress. I&rsquo;ve been considering moving away
  from my current web host, but the idea of deciding on a new host,
  going through a new Wordpress install on that host, and putting my old blog
  data in its MySQL database almost makes me sick to my stomach.
</p>

<p>
  The sites generated by Jekyll are not married whatsoever to any particular
  host and the services they provide. It doesn&rsquo;t matter if my web host
  has a PHP server, .NET, Rails, or Node.js, or whether it uses MySQL, Postgres,
  or a document database. The end product is static HTML. If Github crashed and burned,
  I could upload that HTML anywhere else with hardly any setup needed.
</p>

<p>
  And as awesome the admin areas of Wordpress are, in no way does its
  <code>&lt;textarea&gt;</code> compare to Vim in my view. I&rsquo;m sure you&rsquo;d
  feel the same with your text editor of choice. The short of it: If you&rsquo;re
  a web developer intending to blog about code (or even not about code, if you&rsquo;re
  as bad with Vim commands outside of Vim as I am), Jekyll and Github Pages is
  likely the best way to go about it.
</p>

<figure class="fullWidth">
  <div class="curledShadow">
    <a href="https://plus.google.com/photos/101625155591132408533/albums/5728262585017161025/5728272140646561698">
      <img src="https://lh4.googleusercontent.com/-2C8s7WGIyZ8/T37pKYgBN6I/AAAAAAAAGRc/5cYNRbKJc9w/s757/P2235687.jpg"
        alt="Photo of a doll strapped to the front grill of a construction truck in DUMBO" />
    </a>
  </div>
  <figcaption>Happy Blogging!</figcaption>
</figure>
