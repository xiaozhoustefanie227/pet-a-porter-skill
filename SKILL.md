---
name: pet-a-porter
display_name: Pet-à-Porter
version: 2.0.0
description: Analyze a user's outfit photo, choose a pet that matches the same fashion identity, lightly echo the outfit through pet styling, and naturally add the pet into the image while preserving the person.
author: A2H Market
license: MIT
---

# Pet-à-Porter

**Find the pet that matches your style.**

Pet-à-Porter is a fashion-led image-editing skill. Given a single outfit or lifestyle photo, it analyzes the person’s style DNA, chooses a pet that belongs in the same aesthetic world, styles that pet to lightly echo the person’s outfit, and integrates the pet naturally into the original image.

The goal is not to add a random cute animal. The result should feel as if the person genuinely owns this pet and as if the pet belongs to the same visual world, wardrobe logic, and lifestyle atmosphere.

## Core Principles

1. **Style first, species second.** Identify the human’s fashion identity before choosing a pet.
2. **Match the world, not just the colors.** Similar color alone is not enough.
3. **Echo the outfit with restraint.** The pet may wear clothing or accessories that lightly reflect the person’s look.
4. **Preserve the person.** The uploaded person’s identity and styling are the highest priority.
5. **Natural integration.** The pet must share the same perspective, lighting, scale, and scene logic.
6. **Editorial restraint.** The result should be chic, believable, tasteful, and highly shareable.

## When to Use

Use this skill when the user uploads an outfit or lifestyle photo and asks to:
- match them with a pet based on their style;
- add a stylish companion pet to the image;
- create a fashion-pet portrait;
- create a "mini me" pet version of their outfit;
- add a pet whose styling echoes their clothing.

Do not use this skill for:
- veterinary or real pet-care advice;
- breed suitability for ownership;
- health, temperament, or allergy claims;
- pet shopping recommendations.

## Input Requirements

Preferred input:
- one clear outfit or lifestyle photo;
- enough visibility to read silhouette, palette, texture, accessories, and scene context;
- full-body or 3/4-body is ideal;
- keep the original composition unless the user explicitly asks otherwise.

If the user explicitly names a pet, breed, mode, or styling detail, honor that request and use style analysis to refine the result.

## Workflow

### Step 1 — Read the Style DNA

Analyze the look across four layers.

#### A. Style Labels
Choose 1–3 best-fit labels:
- Quiet Luxury
- Old Money
- French Chic
- Clean Girl
- Minimalist
- Vintage
- Coquette
- Balletcore
- Preppy
- Streetwear
- Y2K
- Sporty
- Resort
- Art Girl
- Rich Girl / Heiress
- Avant-garde
- Bohemian
- Gorpcore
- Romantic
- Soft Tailoring
- Modern Classic
- Eclectic

#### B. Mood / Personality Keywords
Infer 3–5 visual descriptors such as:
- refined
- relaxed
- cool
- playful
- polished
- romantic
- delicate
- sculptural
- artistic
- sporty
- understated
- dramatic
- nostalgic
- youthful
- elegant
- urban
- effortless

These are visual style descriptors only.

#### C. Visual Cues
Read:
- silhouette and proportions;
- fabric and texture;
- color palette;
- level of tailoring or softness;
- shoes and bag;
- jewelry and accessories;
- hair and makeup direction if visible;
- setting and lifestyle context;
- visual era or styling reference when obvious.

#### D. Energy Level
Classify the look loosely as one of:
- understated / quiet;
- polished / refined;
- playful / expressive;
- bold / experimental;
- romantic / delicate;
- outdoorsy / functional.

### Step 2 — Choose the Pet Persona

Use `references/pet-matching-library.md` as a guide, not a rigid lookup table.

The pet choice should work at three levels:
1. **Aesthetic fit** — shape, texture, palette, and visual energy.
2. **Persona fit** — elegant, quirky, refined, playful, sculptural, soft, sporty, etc.
3. **Scene fit** — the pet should plausibly belong in the photographed environment.

Prefer small or medium companion pets unless the styling strongly supports a larger animal.

Default recommended pool:
- wire-haired dachshund
- smooth dachshund
- miniature poodle
- toy poodle
- miniature schnauzer
- Italian greyhound
- whippet
- Pomeranian
- Maltese
- bichon frise
- Papillon
- Cavalier King Charles Spaniel
- Jack Russell Terrier
- French bulldog
- Boston terrier
- Beagle
- Cocker Spaniel
- black cat
- Russian Blue cat
- white long-haired cat
- tuxedo cat
- Sphynx cat
- mini pig

### Step 3 — Select a Matching Mode

If the user does not specify a mode, use **Perfect Match**.

#### Perfect Match — Default
Choose the pet that most naturally belongs in the same aesthetic world.

#### Mini Me
Make the pet feel like a subtle style twin. The pet’s outfit or accessories may more clearly echo the human’s outfit.

#### Fashion Contrast
Create an intentionally surprising but still stylish pairing. Contrast should feel editorial, not random.

### Step 4 — Style the Pet

This is the upgraded logic in v2.0.0.

#### Main rule
**Mirror the aesthetic, then lightly echo the outfit.**

The pet should not wear a full human-costume replica unless the user explicitly requests that effect.

#### Pet styling hierarchy
Match the human outfit through one or more of these:
1. **Color echo** — same or neighboring color family.
2. **Material echo** — trench fabric, knit, satin, denim, soft wool, linen feel, etc.
3. **Silhouette echo** — draped, structured, sporty, tailored, voluminous, sleek.
4. **Detail echo** — collar, bow, tiny trench flap, scarf, pearl accent, flower detail.
5. **Energy echo** — clean, romantic, playful, polished, bold.

#### How strong should the echo be?
Use the human outfit’s style intensity.

**Understated / Quiet looks**
- keep pet styling minimal;
- a fine collar, tiny scarf, refined coat, or no clothing at all may be best.

**Polished / Refined looks**
- a small tailored coat, neat knit, or elegant accessory is appropriate.

**Romantic / Delicate looks**
- use soft drape, ribbon, floral detail, lace-like softness, or a pastel outfit.

**Playful / Expressive looks**
- use slightly more visible styling such as a coordinated top, bow, pearl collar, or tiny vest.

**Bold / Experimental looks**
- use sharper silhouette, more unusual pet choice, or fashion-forward pet styling.

#### Good examples
- beige trench coat + white tee + wide jeans → wire-haired dachshund in a tiny beige trench-inspired coat;
- blush pink draped evening dress → Maltese in a soft blush draped outfit or scarf with one floral accent;
- clean black blazer look → black cat with sleek leather collar;
- French vintage cardigan look → dachshund with subtle knit neck scarf.

#### Avoid
- exact human outfit cosplay unless explicitly requested;
- novelty costumes;
- over-accessorizing;
- branding or logos not already present;
- pet styling that overwhelms the human subject.

### Step 5 — Integrate the Pet into the Image

The human is the locked visual anchor.

#### Preserve
- face and facial geometry;
- expression where possible;
- body proportions;
- pose;
- skin tone;
- hair identity;
- clothing design and construction;
- bag, shoes, jewelry, and key accessories;
- original composition unless a small framing shift is needed.

#### Match
- camera angle;
- perspective;
- lens feel;
- light direction;
- color temperature;
- shadow quality;
- image texture / grain;
- depth of field;
- ground contact;
- pet scale.

#### Placement priorities
Prefer one of these:
- beside the lower leg;
- slightly in front or behind at ankle distance;
- seated near a chair, bag, doorway, sofa, or bench;
- walking beside the person;
- held only when the original pose physically supports it.

Never force pet contact that the original pose cannot support.

### Step 6 — Output

When a short text output is appropriate, give one concise editorial match line before the image.

Format:

**Your Fashion Pet: [Pet]**  
[One concise sentence explaining the match.]

Examples:

**Your Fashion Pet: Wire-haired Dachshund**  
Relaxed tailoring, soft neutrals, and effortless polish make this the most natural match.

**Your Fashion Pet: Maltese**  
Delicate drape, blush softness, and elegant femininity call for a pet with the same romantic charm.

Keep the explanation brief. The image is the main deliverable.

## Decision Notes

- If the person’s look is very minimal, pet styling should stay minimal too.
- If the pet outfit is used, it should visually echo the person rather than copy them literally.
- If the species match is good but clothing would reduce taste, skip pet clothing and use only a refined accessory.
- If the user explicitly asks for the pet’s outfit to echo the human look, increase the outfit echo strength while keeping the result elegant.

## Success Criteria

A strong result should feel like:
- the right person;
- the right pet;
- the right styling on the pet;
- the right scene integration;
- one coherent fashion image.
