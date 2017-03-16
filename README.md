# Building Your Own JavaScript Modal   

Code repository for the tutorial by [Ken Wheeler](http://kenwheeler.github.io/)

Demo found at: http://codepen.io/kenwheeler/pen/LvGjK/

Extended to: 

##Accept params by data attributes:

    <div id="jsm" data-auto-open="true" data-max-width="80%" data-max-height="false">    
      <a href="..."><img src="..." /></a>
    </div>

##Omit trigger button

    var myContent = document.getElementById('jsm');

    if (myContent !== null)
    {
      var myModal = new Modal({
        content: myContent
      }); 

      var triggerButton = document.getElementById('trigger');

      if (triggerButton !== null)
      {
        triggerButton.addEventListener('click', function() {
          myModal.open();
        });
      }
    }
