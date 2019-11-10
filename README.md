# TextMeshAnimator

Adds basic shake and wave animation tags to Unity TextMesh. This is a proof of concept as I found it pretty hard to find any decent documentation on a way to achieve this.

![Text](https://raw.githubusercontent.com/Abban/TextMeshAnimator/master/text.gif)

What it does is:

1. Parse any `<wave></wave>`, `<shake></shake>` and `<shake=0.5></shake>` (for a custom amount) into `<link>` tags which can then be accessed through Textmesh's linkInfo property.
2. Set all characters alpha to 0.
3. Start a Coroutine that makes them visible one by one.
4. In Update it checks to see if any shake or wave characters are visible and applies the effects.