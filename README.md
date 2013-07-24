ProcessWire Image Wrapper Textformatter
=======================================

NOTE: this module is in beta state, as in "use in production environment (or
anywhere else for that matter) at your own risk." This approach is also only
one of many, as discussed in this processwire.com forum thread in more detail:
http://processwire.com/talk/topic/1344-captions-for-images-in-tinymce/

This textformatter, when applied to fields with HTML content, identifies <img>
tags and wraps them with a <div> element. This <div> elements gets any classes
of the <img> element wrapped, class "with_caption" if caption exists + default
class "image_wrap".

Module setting show_captions (enabled by default) also adds image alt text (if
one exists) as a caption to the wrapper.

# Markup example

This basic embedded image ..

``
<img class="align_left" alt="Alt text" src="..." />
``

.. becomes wrapped image like this:

´´
<div class="image_wrap with_caption align_left">
    <img class="align_left" alt="Alt text" src="..." />
    <div class="caption">Alt text</div>
</div>
´´