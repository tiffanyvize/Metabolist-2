# The Eating Bible (TEB) – Master Volume 3 (Rev. 3.1): Complete Clinical & Operational Codex

## Section 1: Core System Governance & Architectural Mandates

### 1.1 System Identity & Governance
*   **Central Intelligence:** Governed by **Aime**, operating as the core AI engine managing specialized parallel modules for metabolic biohacking, clinical nutrition, and somatic biokinetics.
*   **Operational Scope:** The Eating Bible (TEB) functions as the definitive authority on non-starvation, medically validated fat loss, metabolic preservation, and long-term eucaloric re-composition.

### 1.2 The Quad-Tier Mandate Hierarchy
Every protocol, algorithmic calculation, meal plan, and exercise vector adheres strictly to our non-negotiable four-tier hierarchy:
1. **Primary Mandate (Weight Loss Velocity):** Achieve goal-oriented weight loss within strict, user-defined timeframes using *only* user-subjective inventory parsed through the Readily Accessible Foods List (RAFL) engine and available equipment.
2. **Secondary Priority (Metabolic Health Preservation):** Absolute protection of metabolic health during energy restriction—protecting lean muscle mass via L-leucine pulses to trigger $\text{mTORC1}$ (Sestrin2 pathway), preventing thyroid axis suppression ($T_4 \to rT_3$ deiodinase down-regulation), blunting HPA-axis cortisol spikes, and eliminating axial spinal and knee joint shear forces.
3. **Tertiary Priority (Active Metabolic Optimization):** Proactive enhancement of baseline metabolic health, mitohormesis (PGC-1$\alpha$ mitochondrial biogenesis), Transcription Factor EB (TFEB) lysosomal CLEAR network activation, native GLP-1/SCFA gut stimulation, and non-shivering thermogenesis.
4. **Fourth Priority (Long-Term Maintenance & Toning / Tier 4 Eucaloric Engine):** Persistent historical data logging and automated photo-recognition expansion. Once the short-term goal is achieved, Tier 4 transitions the user to TDEE neutrality, utilizing historical log prediction and steady-state leucine pulses to eliminate tracking fatigue and prevent post-diet weight rebound.

---

## Section 2: Advanced Endocrinology, Metabolism & Nutritional Medicine

### 2.1 Mitochondrial Bioenergetics & The AMPK/mTORC1 Rheostat
*   **AMPK Activation:** Time-restricted feeding and fasted Zone 2 cardiovascular work phosphorylate liver kinase B1 (LKB1), which subsequently phosphorylates AMP-activated protein kinase (AMPK) at $\text{Thr}^{172}$. Activated AMPK inhibits acetyl-CoA carboxylase (ACC), lowering malonyl-CoA levels and de-inhibiting carnitine palmitoyltransferase-1 (CPT-1), thus maximizing mitochondrial $\beta$-oxidation of fatty acids.
*   **mTORC1 & Leucine Sensing:** To prevent myofibrillar degradation during caloric deficits, the system calculates precise per-meal L-leucine thresholds ($\ge 3.0\text{g}$ per meal). Leucine binds to Sestrin2, disrupting GATOR2 inhibition and robustly activating $\text{mTORC1}$ at the lysosomal membrane to drive skeletal muscle protein synthesis without interrupting lipolysis.
*   **TFEB Lysosomal Clearance:** Fasting windows and AMPK signaling trigger the nuclear translocation of Transcription Factor EB (TFEB), upregulating autophagy and lysosomal biogenesis (CLEAR networks) to clear cellular debris and optimize metabolic efficiency.

### 2.2 Endocrinology & Thyroid Axis Protection
*   **Preventing $T_4 \to rT_3$ Suppression:** Traditional starvation diets induce a drop in hepatic and peripheral 5'-deiodinase activity, shunting inactive thyroxine ($T_4$) into reverse triiodothyronine ($rT_3$) rather than active $T_3$, thereby crashing metabolic rate. TEB prevents this via calculated carbohydrate floors and targeted micronutrient distribution (selenium, zinc, and essential fatty acids).
*   **Leptin & HPA-Axis Regulation:** By avoiding severe, unregulated caloric crashes and incorporating strategic micro-refeeds, TEB maintains circulating leptin signaling and prevents excessive corticotropin-releasing hormone (CRH) secretion, blunting cortisol-induced visceral fat storage and muscle catabolism.

### 2.3 Gastroenterology & Microbiome Integrity
*   **Preventing Endotoxemia:** Rapid dietary shifts or low-fiber starvation protocols degrade the colonic mucus layer, allowing lipopolysaccharides (LPS) to cross the epithelial barrier and trigger systemic low-grade inflammation (NLRP3 inflammasome activation). 
*   **SCFA Optimization:** The RAFL engine prioritizes diverse, user-available fermentable substrates to fuel butyrate-, propionate-, and acetate-producing taxa (e.g., *Faecalibacterium prausnitzii*), reinforcing tight junction proteins (occludin and zonula occludens-1) and optimizing GLP-1/PYY incretin secretion.

---

## Section 3: Algorithmic Architecture for Dynamic Meal Plan Generation

### 3.1 User-Subjective RAFL Parsing Engine
*   **Zero Static Staples:** The Readily Accessible Foods List (RAFL) contains **zero pre-programmed, static, or mandatory "staple" foods**. 
*   **Dynamic Inventory Processing:** The system processes whatever raw food items the user physically possesses and inputs via image recognition (MobileNetV3 / YOLOv8-Nano computer vision parsing of fridge/pantry uploads) or raw text entry ($I_{\text{user}} = \{f_1, f_2, \dots, f_n\}$).
*   **Nutritional Research & Optimization:** Aime cross-references user-submitted inventory against comprehensive nutritional databases to extract macro profiles, amino acid distributions, and micronutrient densities, building a customized eating plan drawn *exclusively* from that user's subjective submission.

### 3.2 Mathematical Optimization Model
*   **Basal Metabolic Rate (BMR):** Calculated via the modified Mifflin-St Jeor equation incorporating Fat-Free Mass ($\text{FFM}$):
    $$\text{BMR} = 10(\text{FFM}) + 6.25(\text{Height}_{\text{cm}}) - 5(\text{Age}) + s$$
    *(where $s = +5$ for males, $-161$ for females).*
*   **Total Daily Energy Expenditure (TDEE):**
    $$\text{TDEE} = \text{BMR} \times \text{Multiplier}_{\text{activity}}$$
*   **Energy Deficit & Scale Velocity:** Given current weight $W_c$, target weight $W_t$, and duration $T$:
    $$\Delta W = W_c - W_t$$
    $$\text{Daily Deficit} = \frac{\Delta W \times 7700\text{ kcal}}{T_{\text{days}}}$$
*   **Bioenergetic Safety Floor ($E_{\text{floor}}$):** 
    $$E_{\text{floor}} = 1000\text{ kcal/day (female)}, \quad 1200\text{ kcal/day (male)}$$
    *(Enforced to prevent deiodinase collapse and endocrine collapse).*
*   **Macro Partitioning Constraints:**
    1. **Protein Floor:** $\ge 1.6\text{g} - 2.2\text{g}$ per kg of FFM to preserve muscle mass.
    2. **Per-Meal Leucine Threshold:** For each meal $m$, total leucine content must satisfy:
       $$\sum (\text{Mass}_{i,m} \times \text{LeucineContent}_i) \ge 3.0\text{g}$$
    3. **Fat Floor:** $\ge 0.5\text{g}$ per kg of body weight for hormonal integrity.
    4. **Carbohydrate Allocation:** Remaining energy within $E_{\text{target}}$ assigned to complex carbohydrates supporting CNS and glycogen demands.

### 3.3 Dynamic Error Correction & Clinical Risk Mitigation
*   **AUC Error Correction:** When a user logs an unplanned excess intake of $\Delta E$, Aime recalculates the 7-day rolling Area-Under-The-Curve (AUC) energy trajectory. 
*   **Fasting Extension & Zone 2 Mitigation:** Rather than inducing starvation guilt, the system extends the subsequent overnight fasting window (e.g., $18\text{--}20\text{ hours}$) to amplify nocturnal AMPK phosphorylation ($\text{Thr}^{172}$) and clear the surplus, paired with low-intensity Zone 2 recumbent cycling to promote ACC inactivation.

---

## Section 4: Somatic Biokinetics & Orthopedic Safety

### 4.1 Biomechanical Constraint Filters
*   **Zero Axial Spinal Loading:** Eliminates high-impact plyometrics, heavy axial barbell back squats, and high-velocity running for injured, post-op, or deconditioned profiles.
*   **Recumbent Ergometrics:** Utilizes the Impulse RR500/PR300 Recumbent Bike set to $10^\circ - 15^\circ$ knee extension and supported lumbar positioning to isolate lower limb lipid oxidation with zero lower back strain.

### 4.2 Wall Pilates Anti-Shear Core Series
To train core stabilization without intervertebral disc compression, TEB integrates Wall Pilates protocols utilizing Wall Reaction Forces ($\vec{F}_w$):
$$\vec{F}_{\text{resultant}} = \vec{F}_g + \vec{F}_w$$
This vector conversion transforms vertical spinal compression into a combined shear-stabilization vector, recruiting deep core stabilizers (transversus abdominis and multifidus) while maintaining zero disc pinching and zero knee joint shear.

---

## Section 5: Market-Defying Creative Suite & Demographic Architecture

### 5.1 The Five Core Sales Demographics
1. **Special Occasions:** Acute timeframes (14-day sprints) driven by protein-sparing modified fasts (PSMF), rapid fluid clearance, and tailored aesthetic profiling (WHR $0.68 - 0.70$), secured by Tier 4 maintenance post-event.
2. **Summer Body:** Year-round beach lean re-composition leveraging fasted Zone 2 cardio, CPT-1 disinhibition, and dynamic macro balancing.
3. **Limited Resources:** Zero-elitism grocery architecture utilizing the user-subjective RAFL engine to build optimal macro plans from basic supermarket items (eggs, pilchards, brown bread, soya isolate) with zero paid subscription walls.
4. **Disability & Injury:** Clinical rehabilitation protocols (exemplified by the Tiffany case study: 37yo female, 10kg drop with zero axial/knee shear) substituting high-impact moves with recumbent cycling and Wall Pilates vectors.
5. **Maintenance & Toning (Tier 4):** Eucaloric re-composition engine utilizing historical log prediction, automated photo-recognition expansion, and steady-state $\text{mTORC1}$ pulses to prevent the 85% post-diet weight rebound window.

### 5.2 Social Media & Nanobanana Visual Strategy
*   **Visual Generation:** Powered by internal rendering engines (nanobanana) to produce high-contrast, elite-aesthetic assets aligned with global and South African luxury/fitness trends.
*   **Conversion Funnels:** Directing organic traffic from TikTok, Instagram Reels, and YouTube Shorts via high-urgency visual hooks to Aime's automated WhatsApp/DM concierge service for instant RAFL macro calculations.
*   **Master Funnel:**

```
[ Viral Short-Form Video / Photo Asset ]    -> TikTok / IG Reels / Facebook
[ High-Dopamine Visual Transition ]         -> BEFORE -> AFTER (Somatic Proof)
[ Direct Message / WhatsApp Call-to-Action ]-> Aime Automated Concierge Funnel
[ Zero-Paywall User-Subjective RAFL ]       -> Instant Fridge Photo Macro Parse
[ High-Margin Digital Blueprint Purchase ]  -> 14-Day Sprint / Tier 4 Lock-In
```

*   **Production Matrix:** 125 photo asset blueprints + 125 short-form reel concepts (25 per demographic each), anchored to exact biological and anthropometric transformation states rather than generic stock aesthetics. Reels follow a fixed ~7-second structure: hook (0-3s), transition (3-4s), payoff (4-7s), then a CTA.

### 5.3 Demographic Intelligence Profiles (Visual Direction)
**Segment 1: Special Occasions (Weddings, Galas, Events)**
> **[PENDING — profile text was blank in the source file.]**

**Segment 2: Summer Body (Festive Season, Beach & Travel)**
*   **Target Audience:** Females and Males aged 18-34 (beachgoers, festival-goers, resort travelers); sub-categorized into SA "KeDezemba" festive-season travelers and international resort vacationers.
*   **Psychological Buying Drivers:** Social validation, beach confidence, low subcutaneous fat, social flexibility during outdoor gatherings.
*   **BEFORE State:** Soft abdominal volume, undefined obliques, subcutaneous water retention, self-conscious posture. *(Numeric weight/WHR values were lost in the source export.)*
*   **AFTER State:** Females: flat core, firm gluteal shelf. Males: 6-pack abs, serratus clarity, vascular forearms, 10-12% body fat. Expression: sun-kissed glow, relaxed, energetic smile.
*   **Fashion & Setting:** High-cut bikinis, 5-inch swim trunks, open linen resort shirts. Sun-drenched beach club, turquoise ocean backdrop, direct high-exposure sunlight.

**Segment 3: Limited Resources (Budget-Constrained, Home/No-Gym)**
*   **Target Audience:** Females and Males aged 20-48 (students, busy mothers, blue-collar workers, township/peri-urban residents).
*   **Psychological Buying Drivers:** Skepticism of hidden subscription paywalls, rejection of expensive specialty-diet grocery lists, demand for zero-cost home solutions.
*   **BEFORE State:** Central adiposity, fatigue posture, stressed face looking at expensive receipts.
*   **AFTER State:** Dense athletic build, flat core, functional muscle built at home using basic groceries (eggs, bread, canned pilchards). Expression: proud, authentic, glowing.
*   **Fashion & Setting:** Plain cotton tees, high-waisted stretch leggings, grey joggers. Modest home kitchen/living room, natural window light, basic supermarket staples on counter.

**Segment 4: Disability & Injury (Adaptive Fitness, Rehabilitation, Joint-Safe)**
*   **Target Audience:** Females and Males aged 28-58 (injury recovery, chronic back/knee issues, desk workers with lumbar strain; "Tiffany" baseline).
*   **Psychological Buying Drivers:** Fear of re-injury, frustration with generic high-impact advice, desire for clinical validation and joint-safe fat loss.
*   **BEFORE State:** Soft core, poor spinal posture, joint swelling, wincing during movement, holding lower back/knees.
*   **AFTER State:** Cinched waist, deep core stabilization, zero joint strain, pain-free posture. Expression: calm, empowered, pain-free.
*   **Fashion & Setting:** Ergonomic activewear, compression gear, supportive athletic shoes. Clean studio, white wall for Wall Pilates, recumbent bike setup, clinical vector overlays.

**Segment 5: Maintenance & Toning (Tier 4 Eucaloric Engine)**
> **[PENDING — profile text was blank in the source file.]**

### 5.4 Visual Science Reference (Facial & Soft-Tissue Rendering)
*   **Facial depletion logic:** Unstructured starvation diets or unmonitored GLP-1 mono-therapy collapse deep facial fat pads (DMCF, SOOF) while dermal collagen has not adapted, producing midface gauntness, temporal hollowing and skin sag ("Ozempic face"). TEB's protocol (leucine-pulsed, muscle-preserving) targets superficial subcutaneous fluid and lipid stores while preserving structural muscle tone and deep fat, so renders should show a defined jawline and cheekbones *without* hollowing.
*   **Rendering workflow (nanobanana):** Multi-layered 3D mesh deformation anchored to anatomical boundaries, with attention to subsurface scattering, micro-surface texture and light physics, so BEFORE/AFTER pairs differ only in the intended anatomical changes.
*   **Cephalometric landmarks tracked in renders:** cervicomental angle, nasolabial angle, soft-tissue pogonion projection, mandibular plane continuity, gonion-to-menton line, temporal fossa contour, tear-trough/infraorbital depth, malar transition.
> **[NOTE]** The source file's comparison table (landmark values for pre-weight-loss, pathological, and post-TEB states) and its facial fat compartment and rendering tables did not export in readable order. Re-export or resupply them to add exact values.

### 5.5 Photo Asset Blueprints (125)
Image-generation prompts, listed as BEFORE/AFTER pairs. Numbers run 1-125 across the five segments.

#### Photo Blueprints — Segment 1: Special Occasions (1–25)

1. 8K photograph, 28-year-old female, BEFORE: 78kg, unzipped ivory satin gown, 3-inch back gap, soft waist spill, anxious face, marble suite, 85mm f/1.4 lens, 3200K key light.
2. 8K photograph, 28-year-old female, AFTER: 60kg, WHR 0.68, drop-waist basque satin gown, cat-eye corset, snatched waist, radiant glass skin, beaming smile, same marble room.
3. Hyper-realistic image, 32-year-old SA bride, BEFORE: 82kg, tight Xhosa print dress pulling at waist, facial bloat, stressed in fitting mirror.
4. Hyper-realistic image, 32-year-old SA bride, AFTER: 62kg, WHR 0.69, structured traditional Xhosa dress, sheer cape train, sharp jawline, glass skin.
5. High-fashion 8K portrait, 25-year-old gala guest, BEFORE: 75kg, soft arms, double chin posture, struggling with midnight-blue velvet dress zipper.
6. High-fashion 8K portrait, 25-year-old gala guest, AFTER: 58kg, sculpted deltoids, defined cervicomental angle, velvet dress zipped effortlessly, elegant pose.
7. Studio photograph, 35-year-old matron of honor, BEFORE: 80kg, waist spill over shapewear, tired facial expression, holding tape measure.
8. Studio photograph, 35-year-old matron of honor, AFTER: 63kg, WHR 0.70, flat core, emerald green satin dress, youthful radiant face, elegant smile.
9. Cinematic shot, 29-year-old bride, BEFORE: 76kg, sitting in robe, holding gown hanger with worried expression, lower belly volume.
10. Cinematic shot, 29-year-old bride, AFTER: 59kg, standing by arched window, sheer lace corset gown, sunlit snatched waist, defined shoulders.
11. Close-up photograph, 26-year-old bridesmaid, BEFORE: periocular fluid retention, soft cheek contour, frowning while holding tight bodice.
12. Close-up photograph, 26-year-old bridesmaid, AFTER: sharp cheekbones, zero facial bloat, defined jawline, smiling in blue silk dress.
13. 8K commercial image, 30-year-old male groom, BEFORE: 92kg, double-breasted tuxedo straining at midsection button, rounded face.
14. 8K commercial image, 30-year-old male groom, AFTER: 78kg, V-taper frame, midnight-blue tuxedo buttoned smoothly, chiseled gonial angle.
15. Macro photo, back view of 27-year-old female, BEFORE: back fat folds overlapping corset edge of open dress.
16. Macro photo, back view of 27-year-old female, AFTER: smooth back muscle, defined scapulae, dress zipped seamlessly.
17. High-contrast fashion render, 23-year-old matric student, BEFORE: 72kg, soft midsection in unzipped red satin dress.
18. High-contrast fashion render, 23-year-old matric student, AFTER: 55kg, WHR 0.67, red satin dress with high thigh slit, sculpted legs, snatched waist.
19. Architectural indoor shot, 34-year-old bride, BEFORE: sitting at vanity, holding bloated stomach in silk robe.
20. Architectural indoor shot, 34-year-old bride, AFTER: standing in silk robe, flat stomach, cinched waistline, radiant face.
21. Realistic render, 31-year-old female in tailor shop, BEFORE: tailor adding fabric extension on gown back.
22. Realistic render, 31-year-old female in tailor shop, AFTER: tailor taking in dress waist by 3 inches, model smiling.
23. Close-up 8K, female collarbone and neck, BEFORE: soft tissue covering clavicle bone.
24. Close-up 8K, female collarbone and neck, AFTER: sharp, pronounced clavicle definition, lean neck lines, strapless dress edge.
25. Transformation pair, 28-year-old bride, BEFORE: 79kg unzipped vs AFTER: 60kg fully zipped liquid satin gown, neutral lighting.

#### Photo Blueprints — Segment 2: Summer Body (26–50)

26. 8K beach photograph, 24-year-old female, BEFORE: 74kg, soft core, high-waisted shorts over bikini, sitting self-consciously on sunbed.
27. 8K beach photograph, 24-year-old female, AFTER: 56kg, WHR 0.68, flat core, coral high-cut bikini, wet wavy hair, bronzed skin, ocean backdrop.
28. 8K beach photograph, 26-year-old male, BEFORE: 92kg, soft core, loose tee over swim trunks on beach walkway, self-conscious posture.
29. 8K beach photograph, 26-year-old male, AFTER: 75kg, 6-pack abs, serratus clarity, 5-inch olive trunks, open white linen shirt, shoreline walk.
30. Action shot, 22-year-old female, BEFORE: 70kg, sitting on pool edge, pulling linen cover-up down to hide waist.
31. Action shot, 22-year-old female, AFTER: 54kg, leaping into pool, toned glutes, flat stomach, high-cut yellow bikini.
32. Lifestyle portrait, 29-year-old male at beach club, BEFORE: 88kg, holding drink in front of stomach to hide gut.
33. Lifestyle portrait, 29-year-old male at beach club, AFTER: 76kg, lean athletic torso, broad shoulders, holding drink at side, smiling.
34. Macro photograph, female lower back, BEFORE: soft hip volume spilling over bikini bottoms.
35. Macro photograph, female lower back, AFTER: smooth hip-to-waist transition, zero fluid retention, tight gluteal shelf.
36. Full-body shot, 21-year-old female, BEFORE: standing in hotel room mirror trying on bikini, frowning.
37. Full-body shot, 21-year-old female, AFTER: posing in hotel mirror, flat stomach, defined obliques, radiant bronzed skin.
38. Outdoor photo, 28-year-old male, BEFORE: slouching in yacht deck chair, abdominal rolls visible.
39. Outdoor photo, 28-year-old male, AFTER: standing at yacht railing, shredded core, vascular arms, direct sunlight.
40. 25-year-old female in resortwear, BEFORE: 72kg, oversized tunic hiding frame.
41. 25-year-old female in resortwear, AFTER: 57kg, sheer crochet cover-up over bikini, cinched waist visible.
42. Realistic render, 27-year-old male, BEFORE: unbuttoning Hawaiian shirt, hesitant posture.
43. Realistic render, 27-year-old male, AFTER: open Hawaiian shirt flying back, lean V-taper, confident stride.
44. Close-up photo, female abdominal region, BEFORE: smooth, undefined midsection, mild bloat.
45. Close-up photo, female abdominal region, AFTER: sharp rectus abdominis line, low subcutaneous fat, sun-kissed skin.
46. South African holiday setting, 23-year-old female (Cape Town), BEFORE: holding towel wrapped around waist.
47. South African holiday setting, 23-year-old female (Cape Town), AFTER: towel on sand, walking in high-cut bikini, sculpted legs.
48. High-exposure 8K image, 31-year-old male, BEFORE: 95kg, broad but smooth chest and midsection.
49. High-exposure 8K image, 31-year-old male, AFTER: 80kg, chest-shoulder separation, 6-pack abs, defined serratus anterior.
50. Transformation pair, 24-year-old female, BEFORE: towel wrapped vs AFTER: high-cut bikini on beach, side-by-side.

#### Photo Blueprints — Segment 3: Limited Resources (51–75)

51. Authentic 8K image, 30-year-old mother, BEFORE: 82kg, plain oversized tee, modest kitchen, looking at expensive receipt with stressed face.
52. Authentic 8K image, 30-year-old mother, AFTER: 62kg, flat core, black leggings, preparing eggs and bread in modest kitchen, smiling.
53. Hyper-realistic photo, 24-year-old male student, BEFORE: 88kg, soft chest/core, sitting on bed looking at expensive gym contract.
54. Hyper-realistic photo, 24-year-old male student, AFTER: 72kg, lean athletic build, performing push-up in small bedroom, plain grey tee.
55. Raw indoor portrait, 35-year-old female, BEFORE: soft waist, holding expensive superfood tub with confused/frustrated face.
56. Raw indoor portrait, 35-year-old female, AFTER: snatched waist, holding supermarket eggs and macadamia milk, radiant natural face.
57. Action shot, 22-year-old male, BEFORE: attempting home workout, looking fatigued in loose sweatpants.
58. Action shot, 22-year-old male, AFTER: calisthenics dip between two kitchen chairs, dense triceps, lean core.
59. Macro image, modest kitchen counter, BEFORE: cluttered with expensive diet teas and fake supplement bottles.
60. Macro image, modest kitchen counter, AFTER: simple RAFL staples (eggs, canned pilchards, low-GI bread) with Aime macro overlay.
61. 28-year-old female, BEFORE: 78kg, sitting on sofa, loose hoodie hiding body.
62. 28-year-old female, AFTER: 60kg, standing in living room, plain tank top, flat stomach, athletic legs.
63. Realistic portrait, 26-year-old male, BEFORE: standing near open fridge with few items, worried expression.
64. Realistic portrait, 26-year-old male, AFTER: holding phone displaying Aime parsing fridge items into custom meal plan, fit physique.
65. 40-year-old mother, BEFORE: 85kg, fatigue lines under eyes, holding gym bag overwhelmed.
66. 40-year-old mother, AFTER: 65kg, youthful radiant face, doing wall exercise at home, cinched waist.
67. Close-up photo, male arms/torso, BEFORE: undefined arms, soft lower belly.
68. Close-up photo, male arms/torso, AFTER: muscular forearms, vascularity, flat stomach, plain cotton tee.
69. 23-year-old female student, BEFORE: eating instant noodles, bloated face.
70. 23-year-old female student, AFTER: eating budget egg/bread meal, clear glass skin, lean core.
71. 25-year-old SA male (township park), BEFORE: soft frame holding soda bottle.
72. 25-year-old SA male (township park), AFTER: muscle-up on pull-up bar, shredded core, plain shorts.
73. Transformation pair, 32-year-old female, BEFORE: loose hoodie in modest room vs AFTER: fitted tank top, flat stomach.
74. Phone screen close-up, showing "Paywall $20/mo" crossed out in red, modest living room background.
75. Phone screen close-up, showing "TEB Free RAFL Engine Active", simple home meal prep background.

#### Photo Blueprints — Segment 4: Disability & Injury (76–100)

76. Clinical 8K photograph, 37-year-old female (Tiffany profile), BEFORE: 63kg, soft core, holding lower back wincing, knee sleeve visible.
77. Clinical 8K photograph, 37-year-old female (Tiffany profile), AFTER: 53kg, cinched waist, Wall Pilates bridge with feet flat on white wall, green force vectors.
78. Hyper-realistic image, 38-year-old male, BEFORE: 88kg, soft core, sitting on bed rubbing painful knee after jogging.
79. Hyper-realistic image, 38-year-old male, AFTER: 72kg, flat midsection, riding recumbent bike with full lumbar support, 15-degree knee angle.
80. Action shot, 42-year-old female, BEFORE: attempting floor sit-up, neck strained, back arching in pain.
81. Action shot, 42-year-old female, AFTER: Wall Press Isometric Core Hold, lumbar flat to floor, deep core engaged, flat stomach.
82. Studio render, 35-year-old female, BEFORE: looking at high-impact workout video with fearful expression.
83. Studio render, 35-year-old female, AFTER: Wall Supported Single-Leg Press, 50% MVC hold, zero knee strain, lean legs.
84. Spine/pelvis diagram, BEFORE: red force vectors showing vertical spinal compression during heavy squat.
85. Spine/pelvis diagram, AFTER: green force vectors showing anti-shear wall force conversion (F_w) protecting lumbar discs.
86. 45-year-old corporate male, BEFORE: 92kg, slouching, forward head posture, central abdominal fat.
87. 45-year-old corporate male, AFTER: 76kg, erect posture, flat midsection, recumbent bike Zone 2 cardio.
88. 31-year-old post-natal female, BEFORE: checking for diastasis recti gap with worried expression.
89. 31-year-old post-natal female, AFTER: Wall Pilates pelvic tilt, deep transversus abdominis engaged, closed gap, tight waist.
90. 50-year-old female, BEFORE: sitting on chair with swollen knee elevated.
91. 50-year-old female, AFTER: standing smoothly without support, 10kg weight loss, supportive activewear.
92. Recumbent bike pedal setup, close-up showing exact 15-degree knee flexion angle with green alignment graphics.
93. Wall Pilates heel contact close-up, showing gluteus maximus and hamstring engagement vectors.
94. 39-year-old male, BEFORE: 96kg, holding ice pack to lower back.
95. 39-year-old male, AFTER: 80kg, lean core, completing Zone 2 recumbent session without pain.
96. 36-year-old SA female (Cape Town), BEFORE: sitting on mat frustrated by back pain.
97. 36-year-old SA female (Cape Town), AFTER: Wall Pilates bridge hold, snatched waist, beaming smile.
98. Transformation pair, 37-year-old female (Tiffany baseline), BEFORE: wincing in lumbar pain vs AFTER: Wall Pilates bridge execution.
99. Knee joint 3D graphic, showing zero articular cartilage shear during recumbent pedaling.
100. Aime app interface render, showing "Biomechanical Constraint Filter Active: High Impact Excluded".

#### Photo Blueprints — Segment 5: Maintenance & Toning (Tier 4) (101–125)

> **[PENDING — not present in the source file.]** Slots 101–125 are reserved. Supply the source text or request a fresh draft.


### 5.6 Short-Form Video Reel Concepts (125)
Each concept: hook (0-3s) → transition (3-4s) → payoff (4-7s), then CTA. Numbers run 1-125 across the five segments.

#### Reels — Segment 1: Special Occasions (1–25)

> **[PENDING — not present in the source file.]** Slots 1–25 are reserved. Supply the source text or request a fresh draft.


#### Reels — Segment 2: Summer Body (26–50)

26. Towel Drop Transition: (0–3s) Male wrapped in towel hiding torso → (3–4s) Towel toss to camera → (4–7s) Walking shoreline in 5-inch trunks with 6-pack abs. CTA: Get Summer Plan.
27. Shirt Cover-Up Removal: (0–3s) Female sitting at pool pulling shirt down → (3–4s) Water splash cut → (4–7s) Standing in high-cut bikini, flat core. CTA: Link in Bio.
28. Unseasoned Chicken Throw: (0–3s) Male tearing up dry chicken/broccoli meal prep box → (3–4s) Meal swap → (4–7s) Eating social braai plate, shredded abs on display. CTA: Flexible Dieting.
29. Flight Countdown: (0–3s) Looking at Cape Town flight confirmation (3 weeks away) → (3–4s) Plane window transition → (4–7s) Stepping onto beach with lean core. CTA: Start 21-Day Cut.
30. Stomach Sucking-In Relief: (0–3s) Sucking in stomach in bathroom mirror → (3–4s) Exhale → (4–7s) Stomach stays naturally flat without sucking in. CTA: Burn Adipose Fat.
31. Unboxing Bikini Fit: (0–3s) Unboxing new bikini, looking doubtful → (3–4s) Snap transition → (4–7s) Wearing bikini with flat stomach and firm glutes. CTA: DM "BEACH".
32. Beer Can Crush: (0–3s) Male holding beer looking down at gut → (3–4s) Crushes can → (4–7s) Lean V-taper in unbuttoned linen shirt. CTA: Get Male Cut.
33. Group Photo Hide: (0–3s) Female standing behind friends in group photo to hide waist → (3–4s) Flash transition → (4–7s) Posing in front row with snatched waist. CTA: Claim Summer Body.
34. December Festivities Warning: (0–3s) Text: "3 Weeks Until KeDezemba Festivities" → (3–4s) Sunset light flare → (4–7s) Dancing at beach club with flat midsection. CTA: Download App.
35. Shorts Button Snap: (0–3s) Pinching waist fat over tight denim shorts → (3–4s) Button clicks → (4–7s) Shorts sit loose over lean waist. CTA: Start Fat Loss.
36. Treadmill Burnout Swap: (0–3s) Running endlessly on treadmill exhausted → (3–4s) Machine switch → (4–7s) 20-min Zone 2 bike session, lean core result. CTA: Zone 2 Protocol.
37. Sunlight Shadow Test: (0–3s) Harsh overhead sun showing belly shadow → (3–4s) Light sweep → (4–7s) Sunlight highlighting abdominal line definition. CTA: Fluid Clear Protocol.
38. Salad Frustration Swap: (0–3s) Eating plain lettuce while friends eat pizza → (3–4s) Aime macro rebalance → (4–7s) Eating pizza slice, maintaining 6-pack. CTA: Try RAFL.
39. Hotel Room Mirror Check: (0–3s) Pale skin, soft midsection in hotel light → (3–4s) Screen tap → (4–7s) Tanned, vascular, beach-ready frame. CTA: DM "SUMMER".
40. TikTok Trend Match: (0–3s) Watching viral TikTok beach body video → (3–4s) Phone flip → (4–7s) Achieving identical beach frame in real life. CTA: Get The Plan.
41. Bikini Strap Adjustment: (0–3s) Nervous adjusting of bikini straps → (3–4s) Hair flip → (4–7s) Confident stride on sand, sculpted glutes. CTA: Build Beach Body.
42. Tight Tee Swap: (0–3s) Male trying on tight tee showing belly bulge → (3–4s) Shirt change → (4–7s) Fitted chest, flat midsection. CTA: V-Taper Guide.
43. Alcohol Macro Auto-Balance: (0–3s) Pouring holiday cocktail with guilt → (3–4s) Aime app auto-balancing remaining macros → (4–7s) Enjoying drink, lean core. CTA: Use Aime.
44. Tanning Oil Glow: (0–3s) Applying tanning oil to soft stomach → (3–4s) Sun flash → (4–7s) Tanned, sculpted abdominal wall. CTA: Get Shredded.
45. Yacht Deck Stride: (0–3s) Walking onto yacht feeling self-conscious → (3–4s) Confidence shift → (4–7s) Turning heads in resortwear, shredded abs. CTA: Transform Now.
46. 500 Crunch Myth: (0–3s) Text: "Stop doing 500 crunches a day" → (3–4s) AMPK oxidation graphic → (4–7s) Flat core achieved via Zone 2 cardio. CTA: Learn Real Fat Loss.
47. Vacation Countdown Sync: (0–3s) Checking holiday countdown app → (3–4s) Fast forward → (4–7s) Stepping onto resort pool deck with dream body. CTA: Start 14-Day Plan.
48. Cardboard Box Meal Toss: (0–3s) Tossing pre-packaged diet meal in trash → (3–4s) Local grocery cook → (4–7s) Lean beach body eating local food. CTA: Real Food Cut.
49. Poolside Entrance: (0–3s) Hiding behind sunbed umbrella → (3–4s) Steps into sun → (4–7s) Confident stride across pool deck, flat stomach. CTA: Own the Summer.
50. Post-Vacation Lock-In: (0–3s) Vacation ends: "How to maintain your beach body" → (3–4s) UI switch to Tier 4 → (4–7s) Keeping abs 3 months later. CTA: Lock It In.

#### Reels — Segment 3: Limited Resources (51–75)

51. Gym Contract Tear: (0–3s) Ripping expensive $150/mo gym contract → (3–4s) Floor transition → (4–7s) Executing home calisthenics, lean core. CTA: No Gym Needed.
52. Specialty Food Swap: (0–3s) Holding expensive organic salmon with high price tag → (3–4s) Swap to eggs/canned pilchards → (4–7s) Achieving identical bioenergetic results. CTA: Use RAFL.
53. Fridge Parsing Snap: (0–3s) Opening modest fridge with basic staples → (3–4s) Phone camera snap → (4–7s) Aime parsing inventory into custom meal plan. CTA: Parse Your Fridge.
54. App Paywall Rage: (0–3s) Downloading "Free" app → Hit $20/mo paywall immediately → (3–4s) Red 'X' slam → (4–7s) TEB zero-paywall baseline setup active. CTA: Zero Paywalls.
55. Receipt Comparison: (0–3s) Holding $200 specialty grocery receipt vs $15 RAFL basket → (3–4s) Receipt crumple → (4–7s) Model holding basic groceries, in shape. CTA: Get RAFL Engine.
56. Crowded Room Workout: (0–3s) Trying to workout in tiny bedroom, bumping furniture → (3–4s) Pan → (4–7s) Executing simple zero-space wall/floor movement, lean frame. CTA: Home Protocols.
57. 20-Ingredient Recipe Slam: (0–3s) Looking at complicated 20-ingredient diet recipe → (3–4s) Book slam → (4–7s) 3-ingredient budget meal prep, snatched waist. CTA: Simple Meals.
58. Protein Powder Price Drop: (0–3s) Frustrated face over $80 protein tub → (3–4s) Swap to local soya isolate → (4–7s) Calculating 25g protein for pennies, lean muscle. CTA: Read Guide.
59. Chair Dips Setup: (0–3s) Male setting up two kitchen chairs in basic tee → (3–4s) Speed ramp → (4–7s) Executing dips, dense triceps and core. CTA: Home Muscle Plan.
60. Single Family Meal: (0–3s) Mother cooking separate diet meal while family eats dinner → (3–4s) Blend → (4–7s) Family eating same RAFL meal together, mother losing weight. CTA: Single-Meal Plans.
61. Bison Myth Callout: (0–3s) Text: "You don't need grass-fed bison to see abs" → (3–4s) Plate flip → (4–7s) Eggs and bread turned into macro success. CTA: Try TEB Free.
62. Fancy Gear Rejection: (0–3s) Looking at $120 designer workout top price tag → (3–4s) Cut → (4–7s) Training in basic grey cotton tee, great shape. CTA: Start Today.
63. Barcode Scan Upgrade Block: (0–3s) Scanning barcode → "Upgrade to Premium to view Macros" → (3–4s) Phone smash effect → (4–7s) Aime free barcode parsing. CTA: Switch to TEB.
64. Student Instant Noodle Fix: (0–3s) Student eating instant noodles, bloated face → (3–4s) Swap → (4–7s) Low-cost student RAFL meal plan, clear skin, lean core. CTA: Student Hacks.
65. Pantry Photo POV: (0–3s) POV: Taking photo of open pantry with phone → (3–4s) Overlay graphics → (4–7s) Exact macro breakdown generated instantly. CTA: DM Your Pantry.
66. Boutique Studio Laugh: (0–3s) Looking at $30/class boutique studio prices → (3–4s) Laughing → (4–7s) Executing bodyweight routine at home, fit body. CTA: Zero Gym Cost.
67. Tap Water Pre-Workout: (0–3s) Pouring tap water into bottle with pinch of sea salt → (3–4s) Text: "Pre-workout $0" → (4–7s) Executing push-ups with high energy. CTA: Learn Electrolytes.
68. After-Work Fatigue Drop: (0–3s) Tired worker coming home, no energy for 1-hour gym drive → (3–4s) Drops bag → (4–7s) 15-min home routine completed in living room. CTA: 15-Min Workouts.
69. Township Park Calisthenics: (0–3s) Township youth looking at park pull-up bar → (3–4s) Jump up → (4–7s) Muscle-up execution, shredded core. CTA: Calisthenics Cut.
70. Zero Subscription Guarantee: (0–3s) Frustration of quitting past apps due to hidden costs → (3–4s) UI sweep → (4–7s) Lifetime transparency mandate screen. CTA: Join TEB.
71. Water Bottle Weight Hack: (0–3s) Filling two 2L water bottles for weights → (3–4s) Lift → (4–7s) Toned arms and shoulders. CTA: Home Weight Hacks.
72. Cancel Subscriptions: (0–3s) Looking at bank statement with $50/mo app fees → (3–4s) Canceling subs → (4–7s) Using free Aime baseline, losing weight. CTA: Cut Expenses.
73. Anti-Influencer Reality: (0–3s) Text: "Stop letting expensive influencers lie to you" → (3–4s) Reality check → (4–7s) Real budget results proof using store items. CTA: Real Science.
74. Canned Fish Macro Power: (0–3s) Cooking basic canned pilchards with rice → (3–4s) Macro overlay: 40g Protein, $0.50 cost → (4–7s) Lean physique. CTA: Get Budget Recipes.
75. Permanent Budget Lock-In: (0–3s) Reaching goal weight using store items → (3–4s) UI switch → (4–7s) Tier 4 maintenance active without buying supplements. CTA: Maintain Forever.

#### Reels — Segment 4: Disability & Injury (76–100)

76. Jumping Squat Wince: (0–3s) Female wincing during jumping squat → (3–4s) Red 'X' slam → (4–7s) Smooth Wall Pilates bridge with green force vectors. CTA: Joint-Safe Plan.
77. Generic App Pain Callout: (0–3s) Male holding back after generic app workout → (3–4s) Green vector sweep → (4–7s) Recumbent bike Zone 2 cardio with full lumbar support. CTA: Zero-Impact Workout.
78. Spinal Compression Diagram: (0–3s) 3D graphic of spinal disc pinching during squats → (3–4s) Wall vector conversion → (4–7s) Anti-shear force path ( → ) protecting discs. CTA: Read Science.
79. Knee Sleeve Removal: (0–3s) Female looking at knee sleeve on bed, feeling helpless → (3–4s) Stand up → (4–7s) Unassisted movement, flat stomach, pain-free. CTA: Tiffany Protocol.
80. Burpee Delete Callout: (0–3s) Text: "If your app prescribes burpees to someone with bad knees, delete it" → (3–4s) App delete animation → (4–7s) Biomechanical filter UI demo. CTA: Safe Fitness.
81. Neck Strain Crunch Swap: (0–3s) Neck straining during crunches → (3–4s) Shift → (4–7s) Wall Isometric Core Hold, flat lumbar, cinched core. CTA: Core Protection.
82. Doctor Paradox Resolution: (0–3s) Doctor: "You need to lose weight but can't run" → (3–4s) Transition → (4–7s) PSMF + Recumbent Bike routine executing fat burn. CTA: Low-Impact Fat Loss.
83. MRI Disc Bulge Fix: (0–3s) MRI showing lumbar disc bulge → (3–4s) Slide → (4–7s) Transversus abdominis recruitment model stabilizing spine. CTA: Spine-Safe Core.
84. Chair Standing Wince: (0–3s) Male wincing getting up from office chair → (3–4s) Fast forward → (4–7s) Smooth posture, flat midsection, pain-free standing. CTA: Fix Back Pain.
85. Swollen Knee Ice Swap: (0–3s) Rubbing swollen knee after jogging attempt → (3–4s) Ice pack drop → (4–7s) Smooth recumbent pedaling at 80 RPM. CTA: Zone 2 Bike.
86. Tiffany 10kg Case Study: (0–3s) Text: "How Tiffany dropped 10kg with active back/knee injuries" → (3–4s) Protocol metrics → (4–7s) Full 14-day transformation proof. CTA: Read Case Study.
87. High-Jumper Video Sigh: (0–3s) Watching video of high-jumping models, sighing → (3–4s) Screen switch → (4–7s) Adaptive Wall Pilates routine execution. CTA: Adaptive Plans.
88. Movement Fear Extinction: (0–3s) Fearful face before attempting core movement → (3–4s) Wall setup → (4–7s) Confident smile during Wall Single-Leg Press. CTA: Safe Movement.
89. Plyometric Skull Cross-Out: (0–3s) Standard plyometric workout crossed out with skull icon → (3–4s) Filter sweep → (4–7s) Biomechanical replacement matrix loading. CTA: Get Filters.
90. Recumbent Seat Angle Setup: (0–3s) POV: Adjusting recumbent bike seat for → knee angle → (3–4s) Pedal stroke → (4–7s) Smooth pedaling with lipid burn stats. CTA: Bike Protocols.
91. Pill Bottle Drop: (0–3s) Waking up with back stiffness, taking painkillers → (3–4s) Bottle drop → (4–7s) Morning anti-flexion movement, pain-free day. CTA: Biokinetic Flow.
92. Zero Knees Force Graphic: (0–3s) Text: "Burn 500 Calories Without Putting 1lb of Force on Your Knees" → (3–4s) Force graph → (4–7s) Recumbent bike bioenergetic display. CTA: Learn How.
93. Floor Get-Up Technique: (0–3s) Female struggling to push up from floor → (3–4s) Wall technique → (4–7s) Stands up effortlessly, lean midsection. CTA: Rebuild Strength.
94. Barbell Disappear: (0–3s) Heavy barbell squat attempt, knees caving → (3–4s) Barbell disappears → (4–7s) Wall Isometric squat hold with zero shear. CTA: Anti-Shear Plan.
95. 4 Anti-Force Vectors: (0–3s) Text: "The 4 Anti-Directional Core Forces" → (3–4s) Vector animation → (4–7s) Executing anti-extension hold safely. CTA: Save Post.
96. Silent Apartment Workout: (0–3s) Attempting jumping jacks, stomping loudly → (3–4s) Shhh icon → (4–7s) Silent, non-impact Wall Pilates flow. CTA: Silent Workouts.
97. Diastasis Recti Check: (0–3s) Post-natal woman checking diastasis recti gap → (3–4s) Deep core activation → (4–7s) Closed gap, tight waist. CTA: Post-Natal Core.
98. Running vs Wall Load: (0–3s) Graph: Running joint load vs Wall Bridge load → (3–4s) Data pulse → (4–7s) Wall Bridge execution, zero compression. CTA: Protect Your Spine.
99. Zero Gasping Finishing: (0–3s) Model finishing workout without sweating/gasping in pain → (3–4s) Heart rate check → (4–7s) Relaxed smile in Zone 2. CTA: Try Zone 2.
100. Rehab-to-Maintenance Switch: (0–3s) Reaching 53kg goal weight post-rehab → (3–4s) UI switch → (4–7s) Tier 4 eucaloric joint-safe maintenance active. CTA: Maintain Safely.

#### Reels — Segment 5: Maintenance & Toning (Tier 4) (101–125)

> **[PENDING — not present in the source file.]** Slots 101–125 are reserved. Supply the source text or request a fresh draft.


### 5.7 Creative Suite Deployment Safeguards *(proposed, for review)*
These are protective rules added alongside the blueprints so that the Creative Suite stays consistent with the Tier 2 mandate. Edit or remove as you see fit.
*   **Synthetic imagery labelling:** Blueprint images are AI-generated illustrations, not real client results. Label them as such. Real before/after content is used only with documented consent from real users.
*   **Platform and advertising policy check:** Before/after body imagery and specific kg-in-X-days claims are restricted on Meta, TikTok and Google, and in South African advertising and consumer-protection rules. Run each asset against current platform policy before publishing.
*   **Claims discipline:** Avoid unsupported absolutes (e.g. "zero force", "burn 500 calories", "burn adipose fat") and avoid naming hormonal outcomes as guarantees.
*   **Deadline feasibility messaging:** Where a user's deadline is unrealistic, the app explains why, then offers the earliest safe date and the best alternative plan while keeping metabolic health intact. Marketing for sprint segments must reflect this and never promise a date-bound weight outcome.
*   **Body-image care:** Avoid shame-based hooks and target physiques below healthy BMI ranges; include a short health disclaimer and a prompt to consult a medical professional.

---
*This document serves as the master operational codex for The Eating Bible (TEB). All algorithms, biological pathways, and governance rules are locked into core memory.*