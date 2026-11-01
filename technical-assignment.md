# Technical assignment: Nikita's Tower

The website presents your résumé as a **single red-brick skyscraper, with your introduction on a rooftop billboard and résumé sections on posters attached to its walls**. The surrounding interface is quiet and editorial: soft pink neutrals, deep navy typography, and a compact navigation bar.

### Overall composition

The page has three main horizontal areas:

1. A slim header with your name and professional role.
2. A centered toolbar containing navigation, poster arrows, and weather controls.
3. A large rectangular 3D scene occupying most of the page.

The background is a pale rose-beige. Thin borders, restrained spacing, and mostly square buttons give the interface a slightly vintage architectural feel. In dark mode the page switches to deep navy with peach accents.

There are no photographs, project thumbnails, or conventional résumé cards. The building is the main visual and the carrier of information. Below the scene, a plain-text version of the whole résumé repeats the content for readers and for browsers without WebGL.

### Header

At the upper left, **"Nikita."** appears in a bold serif typeface (DM Serif Display). The letters are deep navy, with a small wine-red period.

At the upper right, two lines of small uppercase text read:

> BACKEND DEVELOPER
> ML ENGINEER

The role label uses widely spaced, monospaced lettering (IBM Plex Mono). A thin horizontal rule separates the header from the navigation area.

### Unified control bar

A rounded rectangular container sits beneath the header. It has a near-white pink fill and a fine rose border.

Inside it, the controls appear in three groups:

| Group | Visible controls | Appearance |
| --- | --- | --- |
| Résumé sections | Profile, Backend, ML, Experience, Contact | Text buttons; the active section is filled navy |
| Up/down | Arrows with a counter (for example 2/3) | Switch between the posters on the current side of the building, in a loop. Disabled when a side has only one poster |
| Weather | Sun, umbrella, snowflake, pause | Compact square icon buttons; sun (sunrise) is selected by default; the selected button has a pale pink background |

Thin vertical dividers separate the groups.

Below the toolbar, a small caption on the left names the current view, for example **"01 / PROFILE · SOUTH FAÇADE · ROOFTOP"** or **"04 / EXPERIENCE · WEST FAÇADE · PROJECTS"**. On the right, another caption reads **"SECTIONS GUIDE YOUR VIEW."** Both use tiny uppercase monospaced text.

### The 3D scene

The scene fills almost the entire available width beneath the controls. Its background is a sunrise sky: dusky blue near the top, through lavender and pink, to a warm gold glow at the horizon, with a soft sun disc low on the left.

The camera is always close up on the building. It looks straight at the wall (square to it and centered) and does not move with the mouse. Moving between views flies the camera around the tower.

Behind the tower stands a hazy city of lower buildings in dusty blue, rose, and sand tones. They fade into the haze with distance. A few soft clouds drift slowly.

Weather changes the mood:

- **Sun (default):** sunrise sky, low warm light, swallows in flight.
- **Snow:** small white particles of different sizes fall in front of the building, giving depth. The sky is a cooler dusk.
- **Rain:** thin streaks fall in front of the building under a darker, bluer sky.
- **Pause:** freezes particles and swallows.

### Swallows

In sunrise mode, a formation of three or four pixel-art swallows (8-frame wing-flap sprite, navy silhouette) enters from the upper left. They dive steeply like aircraft, with wings tucked in the steep part, pull out, and leave to the right. They fly behind the billboard and the tower. Each bird leaves a thin, fading white contrail, like an airplane trail. A new pass starts every 6–12 seconds.

### Rooftop billboard

The billboard is the dominant element on the first view, positioned near the horizontal center above the roof.

It is a wide near-white sign with:

- A thick navy outer frame.
- A thin inset border.
- Large navy serif lettering for your name.
- Bold uppercase lettering for your professional role.
- A smaller, centered two-line summary.

Its text reads:

> **NIKITA**
> **BACKEND DEVELOPER**
> **& ML ENGINEER**
>
> Building services, data pipelines
> and production ML systems.

The sign is mounted on narrow supports above the highest roof structure. It projects beyond the width of that small rooftop structure. The lettering is crisp, and your name occupies about 60% of the sign's width.

### Building architecture

The tower has a stylized, simplified New York masonry appearance.

**Materials and colors:** The walls use muted wine-red brick with lighter mortar lines in fine courses. Roof caps, window surrounds, and projecting ledges use pale rose-sand stone. Window glass uses navy and teal, with a few warm peach lit panes.

**Roof silhouette:** Several rectangular volumes step inward as they rise. Broad, flat stone cornices cap each level, creating a tiered silhouette beneath the billboard.

**Upper façade:** Two rows of four small square windows occupy the central upper wall. Each window has a thick light-colored surround and a navy or teal interior.

**Outer window columns:** Narrow, taller windows run down the edges of the façade. These have divided panes, blue-teal glazing with a peach tint at the top, and projecting stone sills.

**Floor divisions:** Thick horizontal stone bands cross the façade every floor. Their projections, together with the visible roof surfaces, establish the building's depth.

**Street level:** The south façade ends in a stone entrance with a navy door. The Contact poster hangs just above it.

Lighting is low and warm, coming from the sun's side. It rakes across each wall, so one edge of the façade catches the glow and the other falls into cool shadow.

### How the résumé is represented

The rooftop billboard serves as your introduction. Each section button flies the camera to one side of the building. A side holds one or more posters stacked down the wall, and the up/down arrows move through them in a loop.

| Section | Side of the tower | Posters, top to bottom |
| --- | --- | --- |
| Profile | South | Rooftop billboard, About, Toolbox |
| Backend | East | Services, Systems |
| ML | North | Production ML, LLM agents |
| Experience | West | Employment, Projects, Automation |
| Contact | South, street level | Contact |

Each poster is a framed sheet with a small numbered tag, a large serif title, a one-line summary, and grouped bullet lists. Text is scaled so it fills the poster. The full poster text is in `resume.md`.

The visible hierarchy is:

**Your name in the page header → navigation controls → rooftop introduction → posters on the current wall → plain-text résumé below the scene.**

The overall impression is a warm, sunlit architectural résumé: a substantial brick tower presented close up at dawn, with a large personal billboard, restrained interface controls, and a city waking up behind it.

---

## What changed from the original description

- Palette: warm neutrals and dark green became pale pink, navy, wine red, teal, and peach.
- Weather: snow was the default; sunrise is now the default, with sun, rain, and snow selectable.
- Camera: no longer off-axis; straight on and centered, with no mouse movement.
- Navigation: up/down arrows now loop through several posters on one side, with a counter and a longer caption. Each section has its own side.
- Added: city backdrop, sunrise sky and sun, clouds, swallow formation with contrails, street-level entrance, plain-text résumé section.
- Removed: the note that the description matched one screenshot, and the stretched, soft billboard lettering.
