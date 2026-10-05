This is the code for [Andy Zeng](https://andyzeng.github.io/)'s academic website. Notably, this uses [Isotope](https://isotope.metafizzy.co/) to create subpages, so you can get fancy with "sort by category" features if you want to. You can customize the `data-filter` and `data-category` fields, as well as Isotope parameters in the JS code at the bottom of `index.html`. Feel free to download this for your own personal use. Remember to delete the analytics tags at the top of `index.html` that you do not want on your own website. I'd appreciate a link back to my website. Inspired by [Jon's website](https://jonbarron.info/).

## Research categories

The Research section groups publications by their primary contribution, with each paper appearing once:

- **Embodied AI:** robot learning, manipulation, VLA policies, and affordance grounding.
- **Foundation Model:** vision-language reasoning and multimodal evaluation; earlier recognition, compositional learning, and document-understanding papers are included here.
- **Generative Models & World Models:** image/video generation, diffusion-based perception, and world modeling.
- **Reinforcement Learning:** reinforcement-learning post-training, including multimodal reasoning and VLA fine-tuning.

The October 2026 catalog includes the 32 entries on the author's Google Scholar profile plus the public PerturBot manuscript/repository. Publication venues follow the profile; paper metadata and links are checked against arXiv, official proceedings, or project pages. PerturBot remains labeled as a manuscript without an unverified paper URL or acceptance claim.

Entries remain static HTML in `index.html`. To add a paper, copy a `.publication-entry` into the appropriate group, give it a unique `id`, one `research-*` class, `data-category="publication"`, `data-year`, `data-author-position`, and `data-lead-author`. Within each group, Mingyu Liu's first/co-first-author papers come first; other papers follow in ascending order of his position in the complete author list. Within the first/co-first group or the same author position, use publication year and date, newest first. VideoAfford marks Hanqing Wang and Mingyu Liu as equal contributors, as confirmed by the author.

Each entry displays **Webpage · Code · PDF**. Preserve verified project/code URLs; when either is unavailable, point that label to the paper's PDF and mark the fallback in its tooltip and `data-link-fallback` attribute. PerturBot has no verified public PDF: its Webpage points to the public repository and its PDF label remains visibly disabled until a link is supplied. Do not invent a URL or publish a private draft as a substitute. Use local thumbnails with intrinsic `width`, `height`, and descriptive `alt` text. Category counts are computed from entries; section and category selections are remembered separately when browser storage is available.

Preview locally with `python3 -m http.server 8765 --bind 127.0.0.1`, then open `http://127.0.0.1:8765/` and select **Research**. No build step is required.

## Experience

The **Experience** tab uses a single-column list with local institution logos, grouped into Research & Industry and Education. It includes ByteDance Seed, Shanghai AI Laboratory, Shanghai Jiao Tong University / MVIG, Zhejiang University, and HUST. ByteDance lists the Multimodal Interaction and World Model team; Shanghai AI Laboratory lists Tong He and Jiangmiao Pang. HUST shows education only, and the NTU visit is omitted from this tab. No missing start/end dates or additional positions are inferred.

The five displayed date ranges are taken from the supplied CV: ByteDance Nov. 2025–Present, Shanghai AI Laboratory Dec. 2024–Oct. 2025, SJTU Dec. 2022–Nov. 2023, Zhejiang Sep. 2024–Present, and HUST Sep. 2020–Jun. 2024. The CV itself is not included in the website. SJTU uses a blue display variant of the existing emblem; the original red asset is retained.

Update the static entries in `#experience` when roles or dates change. Keep institution logos proportional and local; asset sources are recorded in `images/institutions/README.md`. The tab shares the existing navigation persistence without changing the Research filters or paper order.

## Profile

The portrait in the original right-hand profile slot uses `images/profile-portrait-hd.jpg`, a 1031-by-1031 center crop of the author's supplied illustration screenshot. On October 5, 2026, GPT Image 2 removed the screenshot's circular crop guide, dimmed outer overlay, and top gray strip using the author's supplied API. This is an AI-repaired image, not a recovered original. The display size and rounded corners remain unchanged. The earlier 200-by-200 LinkedIn thumbnail is retained as `images/linkedin-portrait.jpg`. Keep profile images local rather than relying on expiring LinkedIn image URLs. Experience links Jiangmiao Pang to his personal homepage and lists Yuliang Liu and Xiang Bai as undergraduate advisors.
