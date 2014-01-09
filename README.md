# Simple Photo

The simple theme for photo blogging with [Ghost](http://github.com/tryghost/ghost/).

## How to display photos only in a Ghost post listing

If you're an editor / just want to post photos:
Simply create a new post with an image as the first piece of content.  You may add additional content under the image.  It will be displayed on the posts page, but not on the listing page.

In your theme:
Use the following code to display only an image for each post
    {{#foreach posts}}
        {{content words="0"}}
    {{/foreach}}


The trick here is to request the full content of the post, but limit it to 0 words.  Since the image tag is the first element in the post (and Ghost wont count HTML tags/truncate them) it is still displayed.

## Copyright & License

Copyright (C) 2013 Ghost Foundation - Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
