# index.html-
<!DOCTYPE html>
<html lang="en">
<head> "<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-2635047771308146"
     crossorigin="anonymous"></script>"
  <meta charset="utf-8"<meta name="google-adsense-account" content="ca-pub-2635047771308146">" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>CookSmart – Ask for any recipe & get a step‑by‑step guide</title>
  <meta name="description" content="Type any dish you want to cook and get a clear, step‑by‑step guide, related videos, and mouth‑watering images. Fully responsive, fast, and SEO‑ready." />
  <meta name="keywords" content="recipes, cooking guide, how to cook, step by step recipes, easy recipes, cooking videos" />
  <link rel="canonical" href="https://example.com/" />

  <!-- Open Graph -->
  <meta property="og:title" content="CookSmart – Ask for any recipe" />
  <meta property="og:description" content="Get step‑by‑step instructions, videos, and photos for any dish you ask." />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://example.com/" />
  <meta property="og:image" content="https://source.unsplash.com/featured/?cooking,food" />

  <!-- Twitter Cards -->
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="CookSmart – Ask for any recipe" />
  <meta name="twitter:description" content="Type any dish and get a clear, step‑by‑step guide with videos and images." />
  <meta name="twitter:image" content="https://source.unsplash.com/featured/?recipe" />

  <!-- Preconnect hints -->
  <link rel="preconnect" href="https://i.ytimg.com" crossorigin>
  <link rel="preconnect" href="https://www.youtube.com" crossorigin>
  <link rel="preconnect" href="https://source.unsplash.com" crossorigin>

  <!-- Favicon (optional) -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='0.9em' font-size='90'>🍳</text></svg>">

  <style>
    :root {
      --bg: #0f172a;        /* slate-900 */
      --bg-soft: #111827;   /* gray-900 */
      --card: #111827;
      --muted: #9ca3af;     /* gray-400 */
      --text: #e5e7eb;      /* gray-200 */
      --accent: #f59e0b;    /* amber-500 */
      --ring: rgba(245, 158, 11, 0.35);
      --success: #10b981;   /* emerald-500 */
      --danger: #ef4444;    /* red-500 */
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius: 18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0; font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Cantarell,Inter,Helvetica,Arial,sans-serif;
      background: radial-gradient(1200px 800px at 10% -10%, #1f2937 0%, var(--bg) 40%) no-repeat fixed;
      color:var(--text);
      line-height:1.6;
    }
    header{
      position:sticky; top:0; z-index:20; backdrop-filter: blur(10px);
      background: linear-gradient(180deg, rgba(17,24,39,.8), rgba(17,24,39,.4));
      border-bottom: 1px solid rgba(255,255,255,.06);
    }
    .container{max-width:1100px; margin:0 auto; padding: clamp(16px, 2vw, 24px);}
    .brand{display:flex;align-items:center;gap:10px}
    .brand .logo{font-size:28px}
    .brand h1{font-size:20px;margin:0}
    .muted{color:var(--muted)}

    .hero{display:grid;grid-template-columns:1.2fr .8fr; gap:24px; align-items:center; padding-top:24px}
    @media (max-width: 900px){ .hero{grid-template-columns:1fr} }

    .card{background: linear-gradient(180deg, rgba(255,255,255,.04), rgba(255,255,255,.02)); border:1px solid rgba(255,255,255,.08); border-radius: var(--radius); box-shadow: var(--shadow)}
    .search-card{padding:20px}
    .search{display:flex; gap:10px; align-items:center; flex-wrap:wrap}
    .search input{
      flex:1; min-width:240px;
      padding:14px 16px; border-radius:14px; border:1px solid rgba(255,255,255,.08);
      background:#0b1220; color:var(--text); outline:none;
      box-shadow: inset 0 0 0 1px transparent, 0 0 0 0 transparent;
      transition:.2s box-shadow, .2s border-color;
    }
    .search input:focus{ box-shadow: 0 0 0 6px var(--ring); border-color: rgba(245,158,11,.4) }
    .btn{padding:12px 16px; border-radius:14px; border:1px solid rgba(255,255,255,.08); background:linear-gradient(180deg, #f59e0b, #d97706); color:#0b1220; font-weight:600; cursor:pointer}
    .btn:disabled{opacity:.6; cursor:not-allowed}
    .chips{display:flex; gap:8px; flex-wrap:wrap; margin-top:12px}
    .chip{padding:6px 10px; border-radius:999px; background:rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.08); cursor:pointer; font-size:13px}
    .chip:hover{background:rgba(255,255,255,.1)}

    .gallery{display:grid; grid-template-columns:repeat(3,1fr); gap:10px}
    .gallery img{width:100%; height:150px; object-fit:cover; border-radius:14px; border:1px solid rgba(255,255,255,.08)}
    @media (max-width: 700px){ .gallery{grid-template-columns:repeat(2,1fr)} }

    main .section{margin-top:28px}
    h2{margin:0 0 8px; font-size:22px}

    .results{display:grid; grid-template-columns: 1.1fr .9fr; gap:24px}
    @media (max-width: 1000px){ .results{grid-template-columns: 1fr} }

    .recipe-card{padding:20px}
    .recipe-title{display:flex; align-items:flex-start; justify-content:space-between; gap:10px}
    .recipe-title h3{margin:0; font-size:22px}
    .badge{font-size:12px; padding:4px 8px; border-radius:999px; border:1px solid rgba(255,255,255,.12); color:var(--muted)}

    .two-col{display:grid; grid-template-columns: .8fr 1.2fr; gap:16px}
    @media (max-width: 700px){ .two-col{grid-template-columns: 1fr} }

    ul, ol{margin:8px 0 0 20px}
    li{margin:6px 0}

    .videos-card{padding:20px}
    .video-embed{position:relative; width:100%; aspect-ratio:16/9; border-radius:14px; overflow:hidden; border:1px solid rgba(255,255,255,.08)}
    .video-embed iframe{position:absolute; inset:0; width:100%; height:100%; border:0}

    .ads-card{padding:16px; display:grid; gap:8px}
    .ads-note{font-size:12px; color:var(--muted)}

    footer{margin:40px 0; color:var(--muted); font-size:14px}
    .notice{font-size:12px; color:var(--muted)}
  </style>

  <!-- Structured data for the website and on-site search (SEO) -->
  <script type="application/ld+json" id="site-jsonld">
    {
      "@context": "https://schema.org",
      "@type": "WebSite",
      "name": "CookSmart",
      "url": "https://example.com/",
      "potentialAction": {
        "@type": "SearchAction",
        "target": "https://example.com/?q={search_term_string}",
        "query-input": "required name=search_term_string"
      }
    }
  </script>
</head>
<body>
  <header ></script>">
    <div class="container" style="display:flex; align-items:center; justify-content:space-between; gap:16px">
      <div class="brand">
        <div class="logo">🍳</div>
        <h1>CookSmart</h1>
        <span class="muted">Your instant cooking guide</span>
      </div>
      <nav class="muted" aria-label="Top navigation">
        <a href="#videos" class="muted" style="margin-right:14px; text-decoration:none">Videos</a>
        <a href="#photos" class="muted" style="text-decoration:none">Photos</a>
      </nav>
    </div>
  </header>

  <div class="container">
    <section class="hero">
      <div class="card search-card">
        <h2 style="margin-top:0">What do you want to cook?</h2>
        <p class="muted" style="margin:6px 0 14px">Type a dish name (e.g., "chicken curry", "veg pasta", "omelette"). You'll get steps, ingredients, videos, and images.</p>
        <form id="searchForm" class="search" role="search" aria-label="Recipe search">
          <label for="q" class="visually-hidden" style="position:absolute;left:-9999px">Dish or recipe</label>
          <input id="q" name="q" type="search" placeholder="Search any recipe…" autocomplete="off" />
          <button id="searchBtn" class="btn" type="submit">Get Guide</button>
        </form>
        <div class="chips" aria-label="Popular quick picks">
          <button class="chip" data-q="pasta" type="button">Pasta</button>
          <button class="chip" data-q="omelette" type="button">Omelette</button>
          <button class="chip" data-q="pancakes" type="button">Pancakes</button>
          <button class="chip" data-q="chicken curry" type="button">Chicken Curry</button>
          <button class="chip" data-q="fried rice" type="button">Fried Rice</button>
        </div>
      </div>
      <div class="card" style="padding:0">
        <picture>
          <source srcset="https://source.unsplash.com/900x700/?home-cooking,food" media="(min-width: 900px)">
          <img src="https://source.unsplash.com/700x500/?cooking,ingredients" alt="Assorted cooking ingredients and utensils" loading="lazy" style="width:100%; height:100%; object-fit:cover; border-radius: var(--radius)">
        </picture>
      </div>
    </section>

    <main>
      <section id="results" class="section results" aria-live="polite" aria-busy="false" hidden>
        <article class="card recipe-card">
          <div class="recipe-title">
            <h3 id="recipeTitle">Recipe</h3>
            <span class="badge" id="matchBadge" title="How we created this guide">guide source</span>
          </div>
          <div class="two-col">
            <div>
              <h4>Ingredients</h4>
              <ul id="ingredients"></ul>
            </div>
            <div>
              <h4>Steps</h4>
              <ol id="steps"></ol>
            </div>
          </div>
        </article>

        <aside id="adAfterGuide" class="card ads-card" aria-label="Advertisement area">
          <strong>Sponsored</strong>
          <!-- Replace ADSENSE_CLIENT and ADSENSE_SLOT below. See JS config. -->
          <ins class="adsbygoogle"
               style="display:block"
               data-ad-client=""
               data-ad-slot=""
               data-ad-format="auto"
               data-full-width-responsive="true"></ins>
          <div class="ads-note">Ads appear here after the recipe guide. Configure your Google AdSense client and slot IDs in the code.</div>
        </aside>

        <section id="videos" class="card videos-card">
          <h4 style="margin-top:0">Related videos</h4>
          <div class="video-embed">
            <iframe id="ytSearch" title="Recipe videos" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen referrerpolicy="strict-origin-when-cross-origin"></iframe>
          </div>
        </section>

        <section id="photos" class="card videos-card">
          <h4 style="margin-top:0">Photo inspiration</h4>
          <div id="gallery" class="gallery" aria-label="Recipe image gallery"></div>
          <p class="notice">Images served via Unsplash Source for demo purposes. Add your own images or CDN for production.</p>
        </section>
      </section>

      <section class="section">
        <div class="card videos-card">
          <h3 style="margin:0">Recently searched</h3>
          <ul id="recentList" class="muted" style="margin:10px 0 0 18px"></ul>
        </div>
      </section>
    </main>

    <footer>
      <div>© <span id="year"></span> CookSmart. Built for speed, accessibility, and SEO.</div>
    </footer>
  </div>

  <script>
    // =============================
    // CONFIG: AdSense + Images
    // =============================
    // Insert your AdSense IDs here (or set at runtime):
    window.ADSENSE_CLIENT = "" </script> ></script>  // e.g., ca-pub-1234567890123456
    window.ADSENSE_SLOT   = "" // e.g., 1234567890

    // How many photos to show in the gallery:
    const PHOTO_COUNT = 9;

    // =============================
    // Minimal recipe knowledge base
    // =============================
    const RECIPES = [
      {
        id: 'pasta',
        names: ['pasta', 'tomato pasta', 'veg pasta', 'red sauce pasta'],
        ingredients: [
          '200g pasta (penne/spaghetti)', '2 tbsp olive oil', '3 cloves garlic, minced', '1 small onion, chopped',
          '2 cups tomatoes (fresh or canned)', '1/2 tsp chili flakes', '1 tsp mixed herbs', 'Salt & pepper', 'Parmesan / basil to finish'
        ],
        steps: [
          'Boil pasta in salted water until al dente; reserve 1/2 cup pasta water.',
          'Sauté onion and garlic in olive oil until fragrant.',
          'Add tomatoes, chili flakes, herbs; simmer 8–10 minutes.',
          'Toss in pasta; loosen with reserved water as needed.',
          'Adjust seasoning. Finish with parmesan and basil.'
        ]
      },
      {
        id: 'omelette',
        names: ['omelet', 'omelette', 'masala omelette', 'cheese omelette'],
        ingredients: [
          '2–3 eggs', '1 tbsp butter/oil', 'Salt & pepper', '2 tbsp onion (finely chopped)', '1 tbsp capsicum/tomato', 'Grated cheese (optional)'
        ],
        steps: [
          'Whisk eggs with salt and pepper (and a splash of milk).',
          'Melt butter in a non‑stick pan on medium heat.',
          'Pour eggs, swirl; add veggies/cheese on one side.',
          'When almost set, fold and cook 30–60 sec more.',
          'Slide onto a plate and serve hot.'
        ]
      },
      {
        id: 'pancakes',
        names: ['pancakes', 'fluffy pancakes'],
        ingredients: [
          '1 cup flour', '2 tbsp sugar', '1 tsp baking powder', '1/2 tsp baking soda', 'Pinch salt',
          '3/4 cup milk', '1 egg', '1 tbsp melted butter', '1 tsp vanilla'
        ],
        steps: [
          'Whisk dry ingredients in a bowl.',
          'Whisk wet ingredients separately; combine to a thick batter (do not overmix).',
          'Rest 5–10 minutes.',
          'Cook 1/4 cup scoops on a lightly oiled pan until bubbles form; flip and cook through.',
          'Serve with syrup, fruit, or butter.'
        ]
      },
      
        ]
      },
      {
        id: 'fried-rice',
        names: ['fried rice', 'veg fried rice', 'egg fried rice'],
        ingredients: [
          '3 cups cooked cooled rice', '1–2 tbsp oil', '1/2 cup mixed veggies', '2 cloves garlic, minced',
          'Soy sauce 1–2 tbsp', 'Pepper', 'Spring onions', 'Eggs or tofu (optional)'
        ],
        steps: [
          'Heat wok; add oil and garlic; stir‑fry veggies 2–3 minutes.',
          'Push aside; scramble eggs if using.',
          'Add rice; toss on high heat; add soy sauce and pepper.',
          'Finish with spring onions.'
        ]
      }
    ];

    // fallback guide generator if we don't have a specific recipe
    function generateGenericGuide(query){
      const q = query.trim();
      return {
        title: capitalize(q) + ' – Basic Home‑Style Guide',
        ingredients: [
          'Main ingredient(s) for ' + q,
          'Aromatics (onion/garlic/ginger as suitable)',
          'Cooking fat (oil/butter)',
          'Seasoning (salt, pepper, herbs/spices)',
          'Optional garnish (fresh herbs, lemon, sauce)'
        ],
        steps: [
          'Prep ingredients: wash, peel, and cut appropriately.',
          'Heat pan/pot; add oil/fat and aromatics; cook until fragrant.',
          'Add main ingredient(s); cook until nearly done.',
          'Season and add liquids/sauces if needed; simmer to desired texture.',
          'Taste, adjust seasoning, garnish, and serve.'
        ],
        source: 'generic template'
      };
    }

    function findRecipe(query){
      const q = query.toLowerCase();
      for(const r of RECIPES){
        if(r.names.some(n => q.includes(n))){
          return {
            title: capitalize(query),
            ingredients: r.ingredients,
            steps: r.steps,
            source: 'curated'
          };
        }
      }
      return generateGenericGuide(query);
    }

    function setYouTubeSearch(query){
      const iframe = document.getElementById('ytSearch');
      const list = encodeURIComponent(query + ' recipe');
      // YouTube search playlist embed
      iframe.src = `https://www.youtube.com/embed?listType=search&list=${list}`;
    }

    function setGallery(query){
      const g = document.getElementById('gallery');
      g.innerHTML = '';
      const kw = encodeURIComponent(query + ', food, recipe');
      for(let i=0;i<PHOTO_COUNT;i++){
        const w = i % 3 === 0 ? 700 : 500; // vary sizes a bit
        const h = i % 2 === 0 ? 500 : 400;
        const url = `https://source.unsplash.com/${w}x${h}/?${kw}&sig=${Date.now()+i}`;
        const img = new Image();
        img.loading = 'lazy';
        img.decoding = 'async';
        img.alt = `${query} photo ${i+1}`;
        img.src = url;
        g.appendChild(img);
      }
    }

    function updateRecipeJSONLD(title, ingredients, steps){
      const data = {
        '@context': 'https://schema.org',
        '@type': 'Recipe',
        'name': title,
        'recipeIngredient': ingredients,
        'recipeInstructions': steps.map(s => ({ '@type': 'HowToStep', 'text': s })),
        'author': { '@type': 'Organization', 'name': 'CookSmart' },
        'image': `https://source.unsplash.com/900x600/?${encodeURIComponent(title)},food`,
        'description': `Step‑by‑step guide for ${title}.`,
        'isAccessibleForFree': true
      };
      let node = document.getElementById('recipe-jsonld');
      if(!node){
        node = document.createElement('script');
        node.type = 'application/ld+json';
        node.id = 'recipe-jsonld';
        document.head.appendChild(node);
      }
      node.textContent = JSON.stringify(data);
    }

    function showResults(){
      document.getElementById('results').hidden = false;
      document.getElementById('results').setAttribute('aria-busy','false');
    }

    function capitalize(s){return s.replace(/\b\w/g, c => c.toUpperCase());}

    function addRecent(q){
      const key = 'cooksmart_recent';
      const list = JSON.parse(localStorage.getItem(key) || '[]');
      const trimmed = q.trim();
      if(!trimmed) return;
      const exists = list.find(x => x.toLowerCase() === trimmed.toLowerCase());
      if(!exists){
        list.unshift(trimmed);
      }
      const kept = list.slice(0,8);
      localStorage.setItem(key, JSON.stringify(kept));
      renderRecent();
    }

    function renderRecent(){
      const key = 'cooksmart_recent';
      const list = JSON.parse(localStorage.getItem(key) || '[]');
      const ul = document.getElementById('recentList');
      ul.innerHTML='';
      list.forEach(item => {
        const li = document.createElement('li');
        const a = document.createElement('a');
        a.href = '#'; a.textContent = item; a.addEventListener('click', e => { e.preventDefault(); runSearch(item); });
        li.appendChild(a); ul.appendChild(li);
      });
    }

    function configureAds(){
      const client = window.ADSENSE_CLIENT || '';
      const slot = window.ADSENSE_SLOT || '';
      const ins = document.querySelector('#adAfterGuide ins.adsbygoogle');
      if(ins){
        ins.setAttribute('data-ad-client', client);
        ins.setAttribute('data-ad-slot', slot);
      }
      if(client && slot){
        // Load AdSense script only if IDs are provided
        const s = document.createElement('script');
        s.async = true;
        s.src = 'https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=' + encodeURIComponent(client);
        s.crossOrigin = 'anonymous';
        s.onload = () => {
          try { (adsbygoogle = window.adsbygoogle || []).push({}); } catch(e) { console.warn('AdSense push error', e); }
        };
        document.head.appendChild(s);
      } else {
        // Show a subtle hint if not configured
        const note = document.createElement('div');
        note.className = 'ads-note';
        note.textContent = 'Demo mode: set ADSENSE_CLIENT and ADSENSE_SLOT in the source to enable ads.';
        document.getElementById('adAfterGuide').appendChild(note);
      }
    }

    function runSearch(query){
      const results = document.getElementById('results');
      results.setAttribute('aria-busy','true');
      const { title, ingredients, steps, source } = findRecipe(query);
      document.getElementById('recipeTitle').textContent = title;
      document.getElementById('matchBadge').textContent = source === 'curated' ? 'from curated base' : 'smart generic';

      const ingUl = document.getElementById('ingredients');
      const stOl = document.getElementById('steps');
      ingUl.innerHTML = '';
      stOl.innerHTML = '';
      ingredients.forEach(item => { const li = document.createElement('li'); li.textContent = item; ingUl.appendChild(li); });
      steps.forEach(step => { const li = document.createElement('li'); li.textContent = step; stOl.appendChild(li); });

      setYouTubeSearch(query);
      setGallery(query);
      updateRecipeJSONLD(title, ingredients, steps);
      addRecent(query);
      showResults();
      window.scrollTo({ top: results.offsetTop - 70, behavior: 'smooth' });
    }

    // Event wiring
    document.getElementById('searchForm').addEventListener('submit', e => {
      e.preventDefault();
      const q = document.getElementById('q').value.trim();
      if(q){ runSearch(q); }
    });
    document.querySelectorAll('.chip').forEach(btn => btn.addEventListener('click', () => runSearch(btn.dataset.q)));
    document.getElementById('q').addEventListener('keydown', e => { if(e.key === 'Enter'){ e.preventDefault(); document.getElementById('searchBtn').click(); }});

    // Init
    document.getElementById('year').textContent = new Date().getFullYear();
    renderRecent();
    configureAds();

    // If URL has ?q=...
    const params = new URLSearchParams(location.search);
    const qParam = params.get('q');
    if(qParam){
      document.getElementById('q').value = qParam;
      runSearch(qParam);
    }
  </script>
</body>
</html>
