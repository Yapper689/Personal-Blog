---
title: Gushing over WuWa graphics
published: 2024-07-28
description: ''
image: 'cover-images/changli.jpg'
tags: [Game,Tech]
category: 'Appreciation'
draft: false 
---
The Anime Style Game (ASG) genre has witnessed many new titles recently, with each new one looking more stylized than the last. Among these, Wuthering Waves stands out as a quintessential example of the successful blend of 3D and 2D elements within the Anime, Comic, and Games (ACG) aesthetic. This game exemplifies a level of visual sophistication that has rarely been seen before in the genre, setting a new standard for how anime-inspired games can look.

Proprietary Engine and Unity Engine has been the go to for these types of games for its ease of use. However, a significant shift has occurred in recent years, with an increasing number of high-profile titles opting for the Unreal Engine to achieve breathtaking visuals and immersive environments.

Games like Guilty Gear Strive, Snowbreak, and the upcoming Project Mugen, Azure Promilia (and Duel Night Abyss?) have all embraced Unreal Engine, and the results are nothing short of stunning. Unreal Engine's advanced rendering capabilities and graphical prowess have enabled these titles to achieve a level of detail and beauty that sets them apart from their peers, making them appear somewhat dated by comparison.

<iframe width="100%" height="522" src="https://www.youtube.com/embed/vq3ui-j-gZU" title="Genshin Impact vs Wuthering Waves Ultra Settings : Graphics &amp; Physics Comparison" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Wuthering Waves serves as a prime example of how Unreal Engine can be harnessed to create a visually striking game. The game's graphics are a testament to the engine's ability to handle complex visual effects and high-fidelity textures with ease. This results in a game that not only looks incredibly beautiful but also maintains a high level of performance (sorta) and fluidity. The seamless integration of 3D and 2D elements in Wuthering Waves demonstrates the engine's versatility and the developers' adept use of its features to craft a captivating visual experience.

Recently released Zenless Zone Zero, while undeniably stylish, still falls short when compared to the visual impact of Wuthering Waves. Despite ZZZ's distinctive aesthetic, it struggles to match the level of graphical fidelity and overall polish achieved by Wuthering Waves. This disparity highlights the advantages of using a powerful engine like Unreal Engine, which provides superior graphics capabilities out of the box and reduces the amount of effort required to achieve high-quality visuals.

<img src="https://i.pinimg.com/736x/36/19/17/361917b7b4a30db3a97f3d6fe2b4a8e1.jpg" width="100%" height="522">

# Why Unreal Engine?

[Interview Recap](https://www.unrealengine.com/en-US/developer-interviews/exploring-the-post-apocalyptic-charm-of-asg-open-worlds-in-wuthering-waves)

In developing the game, the creative team has set out to create a distinctive artistic style that stands out in the market. The game emphasizes a richly developed world with a notable contrast between scenes and an innovative use of complementary colors. This approach extends to character portrayal, where the team employs advanced animation cinematography techniques. By utilizing sophisticated color grading strategies, they achieve a strong filter effect that diverges from the conventional flat animation style often seen in similar games.

<img src="https://cdn2.unrealengine.com/wuthering-waves-img-2-1920x1080-fbc14e3e21d8.jpg?resize=1&w=1000" width="100%" height="522">

Integrating 2D characters into a 3D environment presents unique challenges, particularly concerning time of day (TOD) and post-processing lighting. To address these, the team has harnessed Unreal Engine's curve tools to accurately simulate natural daily changes in character brightness. This ensures that characters blend seamlessly with the 3D environment's lighting, maintaining visual consistency across the game. The team also employs a measured approach to the engine's physical features, using limited sampling to preserve the "hand-drawn" aesthetic. Additionally, an independent character lighting pipeline has been established, allowing for swift environmental lighting adjustments through presets and automated tools. This setup has become integral to their character and skill design workflows.

The choice of deferred shading over the often preferred forward shading was driven by the need to deliver high visual quality on mobile devices. Deferred shading facilitates the use of advanced techniques like Screen Space Reflections (SSR) and Ground Truth Ambient Occlusion (GTAO), which enhance rendering efficiency and streamline the pipeline. In the context of an open-world game where content is continuously updated, deferred rendering helps manage the complexities and simplify the development process, reduces maintenance costs, and provides consistency across platforms. Furthermore, advancements in mobile hardware have made one-pass deferred technology viable, cutting down read/write bandwidth and maintaining a steady 60? frames per second rate, which is crucial for optimizing performance and managing power consumption.

Despite its advantages, implementing deferred shading introduced technical challenges. Certain platforms, such as the Mali platform, restricts on-chip cache size and imposed performance overheads. To overcome these hurdles, the team made adjustments to their effects implementation. Integrating rendering effects like SSR and GTAO without disrupting the deferred shading workflow involved using depth and scene color data from previous frames, re-projection for reflection mapping, and applying denoising techniques to enhance SSR quality. Testing indicated that most mobile devices could handle SSR at medium quality and GTAO at high settings with minimal performance impact, ensuring that "Wuthering Waves" delivers both high visual fidelity and smooth gameplay on a range of devices.

# Goated ACG style

A significant aspect of achieving the ACG style involves the use of gradients. The team has focused on integrating gradients into characters' base colors and mask textures, a process that has evolved substantially since the game's first closed beta. The engine’s lighting capabilities, combined with fake volume fog and post-materials, are used to create the desired gradient effects. Custom color grading, often implemented through Look-Up Tables (LUTs), is also utilized to enhance the visual presentation. Each scene is meticulously designed with stable underlying lighting to maintain a consistent lighting baseline, which helps evoke the intended emotional responses from players during their exploration and narrative experiences.

They have also conducted extreme test samples for color calibration as part of their preliminary research to fine-tune the color effects. This rigorous approach ensures that the in-game visuals are both striking and consistent with the intended anime style.

The internal lighting workflow for cutscenes, such as the character PV for Danjin, is another example of how the game’s visual style is maintained. The lighting artists have precise control over light and shadow dynamics through custom lighting components, which allows them to achieve the desired visual effects.

<iframe width="100%" height="452" src="https://www.youtube.com/embed/3bwJOl-ChME" title="Wuthering Waves | Resonator Showcase | Danjin — A WAYFARER&#39;S ESCAPADE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

To meet the visual direction needs of the performance team, the developers utilize UE4's powerful Sequencer system. This tool enables detailed control over visual elements, including keyframe adjustments for various effects. For instance, during the activation effect of marks in characters' ultimate abilities, the shake intensity and frequency can be finely tuned to align with camera requirements, ensuring that the visual impact is both dramatic and coherent.

<video autoplay muted loop> <source src="https://cdn2.unrealengine.com/wuthering-waves-video3-2208ad0d58fb.mp4" type="video/mp4"> Your browser does not support the video tag. </video>

<img src="https://preview.redd.it/jinshis-animations-really-just-hit-different-v0-tcrkciqumt9d1.jpeg?width=1080&crop=smart&auto=webp&s=283d8e1f682277f2d66179e7a3c66388d7aeaa48" width="100%" height="522">

Portraying character movements and expressions presented several challenges that required innovative solutions. Initially, the team relied on skeletal techniques for character expressions, but this method proved difficult for accurately and quickly replicating authentic animation expressions. To address this, the team transitioned to a blendshape-based approach. By collecting and categorizing a diverse range of expressions, they created a comprehensive library that significantly accelerated production. This shift allowed for more nuanced and expressive character animations, facilitated through their Digital Content Creation (DCC) toolchain.

<img src="https://cdn2.unrealengine.com/wuthering-waves-img-6-1920x1080-4e425cf420f9.png?resize=1&w=1288" width="100%" height="522">

Another challenge involved rendering detailed facial expression shadows. Conventional solutions were insufficient for the intricate lighting required to capture the subtleties of facial expressions during performances. The team enhanced the facial lighting setup to create specialized shadow effects tailored to the specific needs of each performance. This improvement allowed for more accurate representation of vertical and emotional light sources, which was crucial for conveying the intended emotional impact.

Character rigging, particularly in complex and dynamic areas like joints, also posed difficulties. To address these issues, the team adopted Radial Basis Function (RBF) technology. This technology enabled precise modeling of these complex parts, which was quickly validated and integrated into the production process. The use of RBF technology improved the accuracy and fluidity of character movements, enhancing the overall visual quality of the game.

# Gameplay

<iframe width="100%" height="452" src="https://www.youtube.com/embed/1QTrMr57vps" title="Changli and Jinhsi Gameplay" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# Environment

The environment design blends modern, sci-fi, and traditional Chinese architectural elements (typical). A post-apocalyptic world undergoing reconstruction. Nothing much to say here.

The weather system though, incorporates several unique elements beyond the standard day/night and weather changes. Instead of using Unreal Engine 4’s physical atmosphere system, the team opted for a stylized day/night lighting system. This choice allows for real-time, accurate sky color adjustments that align with the game’s artistic style without relying on pre-computation. The skybox rendering process was simplified to avoid volumetric clouds, opting instead for a streamlined 2D to 3D approach. This method enables diverse sky appearances with colors and depth that change dynamically with the time of day. To compensate for the lack of real-time volumetric clouds, they included animations of clouds forming and dispersing.

# Upgrades to UE5

Lumen, UE5's dynamic Global Illumination (GI) solution. Given the open-world nature of "Wuthering Waves," with its varied terrains and dynamic weather and lighting conditions, Lumen’s real-time GI capabilities would significantly enhance environmental realism and player immersion. The current baked lighting often falls short in dynamic scenarios, and Lumen’s advanced GI functionality would address this limitation effectively.

Niagara system, particularly GPU particle baking. The limitations of mobile hardware, including computation speed, power consumption, and compatibility, currently restrict the ability to support large-scale, visually impressive particle effects. Niagara’s improved performance and functionality in UE5 would enable the creation of more engaging and visually stunning particle effects, enhancing the overall combat experience.

Optimizing multi-threading across game, render, and Render Hardware Interface (RHI) processes. For a fast-paced action game like "Wuthering Waves," maintaining a smooth frame rate is crucial. Improved multi-threading would enhance frame rate stability, leading to smoother visuals and gameplay.

# In Conclusion

People making games in unreal engine are just built different. They also probably look like this:

<img src="https://i.pinimg.com/736x/2f/ce/3b/2fce3b625734471e42c941e27bb1786a.jpg" width="100%" height="522">
