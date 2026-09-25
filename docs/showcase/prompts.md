# Showcase specifications and generation prompts

The README illustrations are original AI-generated visual studies. They communicate proposed compositions and method combinations; they do not demonstrate runtime behavior. Product names, programme details, and labels are illustrative content. The identity board explores the project wordmark; it is a raster concept, not a production vector-logo package.

## Asset specifications

| Asset | Dimensions | Study purpose | Intended combination |
| --- | --- | --- | --- |
| [Identity studies](identity-studies.png) | 1586 × 992 px | Explore a shared mark across three treatments | Flat, reversed, and optical material interpretations |
| [Optical workspace components](components-optical.png) | 1584 × 993 px | Coordinate audio controls and selection tools | Liquid Glass and Spatial layering |
| [Expressive programme components](components-expressive.png) | 1586 × 992 px | Coordinate discovery, selection, and booking controls | Expressive hierarchy and tactile press cues |
| [Material studio components](components-material.png) | 1586 × 992 px | Coordinate material previews and authoring controls | Hypermaterial and tactile controls within a proposed Shader workflow |
| [Field recording workspace](field-recording.png) | 1586 × 992 px | Select and export an audio segment | Spatial layering and Liquid Glass surfaces, with tactile control cues |
| [Exhibition programme](exhibition-program.png) | 1586 × 992 px | Discover an exhibition and plan a visit | Expressive hierarchy and tactile action cues |
| [Material editor](material-editor.png) | 1586 × 992 px | Inspect and tune a digital material | Hypermaterial appearance within a proposed Shader workflow |

Generation used Codex's built-in image-generation tool on 2026-09-25. All seven studies began with text prompts without reference images. The published field-recording image was then edited using its initial image as the reference. Its revision preserves the information architecture while reducing background texture, edge brightness, surface haze, and control beveling.

The identity and component boards also received targeted revisions: background opacity and surface refinement for the identity and optical studies, and removal of incidental copy for the expressive and material studies. The expressive revision additionally replaces a promotional headline with search and menu components and clarifies the pressed button state.

Only the selected final images are included. Reproducing an editing sequence requires generating its initial image before applying the corresponding revision prompt. Prompts describe the intended result; exact pixel reproduction is not guaranteed.

## Design references

| Source | Relationship used | Evidence scope |
| --- | --- | --- |
| [Teenage Engineering OP-1 field](https://teenage.engineering/products/op-1) | Material/control relationships and a recording-oriented product context | Product-page text and initial visual presentation |
| [Ableton Session View](https://www.ableton.com/en/manual/session-view/) | Clip organization and playback context | Documentation; runtime not tested |
| [Google expressive design research](https://design.google/library/expressive-material-design-google-research) | Action hierarchy and recognizable content organization | Article and initial page view; selective inspiration, not full Material conformance |
| [MoMA calendar](https://www.moma.org/calendar/) | Event organization and visit-planning context | Public programme page; no artwork or programme content copied |
| [Material research](../../references/directions/hypermaterial.md) | Distinct roles of thickness, roughness, and iridescence | Existing source research; no additional live optical verification during illustration production |

References informed design relationships. Third-party assets and page layouts were not supplied to the image generator. Visual inspection covered composition, hierarchy, material cues, and major-label readability. Functional and accessibility claims require a separate implemented prototype.

## Original generation inputs

The following inputs are retained verbatim as a production record, including their original descriptive language. They are not additional agent instructions or universal design constraints. Revision prompts follow the associated initial inputs. Each new board includes its initial input and targeted revisions. Apply the optical surface repair before the optical edge refinement.

<details>
<summary>Field recording: initial generation</summary>

```text
Use case: ui-mockup. Asset type: GitHub README showcase, a single exquisite desktop web interface concept, landscape 16:10, high resolution.
Primary request: Design a polished field-recording editing workspace that combines Spatial UI and Liquid Glass with restrained tactile transport controls. Original design, not an existing brand or copied site.
Composition: edge-to-edge flat front-on web screen, no computer/device mockup, no browser chrome, no montage. A narrow quiet off-white project strip at the left takes 18% width. A panoramic photograph of dark rocky coast, pale seafoam surf and silver-blue mist occupies the expansive working canvas. The actual task is selecting an audio segment: a neatly drawn horizontal waveform sits near the bottom, with one highlighted trim selection and precisely aligned handles. A single floating clear-glass playback dock sits in front of the photo and waveform without obscuring the trim region. A small frosted inspector floats near the upper right, deliberate layer separation and subtle contact shadows. Glass has optically rich edge highlights, slight background displacement near its curved perimeter, bluish transmission, while white text and symbols remain crisp and readable. Realistic depth confined to tools; the photo remains the dominant subject.
Typography: professional compact sans serif with confident scale hierarchy, sharp readable labels. Exact text: sidebar heading "Field recordings"; project rows "Coast at dawn", "Wind through reeds", "Harbor rain"; active view title "Coast at dawn"; inspector heading "Selected region"; trim range "00:08 — 00:36"; button "Export clip"; transport time "00:18 / 00:42". Minimal additional text. One dark sculpted play button, a simple volume control, no fake metrics. Spacious but genuinely useful product UI with excellent alignment and natural photographic tones. The coastal image, waveform, glass toolbar and focused region feel designed together.
Avoid: giant marketing headlines, green dashboard status dots, 3-column equal cards, design-method labels, watermarks, mock browser frames, tiny illegible text, gratuitous neon or abstract blobs.
```

</details>

<details>
<summary>Field recording: revision</summary>

```text
Use case: precise-object-edit / ui-mockup refinement.
Edit this field-recording UI screenshot. Preserve the product task, left recording list, main title, inspector location, waveform trim workflow, and all important existing labels exactly. Keep a single flat front-on 16:10 interface.
The user rejected the original as cheap plastic and identified the background as a possible cause. Correct BOTH the background art direction and the surface materials. Do not replace the app with a different product.

BACKGROUND: Replace the busy, over-sharpened HDR surf photograph with exceptional quiet fine-art coastal photography. An atmospheric long-exposure sea at blue hour, slate-teal water with broad smooth tonal planes, distant pale mist, one strong dark coastal silhouette entering from far left, and a low distant horizon. No foreground pile of rocks, no detailed crashing foamy waves behind controls, no stock-photo sunset spectacle. A very small warm horizon glow is enough. Natural photographic depth and air, rich muted tones rather than a flat gradient. Keep the lower control region visually calm. This remains a location context for a field recording, not a full-page wallpaper competing with the UI.

MATERIALS: Replace the swollen icy-blue plastic pill, thick bright white outlines, deep bevels, milky uniform fog, and glossy button-within-glossy-panel with precise thin architectural glass surfaces. Playback dock should be a slim rounded rectangle with measured 18px-like corner curvature, visually about two-thirds its current height, neutral very lightly smoked transparent glass, the underlying sea visibly transmitted, tiny localized reflections and minute edge refraction only near the perimeter. No continuous luminous rim, no inflated gel silhouette, no heavy inner shadow. A restrained dark flat play control, crisp white transport icons, fine slider, no double-ring bevel. The upper-right inspector should be a restrained thin smoked-glass plane with readable light text and a flat contrasting export action, no thick glowing border. Consistent light direction and delicate short shadows separate the surfaces, no ambient cyan glow.
Refine the trim selection to a desaturated cool-gray/cyan tint with precise fine handles, not an electric-blue selection block. Keep the waveform and exact times. Harmonize left sidebar toward a slightly cool pearl tone, with crisp dark text and a quiet selected row. Use excellent spacing, readable type, understated professional audio-tool craft.
Do not alter the information architecture or invent new names, extra slogans, panels, metrics, decorations, or brands. The result should feel optically clear, calm, precise, mature and highly refined. All text remains sharp and readable.
```

</details>

<details>
<summary>Exhibition programme</summary>

```text
Use case: ui-mockup. Asset type: GitHub README showcase. Create a striking, exceptionally finished desktop exhibition-program website concept, one flat front-on landscape 16:10 screen, high resolution. Original art direction.
Primary request: Demonstrate Expressive shape/scale/color hierarchy and tactile action affordances in a cultural website, while preserving recognizable programme navigation. This is an actual visitor-facing programme interface, not a moodboard, infographic or design-method explanation.
Composition: strong asymmetric editorial grid with a slender header; large dark warm-charcoal sans-serif heading "See things differently." occupying the upper-left quarter with purposeful natural line breaks. Main area combines a large evocative art-installation photograph in a rounded arch-shaped aperture (sculptural folded scarlet fabric and cobalt architectural planes in a sunlit gallery), and an orderly three-row programme list alongside it. The curatorial photo is the hero; geometric color fields establish rhythm without extra decorative stickers. Generous butter-yellow background, vermilion active controls, warm graphite typography, pale pink secondary surfaces, disciplined confident contrast. The photograph's color/light echoes the UI without covering text.
Exact header/navigation labels: "Exhibitions", "Calendar", "Visit". Heading above list: "This week". Three programme rows: "Color in motion" with "10:00 — Gallery 1"; "Sound and space" with "13:30 — Studio"; "After hours" with "18:00 — Main hall". A selected date control says "Sat 26". Primary button says "Plan your visit" in clean dark text on a warm vermilion/coral tactile surface with an exact subtle lower lip and believable soft contact shadow. Distinct selected pill silhouette, beautifully crafted icon arrows and generous hit areas. Small footer link "View full programme". The interface has a clear path from seeing an exhibition to planning a visit.
Style: contemporary cultural art direction, expressive but precise, unusually beautiful typographic composition, realistic editorial imagery, clean sharp letterforms. Avoid generic SaaS layouts, repeated rounded-card grids, purple-gradient defaults, numbered feature blocks, starburst/emoji decorations, fake awards or logos, explanatory UI labels, device mockups, watermarks. Do not scatter the programme into an unreadable collage.
```

</details>

<details>
<summary>Material editor</summary>

```text
Use case: ui-mockup. Asset type: GitHub README showcase, exceptionally polished digital material editor web interface, one flat front-on landscape 16:10 screen, high resolution. Original interface, not a copied app.
Primary request: Show a convincing Hypermaterial and Shader-oriented art-direction concept within an actual material authoring workflow, with readable restrained controls and a visually extraordinary editable surface.
Composition: full-screen warm pearl-white studio canvas containing one large sculptural folded glass ribbon with deep cyan transmitted light, delicate rose-gold iridescence at grazing angles, believable curved thickness, sharp specular edge, clear interior distortions and luminous soft caustic on the ground. The object occupies the left two-thirds, has a graceful flowing silhouette and detailed plausible reflections, not a generic sphere or blob. Precise small control points along its silhouette suggest editable geometry. One narrow matte-white properties panel on the right, clean semantic rows and finely finished tactile sliders. Bottom-left a slim material sample strip showing only three small previews: clear glass, pale ceramic, brushed metal. Selected glass sample has an unambiguous dark outline. A compact dark toolbar at the top has restrained typography. Strong contrast between the extraordinary material and calm white editor; no all-over transparent cards.
Exact readable text: top left "Material editor"; top toolbar "Surface", "Light", "Export"; inspector title "Iridescent glass"; property rows "Transmission" value "0.92", "Roughness" value "0.08", "Thickness" value "1.20", "Iridescence" value "0.65"; bottom strip labels "Glass", "Ceramic", "Metal". A small input hint under the canvas says "Drag to rotate". Render these labels crisply without fake paragraphs. Sliders have delicate circular thumb highlights and a discernible track.
Style: sophisticated contemporary software art direction, exceptional product-render lighting, luminous optical material with realistic thickness, intentional negative space, highly accurate spacing and typography, gallery-quality composition. Avoid dark SaaS dashboards, gratuitous gradients over the whole screen, cards for every paragraph, floating meaningless spheres, labels naming design trends, watermarks, device frames, browser chrome or six-panel grids. A beautiful usable-looking editor, not merely a product photograph with text attached.
```

</details>

<details>
<summary>Identity studies</summary>

```text
Use case: logo-brand.
Asset type: premium open-source design-skill README identity exploration board, landscape 16:10, high resolution.
Primary request: create a beautifully art-directed logo specimen board for "ui-gspuer". Exact spelling u i - g s p u e r, all lowercase. A distinctive original geometric mark built from two offset folded planes with an elegant negative-space channel, compact silhouette and precise optical balance. No generic sparkle, atom, brain, magic wand, shield or infinity logo.
Composition: disciplined three-part editorial board. Top two-thirds: generous warm ivory field with one large charcoal geometric mark at left and precise custom sans-serif wordmark "ui-gspuer" next to it; generous clear space. Lower third split between a charcoal panel with a smaller ivory mark/wordmark lockup, and a quiet pale gray panel containing a larger sculptural interpretation of the SAME mark in optically clear smoked glass with a fine spectral edge. Maintain a recognizable identical silhouette across all three treatments. Flat original vector-like logo shapes in the main and reversed versions; premium physical optical rendering only in the third version. Small unobtrusive labels "Primary", "Reverse", "Material study". This is an identity specimen, no product UI or arbitrary merchandise.
Typography: exquisite compact lowercase sans serif, exact spelling, careful kerning, proportionally modest wordmark, all labels legible. Fine dividing rules, perfectly aligned margins, calm balanced composition.
Material: the glass version has slender crisp edges, controlled internal reflection, localized cyan/amber dispersion and a precise contact shadow. The main logo remains clean flat charcoal. No swollen resin, no milky blue plastic, no heavy bevel, no glowing rim, no glossy rounded app icon. No noisy photographic background, no watermark, no extra words.
```

</details>

<details>
<summary>Optical workspace components</summary>

```text
Use case: ui-mockup.
Asset type: high-end UI component specimen board for a design skill README, landscape 16:10, high resolution. One image containing multiple beautifully coordinated components, not a complete app screenshot.
Primary request: an exceptional original component family combining thin optical Liquid Glass and clear Spatial layering for an audio workspace. Visually arresting but extremely refined, with usable sharp typography. Show distinct components freely arranged on a precise asymmetric grid with ample breathing room, not all wrapped in identical cards.
Scene: warm pearl studio canvas with a single broad muted slate-teal geometric plane passing beneath the central glass toolbar, providing calm transmitted background structure. No photograph, no busy texture. Components cast delicate consistent short shadows; almost frontal view, no extreme perspective.
Layout: small header "Optical / Workspace" aligned top left. Large central horizontal clear smoked-glass transport dock with play/pause, crisp time "00:18 / 00:42" and a fine progress rail. Upper-left a slim three-tab segmented control "Listen", "Trim", "Mix" with Trim selected. Upper-right a compact frosted popover titled "Output" with two clean rows "Stereo" and "48 kHz". Lower-left a waveform selection component labeled "Selected region" and time "00:08 — 00:36", with precise trim handles. Lower-middle two contrasting primary and secondary action buttons "Export clip" and "Save". Right side two elegant labeled slider controls "Volume" and "Balance", plus one well-sized toggle labeled "Loop". Include an unobtrusive tiny two-swatch treatment strip "Clear" and "Smoke". No extra components or lorem ipsum.
Visual system: fine neutral translucent planes with restrained 14–20px equivalent curvature; real-looking background displacement only at curved edges, clear interiors, very fine localized specular highlights, thin controlled glass thickness. Flat dark graphite primary action, readable graphite labels on light surfaces and ivory labels on dark surfaces. Differing depths communicate which popover floats over which toolbar, one coherent upper-left soft light. Text and hit areas remain flat and clean.
Avoid inflated jelly/plastic, heavy bevels, continuous white glowing outlines, cyan fog, chunky toy buttons, rainbow wash, spheres, stock photos, generic KPI/dashboard cards, fake metrics, device/browser frames, watermarks. The whole board should resemble a meticulously composed premium component library editorial, not a random collage.
```

</details>

<details>
<summary>Expressive programme components</summary>

```text
Use case: ui-mockup.
Asset type: highly art-directed component specimen board for a design skill README. Landscape 16:10, high resolution. A single image showing a coordinated expressive and tactile component family, not a complete webpage.
Primary request: bold contemporary cultural-programme components with exceptional typography, intentional shape contrast and precise tactile action details. Original coherent design. A warm butter background, ink black typography, controlled vermilion, cobalt, pale lilac and pistachio accents. Rich confident color balance, no gradients or photographic wallpaper.
Composition: generous margins and an asymmetric editorial grid; components varied in scale and silhouette, carefully aligned without identical card containers. Top-left compact heading "Expressive / Programme". Main left a large but compact two-line typographic event card "Color in motion" on vermilion, with a single simple abstract cut-paper arch in cobalt and cream; small event line "Sat 26 · 10:00". Upper-middle a rounded tab group "Today", "This week", "All" with one obvious selected state. Upper-right an elegant date-picker fragment titled "September" with a single week row "24 25 26 27 28", 26 selected in dark shape. Bottom-left a substantial cobalt button "Book a visit" with precise 3px-like darker lower lip/contact shadow, alongside its visibly depressed state shown as a second smaller button. Center an admission stepper labeled "Tickets", minus, "02", plus, with clear hit areas. Right a slim volume-like preference slider labeled "Intensity", contrasting track and broad thumb. Bottom-center two compact chips "Exhibition" and "Workshop", and a legible confirmation toast "Visit saved" with a small check icon. Include two tidy toggle controls, one on and one off, without extra prose.
Typography: highly polished neo-grotesk, strong hierarchy, crisp precise readable labels, human editorial rhythm. Shape variation is tied to action/selection, not arbitrary squiggles. Restrained physical press cue only on primary actions; most surfaces flat matte print-like colors. Soft tiny shadows, no fake 3D objects.
Avoid all-over rounded cards, uniform bento dashboard, generic starbursts, sparkle icons, toy plastic, swollen gel, gratuitous stickers, noisy drop shadows, marketing claims, giant empty hero, browser/device frame, watermarks. All components must fit with elegant spacing in one complete board.
```

</details>

<details>
<summary>Material studio components</summary>

```text
Use case: ui-mockup.
Asset type: premium dark material-authoring UI component specimen board for a design-skill README, landscape 16:10, high resolution. Several coordinated components composed in one image, not a full application or dashboard.
Primary request: striking original Hypermaterial and Shader-oriented components with tactile precision, distinguished material behavior, readable controls and a restrained studio composition. Deep graphite neutral canvas, soft silver, bone-white text and selective electric chartreuse state accent. Refined iridescence belongs only to the material preview.
Composition: small header "Material / Studio" upper left. Asymmetric organized layout with meticulous spacing and coherent alignment, differing sizes, no uniform card grid. Largest element left is an elegantly curved narrow folded optical ribbon contained within a slim dark material-preview viewport; reflective liquid-metal face transitions into transparent smoky glass at the fold, precise cyan and muted rose spectral grazing highlights, physical thickness and localized reflections. A fine scrub line beneath the preview labelled "Surface study". Upper-right a concise settings cluster with readable sliders "Roughness 0.08", "Transmission 0.92", "Thickness 1.20", clean flat typography and neutral rails. Mid-right a row of three material swatches, truly different: brushed aluminum, warm matte ceramic, clear glass, exact labels "Metal", "Ceramic", "Glass", glass selected by a fine chartreuse marker. Lower-left segmented tabs "Surface", "Light", "Motion", Surface selected. Lower-middle a carefully machined metallic rotary control with fine radial ticks and clear label "Exposure", paired with a slim neutral horizontal adjustment rail. Lower-right a restrained chartreuse primary button "Apply material" and a dark secondary button "Reset". A small dark color control with a circular hue ring and hex field "#B9D7D2" fits above the actions.
Lighting/material: thin controlled specular lines, metallic anisotropic reflection in the dial, visibly diffuse ceramic swatch, optically clear glass swatch; a single generous soft studio light direction. Text on matte planes, not on shiny surfaces. The preview carries rich optical variation while all controls stay calm, precise and usable.
Avoid thick glossy plastic cards, milky blue gel, inflated pill buttons, all-over rainbow glow, excessive neon, decorative spheres, generic SaaS metrics, gratuitous graphs, six identical panels, unreadable microtext, extreme perspective, browser/device frame and watermarks. The result should feel like a beautifully curated professional creative-tool component system.
```

</details>

<details>
<summary>Identity studies: background repair</summary>

```text
Use case: precise-object-edit.
Edit this identity specimen board. Preserve the logo geometry, the exact wordmark "ui-gspuer", the three-part layout, and the excellent clear-glass mark in the lower-right panel.
Repair ONLY the backgrounds and opacity. The entire top panel must be a solid fully opaque warm ivory background with crisp charcoal logo and wordmark. The bottom-left panel must be a solid fully opaque charcoal background with crisp ivory logo and wordmark. The lower-right glass study must remain on its fully opaque pale gray studio background. Remove every ragged cutout, transparent hole, black void and pixelated halo. Make the horizontal divider perfectly clean and straight. Keep the small labels "Primary", "Reverse", "Material study" readable in the correct contrasting colors.
This is a complete editorial presentation board, NOT a transparent logo cutout. Every pixel of the finished rectangular board must be opaque, including all margins, all flat background fields and the areas surrounding the logos. Do not remove backgrounds. No added objects, no new text, no altered spelling, no watermark.
```

</details>

<details>
<summary>Optical workspace: surface and background refinement</summary>

```text
Use case: precise-object-edit.
Refine this UI component board, preserving its component inventory, readable labels, positions, and slate-teal diagonal plane. Repair the background: the entire image must be fully opaque warm pearl, including all margins and every area around controls; no transparency, cutout holes, black voids or ragged halos. This is a finished rectangular presentation board, not a transparent asset sheet.
Correct the glass craft locally. Reduce the central transport dock to a slim rounded rectangle with modest corner curvature, a fine single edge highlight and a much clearer transmitted interior. Remove the thick double rims, broad white bevel and heavy shadows. Use a flat dark pause button, simple flat transport glyphs, and remove circular raised housings on secondary icons. Flatten Export clip and Save to precise dark and pale actions with subtle corners, no pillow contours or glossy embossing. Keep the waveform selection, settings panel, labeled sliders and toggle. All glass should be thin precise optical planes; text stays crisp. Keep the small heading "Optical / Workspace". Remove incidental tiny decorative taglines. Strong calm contrast, no noisy textures, no extra shapes or words. Every background pixel fully opaque. Preserve the overall layout and all functional text.
```

</details>

<details>
<summary>Expressive programme: component and copy refinement</summary>

```text
Use case: precise-object-edit.
Polish this component specimen board. Preserve the butter canvas, vermilion event card, cobalt booking buttons, all existing functional components, exact functional labels and the overall grid. Make the whole rectangular image fully opaque.
Remove ALL incidental promotional slogans and decorative microcopy from top-right header, event card margins, calendar bottom, all footer lines and the central area. Specifically remove the central "Same city. New perspectives." headline and lilac slogan blob. In that central space place two elegantly aligned compact component examples: a search field with magnifier and text "Search events", and beneath it a clean three-row menu with "Exhibitions", "Workshops", "Talks", Workshops selected with pale lilac. Do not add any other text.
Keep the event card title "Color in motion" and "Sat 26 · 10:00"; remove the fictional venue name. The calendar fragment should show only heading "September", arrows and dates "24 25 26 27 28", 26 selected; REMOVE the weekday names because no year is specified. Keep the two booking buttons; make the lower "Pressed" example visibly depressed with almost no lower lip, rather than duplicating the raised state. Preserve ticket stepper, chips, toast, slider and toggles. Remove all tiny decorative slogans and leave clean breathing room. Perfect readable typography. No style overhaul, no new poster, no watermark.
```

</details>

<details>
<summary>Material studio: copy refinement</summary>

```text
Use case: precise-object-edit.
Refine this dark material-studio component board by removing incidental promotional and decorative microcopy only. Preserve the beautiful metal-to-glass ribbon image, all material swatches, settings, sliders, color picker, dial, action buttons, their positions, exact functional labels and values, lighting, graphite colors and entire composition. The final rectangular board is fully opaque.
Keep heading "Material / Studio"; section headings "Material Properties", "Material Presets", "Color"; property names and numbers; "Metal", "Ceramic", "Glass"; "Surface study", its scrubber and time; tabs "Surface", "Light", "Motion"; "Exposure" and dial values; "#B9D7D2"; "Apply material"; "Reset".
Remove every other decorative slogan and tiny letterspaced filler: top-right "SHAPE LIGHT MATTER TOGETHER"; all writing inside the ribbon viewport; "REAL-WORLD BEHAVIOR", "BASES FOR NEW IDEAS", "TINT THE UNSEEN"; copy below the tabs and dial; all footer taglines. Replace these only with the existing clean dark background. Do not add replacement text or objects. The outcome should be quiet, exact, and free of advertising filler. Do not change any material rendering or functional component.
```

</details>

<details>
<summary>Optical workspace: edge refinement</summary>

```text
Use case: precise-object-edit.
Preserve this entire component board, all text, positions, background, buttons, controls, spacing and fully opaque rectangular canvas. Change ONLY the optical perimeter of the large central transport surface and the upper-right Output popover.
The current central toolbar looks like a flat white outline. Give its boundary a slender, physically credible clear-glass cross-section: a narrow roughly 5-pixel-wide lens edge that locally bends and offsets the diagonal teal background where the background crosses the top and bottom rim. Use a crisp dark-light specular pairing, small bright reflection on only the upper-left curve, subdued cooler reflection on the lower-right curve, and a subtle close contact shadow below the surface. The interior remains transparent, with the underlying diagonal shape visible and just a little softened. No milky fog, continuous neon glow, thick white border, giant bevel or puffy shape. Preserve existing flat dark pause button and all icons. Give the Output popover the same thinner optical edge language, with clear readable text. Keep everything else identical. This should be precision optical glass, with visible edge refraction, not a plastic capsule and not a mere 1px CSS border. Do not add decorative slogans, labels, elements or alpha transparency.
```

</details>
