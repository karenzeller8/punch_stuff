About
=====

This is a project to build a static documentation website for
Couchbase. After checking out a variety of static frameworks, we
settled on Punch, in NodeJS.

Showstoppers/Blockers
======================
- Something better than Google Custom search or alternate page separatation/anchors, especially for jump-links. (Marty - investigating)

General Requirements/Features
================
- Add corporate website headers, footers, etc to docs initial landing page (Karen)
- Improve left navigation. Items at end disappear when multiple sub-menus are open. (Volker - DONE)
- Short-term mobile hack -toggle open and close of left navigation to support mobile. (Volker)
- Longer term mobile layout.
- Input/improvements popout hooked up to CBugg (Dustin)
- Parser/conversions from SDK comments to Markdown (Sergey Ruby and C)
- Anything else you can think of to make this a great user and authoring experience.
- Make repo public, or at minimum add support as contributors.
- Provide longer pages with jump links to subsections

How to Contribute Code
======================

1. Fork it and clone (`git clone git@github.com:USERNAME/punch_stuff.git`)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

How to Run Locally
==================

1. Make sure you have `npm` installed on your [node.js][1]
2. Install punch (`sudo npm install -g punch`)
3. Start punch server (`punch server`)
4. Go to http://localhost:9009/

How to Contribute Content
=========================

- For general content, be aware of this site structure: 

>  |-contents
    |---_archives
    |---_dev_guide
    |---_index
    |---_java
    |---_ruby
      |---_ruby11
    |---_server_guide

  At this level, the latest, current major point version of the doc exists. For earlier versions, create a 
  subfolder underneath the guide, for instance _ruby11.
  
- For images, Punch requires that they be in templates/images. So use a subfolder in the directory that corresponds to your guide.

- Experimental features/Labs, other items that have not yet been released:

    - For your first paragraph, add the class .labs: `<p class="lab"></p>`

    - Add the text to the paragraph:

    "{Description of your feature here, what someone can use it for, benefits of this feature, potential use cases for the feature.} Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. This feature is experimental and is not meant for use in production systems. Be aware that you are using it at your own risk. We expect to release the final version of this feature in X.X of Y."

    [1]: http://nodejs.org/download/
    
Proposed Framework
=================

http://docs.scalabl3.com/
