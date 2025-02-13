---
layout: post
title: Trail Posting One
date: 2024-01-27 10:14:00-0400
description: Basic GitHub blog positing structure with image, audio, video, and comments options
tags: Trail Posting One
categories: Trail Posting One
disqus_comments: true
related_posts: true
featured: true
thumbnail: assets/img/9.jpg
toc:
  sidebar: left
---
This post shows makes a custom post including sidebar table of content, image, audio, video, twitter posts, and option for comments, and related posts.

## 1. SIDEBAR TABLE OF CONTENTS

Side bar table of content is based on '#' or '##' etc used for heading, sub-heading, .... etc. Let's see how that works out!

### Sidebar table of contents - subheading

Jean shorts raw denim Vice normcore, art party High Life PBR skateboard stumptown vinyl kitsch. Four loko meh 8-bit, tousled banh mi tilde forage Schlitz dreamcatcher twee 3 wolf moon. Chambray asymmetrical paleo salvia, sartorial umami four loko master cleanse drinking vinegar brunch. <a href="https://www.pinterest.com">Pinterest</a> DIY authentic Schlitz, hoodie Intelligentsia butcher trust fund brunch shabby chic Kickstarter forage flexitarian. Direct trade <a href="https://en.wikipedia.org/wiki/Cold-pressed_juice">cold-pressed</a> meggings stumptown plaid, pop-up taxidermy. Hoodie XOXO fingerstache scenester Echo Park. Plaid ugh Wes Anderson, freegan pug selvage fanny pack leggings pickled food truck DIY irony Banksy.

### Sidebar table of contents - Customizing Your Table of Contents
{:data-toc-text="Customizing"}

If you want to learn more about how to customize the table of contents of your sidebar, you can check the [bootstrap-toc](https://afeld.github.io/bootstrap-toc/) documentation. Notice that you can even customize the text of the heading that will be displayed on the sidebar.


## 2. ADDING VIDEO FILES
This is an example post with videos. 

### local video files
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/pexels-engin-akyurt-6069112-960x540-30fps.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/pexels-engin-akyurt-6069112-960x540-30fps.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    A simple, elegant caption looks good between video rows, after each row, or doesn't have to be there at all.
</div>

### embedding videos from different sources
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://www.youtube.com/embed/jNQXAC9IVRw" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://player.vimeo.com/video/524933864?h=1ac4fd9fb4&title=0&byline=0&portrait=0" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


## 3. ADDING AUDIO FILES - from local and external link
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include audio.html path="assets/audio/epicaly-short-113909.mp3" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include audio.html path="https://cdn.pixabay.com/download/audio/2022/06/25/audio_69a61cd6d6.mp3" controls=true %}
    </div>
</div>
<div class="caption">
    This is the caption for the audio files.
</div>

## 4. ADDING IMAGE FILES
This is an example post with image galleries.

### Normal images
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/9.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/7.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A simple, elegant caption looks good between image rows, after each row, or doesn't have to be there at all.
</div>

### Zoomable images
Just add `data-zoomable` to `<img>` tags to make zoomable.
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/8.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/10.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>


## 5. ADD TWITTER POSTS
A sample blog page that demonstrates the inclusion of Tweets/Timelines/etc. For more details on using the plugin visit: [jekyll-twitter-plugin](https://github.com/rob-murray/jekyll-twitter-plugin)

### Add Tweets
An example of displaying a tweet:
{% twitter https://twitter.com/rubygems/status/518821243320287232 %}

### Add Twitter Timeline
An example of pulling from a timeline:
{% twitter https://twitter.com/jekyllrb maxwidth=500 limit=3 %}


## 6. ADDING CODES
This theme implements a built-in Jekyll feature, the use of Rouge, for syntax highlighting.
It supports more than 100 languages.
### Basic markdown code
This example is in C++.
All you have to do is wrap your code in markdown code tags:

````markdown
```c++
code code code
```
````

For instance:
```c++
int main(int argc, char const \*argv[])
{
    string myString;

    cout << "input a string: ";
    getline(cin, myString);
    int length = myString.length();

    char charArray = new char * [length];

    charArray = myString;
    for(int i = 0; i < length; ++i){
        cout << charArray[i] << " ";
    }

    return 0;
}
```
### Show line numbers for the code also

If you want to display line numbers for a specific code block, all you have to do is wrap your code in a liquid tag:

{% raw %}
{% highlight c++ linenos %}  <br/> code code code <br/> {% endhighlight %}
{% endraw %}


The keyword `linenos` triggers display of line numbers.
Produces something like this:

For instance:
{% highlight c++ linenos %}

int main(int argc, char const \*argv[])
{
    string myString;

    cout << "input a string: ";
    getline(cin, myString);
    int length = myString.length();

    char charArray = new char * [length];

    charArray = myString;
    for(int i = 0; i < length; ++i){
        cout << charArray[i] << " ";
    }

    return 0;
}

{% endhighlight %}
