# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一起。

生成时必须把 `three-view.png` 作为图像参考输入，确保 daidai 的角色一致性。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Pure white background. Lots of empty white space. Sparse red/orange/blue handwritten Chinese annotations. Clean absurd product-sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

CRITICAL: Two-layer art style.
1. The character "daidai" must be FULL COLOR hand-drawn: a tall thin young male programmer, ~7.5 head-body ratio, messy black short hair with bangs, large brown eyes with a calm serious expression, straight black eyebrows, small closed mouth. He wears a blue-gray-purple vertical striped loose button-up shirt (open collar over a black crew-neck tee, sleeves rolled to mid-forearm), a thin black cord choker necklace with a tiny irregular turquoise stone pendant, a thin red bracelet on his right wrist, dark charcoal wide-leg trousers, black round-toe leather shoes. For work scenes, he wears a black lanyard with an ID badge (black frame, white card, faint blurry handwritten "daidai" on the card). The character has soft hand-drawn watercolor-like coloring, clean outlines, low-saturation flat colors.
2. EVERYTHING EXCEPT the character — all machines, objects, props, paper, scenery — must be PURE BLACK-AND-WHITE PENCIL LINE ART: only black hand-drawn lines and light pencil hatching shadows. ABSOLUTELY NO color fills, no gray blocks, no beige fills, no colored fills on any prop. The props must look like a simple pencil sketch on white paper.

Theme:
{正文配图主题}

Structure type:
{结构类型：Workflow / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画分镜}

Core idea:
{这张图要表达的核心意思}

Composition:
{具体画面：daidai 在哪里、正在做什么、主要物件是什么、信息如何流动}

Suggested elements:
{元素1} / {元素2} / {元素3} / {元素4}

Chinese handwritten labels:
{标注词1} / {标注词2} / {标注词3} / {标注词4} / {可选标注词5}

Color use:
Character daidai is full color as described above. All props are pure black line art only. Orange for main flow/path/arrows. Red only for key warnings/problems/results (also matches the red bracelet). Blue only for secondary notes or system state (also matches the turquoise pendant).

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten Chinese labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not color any props or machines. Do not make daidai black-and-white — he must be full color. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## 图像编辑提示

去掉左上角标题：

```text
Edit the provided image. Remove only the handwritten title "{要删除的文字}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

道具被误填色：

```text
Edit the provided image. Keep the colored character daidai exactly as is. Remove ALL color fills from every machine, object, prop, and paper in the scene — convert them to pure black-and-white pencil line art with only hand-drawn black lines and light pencil hatching. No gray blocks, no beige fills, no colored fills on any prop. Keep the red/orange/blue handwritten Chinese annotations unchanged. Keep the white background unchanged.
```

增强荒诞感：

```text
Regenerate this illustration with the same core meaning and simple layout, but make daidai more central to the conceptual action. daidai should be doing the strange work that explains the idea, not standing beside the diagram. Keep daidai full color, keep props as pure black-and-white line art, keep it clean, sparse, and not cute.
```
