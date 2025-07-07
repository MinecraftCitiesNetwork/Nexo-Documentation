---
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📤 Shulker Hitbox

**Shulker-Entity Hitboxes** takes an **offset, scale, length** and **direction**\
**Offset** only supports full blocks, as shulkers are forcefully put at a full block. Meaning you cannot offset it by 0.5 blocks\
**Scale** is a single integer and determines the scale of the furniture. You cannot scale only the height, like with Interaction-Entity Hitboxes\
**Length** determines the extra length of the hitbox, and can be between 1..2\
**Direction** determines the way the hitbox faces, if not specified, defaults to UP

{% hint style="warning" %}
This is only available for 1.20.5+ servers\
Should also be noted that the shulker-entity head will be visible on 1.21.1 & below\
It will be invisible for 1.21.2 and above as long as [https://bugs.mojang.com/browse/MC-278123](https://bugs.mojang.com/browse/MC-278123) is not fixed
{% endhint %}

```yaml
myitem:
  Mechanics:
    furniture:
      hitbox:
        shulkers:
        # - offset scale length direction visible
          - 0,0,0 1.0 1.0
          - 1,0,0 1.2 1.5 EAST
          - -1,0,0 0.8 2.0 UP
```

{% hint style="info" %}
If you struggle with finding the accurate hitbox-size you want for shulker-hitboxes, you can make them temporarily visible. To do this simply add `true` after the length or direction argument
{% endhint %}
