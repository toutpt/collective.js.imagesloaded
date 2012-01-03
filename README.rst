Introduction
============

Image loaded is needed by many jquery plugins like masonry (related to layout)

This addon register the most used script to achieve this need::

    $.fn.imagesLoaded = function(callback){
      var elems = this.filter('img'),
          len   = elems.length;
          
      elems.bind('load',function(){
          if (--len <= 0){ callback.call(elems,this); }
      }).each(function(){
         // cached images don't fire load sometimes, so we reset src.
         if (this.complete || this.complete === undefined){
            var src = this.src;
            // webkit hack from http://groups.google.com/group/jquery-dev/browse_thread/thread/eee6ab7b2da50e1f
            // data uri bypasses webkit log warning (thx doug jones)
            this.src = "data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///ywAAAAAAQABAAACAUwAOw==";
            this.src = src;
         }  
      });
      return this;
    };

