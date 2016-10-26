### Profile card

Here is an example of a profile card

```html
<h1>This requires bootstrap</h1>
<div class="my-card">
  <div class="">
    <div="row my-row">
      <div class="profile col-md-3 aligncenter">
        <div class="wrap-avatar">
          <img src="http://placehold.it/150x150" class="img-circle">
        </div>
        <h3 class="">Rahul Raviprasad</h3>
        <p><a href="">View Profile</a></p>
      </div>
      <div class="table-review col-md-8">
        <table class="table">
          <thead>
            <tr>
              <th width="33%"></th>
              <th>Number of Competitions</th>
              <th>Average Score</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>HTML</td>
              <td>
                <div class="">
                  <span class="">36 </span><span>(5 New)</span>
                </div>
              </td>
              <td>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star"></i>
                <i class="glyphicon glyphicon-star"></i>
              </td>
            </tr>
                     <tr>
              <td>OOJS</td>
              <td>
                <div class="">
                  <span class="">3 </span><span>(2 New)</span>
                </div>
              </td>
              <td>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star"></i>
              </td>
            </tr>
                     <tr>
              <td>JAVA</td>
              <td>
                <div class="">
                  <span class="">600 </span><span>(15 New)</span>
                </div>
              </td>
              <td>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star yellow"></i>
                <i class="glyphicon glyphicon-star"></i>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</div>
<h4>This can be used for setting other profile or for products etc</h4>
```
and the css
```css
body {
background:#edeef1;
overflow:hidden;
}

.aligncenter {
text-align: center;
}
.table {
margin-left: 8%;
}

table th {
  color: #999999;
  font-size: .9em;
  border-bottom: none;  
}

.table>tbody>tr>td {
border-top: none;
}

.table>thead>tr>th {
border-bottom: none;
}

.yellow {
color: #ffa500;
}

.my-card {
padding-top: 2em;
margin: 10px;
border-radius: 5px;
background: #fff;
box-shadow: 0 1px 2px rgba(0,0,0,.15);
overflow:hidden;
}

.my-row {
padding: 6em;
}
```
Here is the codepen link: http://codepen.io/RahulRaviprasad/pen/yaAPgN
