# Modals

## Pure HTML CSS and JS approach

```HTML
<!DOCTYPE html>
<html>

<head>
  <style>

  .modal-overlay {
    z-index:3;
    display:none;
    padding-top:100px;
    position:fixed;
    left:0;
    top:0;
    width:100%;
    height:100%;
    overflow:auto;
    background-color:rgb(0,0,0);
    background-color:rgba(0,0,0,0.4);
  }
  .modal-content {
    margin:auto;
    background-color:#fff;
    position:relative;
    padding:0;
    outline:0;
    width:600px;
  }
  .close-button {
    position:absolute;
    right:0;
    top:0
  }


  </style>
</head>


<body>

<div class="">
  <button onclick="document.getElementById('modalId').style.display='block'" class="">Open Modal</button>

  <div id="modalId" class="modal-overlay">
    <div class="modal-content">
      <div class="">
        <span onclick="document.getElementById('modalId').style.display='none'" class="close-button">&times;</span>

        <p> Modal content goes here </p>
      </div>
    </div>
  </div>
</div>

</body>
</html>


```


## Jquery Modal

This tutorial helps you build basically the same, but with few jquery functions
http://www.jacklmoore.com/notes/jquery-modal-tutorial/


Similarly this can also be used if jquery is present in your project
https://github.com/kylefox/jquery-modal
