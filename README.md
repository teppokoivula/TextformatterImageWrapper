ProcessWire Image Wrapper Textformatter
=======================================

NOTE: this module is in beta state, as in "use in production environment (or
anywhere else for that matter) at your own risk." This approach is also only
one of many, as discussed in this processwire.com forum thread in more detail:
http://processwire.com/talk/topic/1344-captions-for-images-in-tinymce/

When applied to fields with HTML content, this textformatter catches `<img>`
tags and wraps them with `<div>` elements. These wrapper elements get classes
of wrapped `<img>` elements, class "with_caption" if caption exists + default
class "image_wrap".

Module setting show_captions (enabled by default) also adds image alt text (if
one exists) as a caption to the wrapper.

## Markup example

Basic embedded image `<img class="align_left" alt="Alt text" src="..." />`, when
processed by this textformatter, becomes wrapped markup like this:


    <div class="image_wrap with_caption align_left">
        <img class="align_left" alt="Alt text" src="..." />
        <div class="caption">Alt text</div>
    </div>
