<script>
  import { _ } from "svelte-i18n";
  import Who from "../components/Who.svelte";
  import Hero from "../components/Hero.svelte";

  export let segment;
</script>

<svelte:head>
  <title>
    {$_('title.index', { default: 'Movement Card - Right to the city' })}
  </title>
</svelte:head>

<Hero {segment} />

<!-- <section id="home" class="section_wrapper dark_bg">
  <div class="section_box header_section">
    <div class="row align_center">
      <h1 class="home_title">Movement Card</h1>

      <h2 class="home_subtitle">
        Use the buttons below to read your rights or see how you can get
        involved in the project.
      </h2>

      <a href="#rights" class="button_transparent">Read your rights!</a>

      <a href="#cta" class="button_transparent">Get involved</a>
    </div>
  </div>
</section> -->

<!-- <section id="about">

  <div class="section_wrapper dark_bg">

    <div class="section_box no_margins_bottom">

      <div class="row">

        <div class="twelvecol">
          <h2 class="title">The card</h2>

          <h3 class="subtitle">
            Movement Card aims to educate and inform all who have interactions
            with people moving in the public domain. Whether that's you, your
            friends, the security guard, or even a police officer. With a
            Movement Card you have an instant educational resource at your
            disposal.
          </h3>

          <div class="features_center nodisplay up_fade">
            <img src="lib/images/mc-mock-spread.png" alt="The Movement Card" />
          </div>

          <div class="features_right big_top_margin right_fade" />

        </div>

      </div>

    </div>

  </div>

  <div class="section_wrapper dark_bg">

    <div class="about_section">

      <div class="row">

        <div class="sixcol">
          <h2 class="page_subtitle">
            Your freedom to move should equal your freedom to speak!
          </h2>

          <h5 class="white">Clean, Simple &amp; Elegant</h5>

          <p>
            The movement card is part resource, part research and part response
            action created to promote freedom of movement. It is a worldwide
            project started in Scotland through a collaboration between Ukemi
            Project and Parkour Outreach.
          </p>

          <p>
            Our goal is to have an option for as many locations as possible and
            we would love to hear from you if you have the knowledge or means to
            contribute!
          </p>
        </div>

        <div class="sixcol last big_top_margin">
          <img
            src="lib/images/mc-mock-both-back.png"
            alt="The Movement Card front & back"
            class="left_fade" />
        </div>

      </div>

    </div>

  </div>

  <div class="section_wrapper dark_bg">

    <div class="about_section">

      <div class="row align-items-center">

        <div class="sixcol vert">
          <figure class="helper">

            <img
              src="lib/images/mc-mock-holder.png"
              alt="The Movement Card front & back"
              class="left_fade box-center" />
          </figure>
        </div>

        <div class="sixcol last big_top_margin">
          <h2 class="page_subtitle">Who's behind the project?</h2>

          <h5 class="white">
            A collaboration between Ukemi and Parkour Outreach. We have now
            partnered with Parkour Earth too!
          </h5>

          <p>
            <b>Ukemi</b>
            promote activity in highly urbanised areas and encourage a healthier
            society through digital design, product creation, and community arts
            development.
          </p>

          <ul class="store_icons">
            <li>
              <a href="https://ukemi.ninja">
                <i class="icon icon-web" />
              </a>
            </li>
            <li>
              <a href="https://fb.me/UkemiProject">
                <i class="icon icon-facebook" />
              </a>
            </li>
            <li>
              <a href="https://instagram.com/UkemiProject">
                <i class="icon icon-instagram" />
              </a>
            </li>
            <li>
              <a href="https://twitter.com/UkemiProject">
                <i class="icon icon-twitter" />
              </a>
            </li>
          </ul>

          <p>
            <b>Parkour Outreach</b>
            is a community interest company seeking to encourage physical
            activity, health and well-being by exploring funding opportunities,
            collaborations, and supporting new and potential Parkour
            communities.
          </p>

          <ul class="store_icons">
            <li>
              <a href="https://fb.me/parkouroutreach">
                <i class="icon icon-facebook" />
              </a>
            </li>
            <li>
              <a href="https://instagram.com/parkouroutreach">
                <i class="icon icon-instagram" />
              </a>
            </li>
            <li>
              <a href="https://twitter.com/parkouroutreach">
                <i class="icon icon-twitter" />
              </a>
            </li>
          </ul>

          <p>
            <b>Parkour Earth</b>
            is the International Federation for Parkour/Freerunning/Art du
            Déplacement. As such, it will be the custodian of the philosophy,
            integrity, and sovereignty of the sport internationally for and on
            behalf of the community.
          </p>

          <ul class="store_icons">
            <li>
              <a href="https://parkour.earth">
                <i class="icon icon-web" />
              </a>
            </li>
            <li>
              <a href="https://www.facebook.com/parkourearth">
                <i class="icon icon-facebook" />
              </a>
            </li>
            <li>
              <a href="https://www.instagram.com/parkourearth/">
                <i class="icon icon-instagram" />
              </a>
            </li>
            <li>
              <a href="https://twitter.com/parkourearth">
                <i class="icon icon-twitter" />
              </a>
            </li>
          </ul>
        </div>

      </div>

    </div>

  </div>

</section>

<section id="rights" class="section_wrapper dark_bg">

  <div class="section_box align_center no_margins_bottom">
    <h2 class="title">Right to the city</h2>

    <h3 class="subtitle">
      The following will guide you through the legal rights relating to the
      typical reasons given by security guards/landowners.
      <br />
      <br />
      Always train with respect for others and your surroundings. Do not run
      away or act suspiciously if police or others approach you. If you are
      asked to move on, then you should explain what Parkour is, be respectful
      and move on. It is better to be on good terms with landowners and/or the
      police if you, or other practitioners, want to return another day.
    </h3>
  </div>

  <div class="section_box no_margins_top">

    <div class="row">

      <div class="sixcol">
        <h2 class="page_subtitle">"This is private property"</h2>
        <p>
          If the land is owned by someone, it is private property. Confusingly,
          this includes land that is publicly accessible. This means that almost
          all land in Scotland will be private property, but this does not
          always mean you cannot be there.
        </p>

        <p>
          If a landowner has made their land accessible to the public, i.e. a
          public square, you have rights of access under the Land Reform
          (Scotland) Act 2003 as long as you are behaving responsibly. This is
          commonly referred to as the Right to Roam.
        </p>

        <p>
          You are not breaking the law by training on private land that is open
          to the public, so you should not be treated as if you are breaking the
          law. Landowners should be reminded of this if they move you on for
          this reason.
        </p>

        <p>
          It is worth noting that the Right to Roam does not apply in certain
          areas, for example, land that is close to or within a building; school
          grounds; and construction/demolition sites.
        </p>
      </div>

      <div class="sixcol last">
        <h2 class="page_subtitle">"We are liable if you hurt yourself"</h2>

        <p>
          Under the Occupiers’ Liability (Scotland) Act 1960, occupiers of
          property owe a duty of care to take care of people entering their land
          or premises as is reasonable in all of the circumstances.
        </p>

        <p>
          An occupier, for these purposes, is someone occupying or having
          control of land or other premises - this would include Landowners and
          their security guards. Landowners are generally worried about being
          liable if you hurt yourself whilst practising Parkour on their land.
        </p>

        <p>
          However, liability would only arise if an injury occurs in one of the
          following situations
        </p>

        <ul>
          <li>
            An injury occurs as result of dangers that are due to the state of
            the premises, e.g. slippery or uneven floors; or
          </li>

          <li>
            An injury occurs as a result of anything done or omitted to be done
            by the occupier that has created a danger on the premises, i.e. they
            have not warned you about something dangerous on their premises.
          </li>
        </ul>

        <p>
          Even if you tried to sue the landowner, they would be able to plead
          the defence of volenti non fit injuria - this means that you
          voluntarily accepted the risk of being injured. The landowner would
          not be liable if you voluntarily accept a risk that is inherent in
          Parkour.
        </p>

        <p>
          As such, landowners are not liable if they have made you aware of any
          danger on the premises or if you have voluntarily put yourself at
          risk. Landowners should therefore be reminded that they would not be
          liable if you hurt yourself when voluntarily training Parkour on their
          land.
        </p>
      </div>

    </div>

    <div class="row">

      <div class="sixcol">
        <h2 class="page_subtitle">"We have you on CCTV"</h2>
        <p>
          If this reason is being given to you, the landowner is assuming that
          you are doing something unlawful. You should let them know that you
          are not doing anything unlawful and that you are happy to captured on
          CCTV.
        </p>

        <p>
          CCTV is merely capturing evidence of what you are doing and is
          definitely not a reason for you to move on. If you are training with
          respect, then the CCTV will only show that you are not breaking the
          law. It is likely that they will then give you one of the reasons that
          we have set out above, i.e. private property and/or occupiers’
          liability.
        </p>
      </div>

      <div class="sixcol last">
        <h2 class="page_subtitle">"We will call the Police"</h2>

        <p>
          If the landowner threatens to call the police, the landowner is
          assuming that you are doing something unlawful. The police should only
          be involved if there is a crime. Practising Parkour responsibly with
          respect for others and your surroundings is not a crime. As such, even
          if the police were called to the premises, it is unlikely that they
          would require you to move.
        </p>

        <p>
          However, if the police request that you move on, you should explain
          what you are doing and then move on upon their request.
        </p>
      </div>

    </div>

    <div class="row">
      <div class="align_center">
        <br />
        <br />
        <p class="white">
          The information here is for educational purposes only and does
          <strong>not</strong>
          constitute legal advice.
        </p>
      </div>
    </div>
  </div>

</section>

<section id="cta" class="section_wrapper">
  <div class="section_box align_center">
    <h2 class="">Help us cover your country!</h2>

    <p class="text-dark">
      Every country needs a champion to step forward to make this happen. We
      will supply the design as well as provide guidance on how to build your
      team and get the information you need. If this is you then get in contact
      by emailing us or with a DM on social media.
    </p>

    <div class="bounce_fade">
      <a href="mailto:founders@ukemi.ninja" class="button_gold">
        Send us an email
      </a>
    </div>
  </div>
</section> -->

<!-- <Who /> -->
