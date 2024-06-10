---
title: About Design Systems
description: List of the best design systems.
date: 2024-01-01
---
{% for post in collections.doc %}
- [{{ post.data.title }}]({{ post.url | url }})
{% endfor %}

### Design systems typically include the following

**Overview**: provides an overview of the design system, which is particularly important for more complex systems. It can mention the new updates to the system, or a list of principles and shared values that define what good design means for the organization. 

**Foundations**: visual or style guidelines that cover color, typography, iconography, imagery, sound, motion, and more. 

**Components**: library of reusable UI elements, expressed both visually and via code. The UI components are typically crafted to work together, through a combination of user research, performance testing, and accessibility evaluation. Components are typically accompanied by a set of guidelines or rationale around how and when they should be used.

**Patterns**: library of reusable component combinations. Patterns represent best practices for arranging the components together to help solve common user needs.

**Content guidelines**: covers standards around voice and tone and the mechanics of grammar and style. It might also include a list of words and how they should or should not be used.

**Brand guidelines**: some design systems include brand guidelines, which outline brand values, personality, a brand promise, or a showcase of the brand out in the world.

**Resources**: include a range of tools, plug-ins, UI kits, articles, and video tutorials that support the entire creation process.