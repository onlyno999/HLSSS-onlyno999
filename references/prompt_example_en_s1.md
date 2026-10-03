# 英文提示词样例 · S1 古风世（2026-10-03 样片实测通过版，节选自项目原文）

> 来源：样片项目 `prompts_en_s1.txt` 原文（任务 2106323852287246337，质检 PASS）。
> 这是本技能「提示词铁律」的标准形态：Ref2VA 六段式、全文英文、只有 `<d>` 台词是中文、
> `non_diegetic_music: N/A`、`[Shot 1]` 无时间戳、后续 Shot 带 `At MM:SS.mmm`。
> 新项目照这个结构换人物/服装/场景/台词内容，结构与记法不许改。
> 派发前自检（剥掉 `<d>…</d>` 后中文字符数）实测 = 0。

```text
subject_definitions:
<Subject 1> is the young man in <Picture 1>, a character card whose large headshot defines his face exactly: same face shape, eyebrows, eyes, nose and lips. He wears his long black hair in a topknot with a gold crown pin, a moon-white robe with pale blue cloud embroidery, a red cord belt at the waist and black cloth boots. He is speaker (S1), a young adult male with a steady, warm, mid-low voice speaking Mandarin.
<Subject 2> is the young woman in <Picture 2>, a character card whose large headshot defines her face exactly: same face shape, eyebrows, eyes, nose and lips, with straight bangs. She wears her long black hair in a bun with a peach-blossom hairpin, a pink-white and pale-blue gradient ancient gown, a thin red string tied around her right wrist and embroidered shoes. She is speaker (S2), a young adult female with a soft, clear voice speaking Mandarin.
<Subject 3> is the ancient peach-blossom forest above a sea of clouds in <Picture 3>: pink blossom trees, drifting petals, layered mountains in cloud, and warm golden morning sidelight.
<Picture 4> is the opening keyframe anchor for [Shot 1], showing both characters standing face to face under the blossom tree.
<Picture 5> is the keyframe anchor for [Shot 2], a medium close-up of the man tying the red string onto the woman's wrist.
<Picture 6> is the keyframe anchor for [Shot 3], showing the woman fading into white light and petals while the man reaches toward her.

summary:
[reference generation + keyframe completion] The target video is a 10-second 16:9 live-action fantasy romance scene in <Subject 3>. <Subject 1> ties a red string on <Subject 2>'s wrist and speaks one short vow line; <Subject 2> answers one short line; a gust of petals and white light then takes her away as he reaches for her. <Picture 4>, <Picture 5> and <Picture 6> anchor the composition of the three shots in order.

retention_analysis:
<Subject 1> (appears in [Shot 1], [Shot 2], [Shot 3]): fully_preserved - his face, topknot with gold crown pin, moon-white robe with pale blue cloud embroidery and red cord belt are retained in every shot.
<Subject 2> (appears in [Shot 1], [Shot 2], [Shot 3]): fully_preserved - her face, bangs, bun with peach-blossom hairpin, pink-white gradient gown and the red string on her right wrist are retained in every shot.
<Subject 3> (appears in [Shot 1], [Shot 2], [Shot 3]): fully_preserved - the peach-blossom forest, sea of clouds, falling petals and golden morning light stay consistent.
<Picture 4> ([Shot 1] keyframe): fully_preserved - the opening two-shot composition under the blossom tree is followed.
<Picture 5> ([Shot 2] keyframe): fully_preserved - the red-string tying close-up composition is followed.
<Picture 6> ([Shot 3] keyframe): fully_preserved - the fading-away composition with the reaching hand is followed.

detailed_description:
The target video is a cinematic live-action fantasy romance with soft golden morning light, drifting peach petals and a gentle, wistful tone. All camera positions stay on the same side of the axis between the two characters: the man remains on the left of the frame and the woman on the right in every shot.
[Shot 1] The shot begins from <Picture 4>. A wide shot establishes <Subject 3>, the peach-blossom forest above the sea of clouds. <Subject 1>, the young man in the moon-white robe, stands in the mid-ground on the left side of the frame facing right; <Subject 2>, the young woman in the pink-white gown, stands in the mid-ground on the right side facing left. They are about one meter apart, looking at each other through falling petals, their lips naturally closed and still. The camera pushes in with small amplitude at a slow speed. Wind moves through the blossom branches and their sleeves sway lightly.
[Shot 2] At 00:03.500, the shot cuts to a medium close-up matching <Picture 5>, keeping the man on the left and the woman on the right. <Subject 1> (S1) lifts her right hand gently and ties the thin red string around her wrist, his fingertips steady on the small knot. Looking at the knot, then at her, he says in a steady, warm young male voice at a slow, quiet pace, <d>[Chinese] 等我回来娶你。</d> He presses his lips into a line, his throat moves once, and he says nothing more. <Subject 2> (S2) first lowers her eyes to the red string, pauses for half a beat with her fingers curling slightly, then raises her eyes to him and answers in a soft, clear young female voice, <d>[Chinese] 我等你，多久都等。</d> Her lips close softly after the line; her eyes glisten but no tears fall, and the camera holds on both faces with a very slow push in.
[Shot 3] At 00:07.500, the shot cuts to a deep-focus wide shot matching <Picture 6>. A sudden gust spins the petals into the air and a soft white glow gathers around <Subject 2> in the right background; her figure gradually turns translucent and fades into light and petals. <Subject 1>, in the left foreground, steps toward the right along a straight path and reaches out his hand, his fingertips touching only falling petals. Both characters keep their lips fully closed and still for the rest of the shot, with no further speech. The camera pulls back with small amplitude at a slow speed and ends on the wide view of the blossom forest and the sea of clouds, the man standing alone on the left.

overall_soundscape: Mountain wind moving through peach branches, softly falling petals, light fabric rustling and quiet breathing continue under the two short dialogue lines.

non_diegetic_music: N/A
negative prompts: music, background music, bgm, soundtrack, score, melody, tune, instrumental, musical instruments, rhythm, singing, song, voiceover, narration, monologue, extra lines, improvised speech, humming, phantom voices, face morphing, extra fingers, extra limbs, gibberish text, hat, cap, subtitles, watermark, logo
```

## 换世改写要点（S2/S3 同法）
- `<Subject 1>/<Subject 2>` 只换本世服装发型（民国短发侧分中山装/旗袍盘发；婚礼西装/婚纱头纱），脸定义句与 (S1)/(S2) 声线句**逐字沿用**。
- `<Subject 3>` 换本世场景（民国雨夜老街/现代婚礼礼堂），`<Picture 4/5/6>` 换本段三锚的剧情构图描述。
- `summary` 开头方括号任务类型按官方选（如 `[reference generation + keyframe completion]`，S2/S3 另含尾帧续接关系时按官方标签组合）。
- 台词换本世 2 句（默认模板见 SKILL.md「对白定版」）；其余结构、negative 词表、N/A 一律不动。
