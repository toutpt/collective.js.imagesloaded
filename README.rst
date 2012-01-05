Introduction
============

Register jquery.imagesloaded_ plugin in Plone's resource registry.

version: 1.0.4

About jquery.imagesloaded
=========================

A small jQuery plugin that triggers a callback after all the selected/child 
images have been loaded. Because you can't do `.load()` on cached images.

::

    $('#my-container').imagesLoaded( function( $images ) {
      // callback provides one argument, the jQuery object of child images
      console.log( $images.length + ' images have been loaded in ' + this )
    });

You can call `imagesLoaded` on a set of images as well.

::

    $('.article img').imagesLoaded( myFunction );

Credits
=======

Companies
---------

|makinacom|_

  * `Planet Makina Corpus <http://www.makina-corpus.org>`_
  * `Contact us <mailto:python@makina-corpus.org>`_


Authors

  - JeanMichel FRANCOIS aka toutpt <toutpt@gmail.com>

.. Contributors

.. |makinacom| image:: http://depot.makina-corpus.org/public/logo.gif
.. _makinacom:  http://www.makina-corpus.com
.. _jquery.imagesloaded: http://desandro.github.com/imagesloaded/
