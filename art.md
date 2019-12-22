---
layout: page
title: Art
permalink: /art/
---

<style>

#myImg {
  border-radius: 5px;
  cursor: pointer;
  transition: 0.3s;
}

#myImg:hover {opacity: 0.7;}

/* The Modal (background) */
.modal {
  display: none; /* Hidden by default */
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  padding-top: 100px; /* Location of the box */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.9); /* Black w/ opacity */
}

/* Modal Content (image) */
.modal-content {
  margin: auto;
  display: block;
  width: auto;
  height: auto;
  max-width: 700px;
  max-height: 600px;
}

/* Add Animation */
.modal-content, #caption {  
  -webkit-animation-name: zoom;
  -webkit-animation-duration: 0.6s;
  animation-name: zoom;
  animation-duration: 0.6s;
}

@-webkit-keyframes zoom {
  from {-webkit-transform:scale(0)} 
  to {-webkit-transform:scale(1)}
}

@keyframes zoom {
  from {transform:scale(0)} 
  to {transform:scale(1)}
}

/* The Close Button */
.close {
  position: absolute;
  top: 15px;
  right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  transition: 0.3s;
}

.close:hover,
.close:focus {
  color: #bbb;
  text-decoration: none;
  cursor: pointer;
}

// 100% Image Width on Smaller Screens 
@media only screen and (max-width: 700px;){
  .modal-content {
    width: auto;
  }
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
}

.header {
  text-align: center;
  padding: 32px;
}

.row {
  display: -ms-flexbox; /* IE10 */
  display: flex;
  -ms-flex-wrap: wrap; /* IE10 */
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create four equal columns that sits next to each other */
.column {
  -ms-flex: 25%; /* IE10 */
  flex: 25%;
  max-width: 25%;
  padding: 0 4px;
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
}

/* Responsive layout - makes a two column-layout instead of four columns */
@media screen and (max-width: 800px) {
  .column {
    -ms-flex: 50%;
    flex: 50%;
    max-width: 50%;
  }
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    -ms-flex: 100%;
    flex: 100%;
    max-width: 100%;
  }
}

canvas {
    box-shadow: inset 0 0 1px 0 rgba(0, 0, 0, 0.2);
    height: 320px;
    width: 320px;
    background-size: cover;
    background-position: center center;
}

button {
    position: absolute;
    top:275px;
    left:425px;
    cursor: pointer;
}

button:hover {
  background-color: darkgrey;
}
</style>

## Generative Art

Piet-Mondrian
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
<canvas id="mondrian-canvas"></canvas>
<button id="mondrian-refresh" class="btn"><i style="font-size:18px" class="fa fa-refresh"></i></button>
<script src="../assets/js/mondrian.js"></script>

## Amaziograph

<div class="row"> 
  <div class="column">
    <img src="../assets/images/amaziograph1.jpeg" class="myImages" id="myImg" style="width:100%">
    <img src="../assets/images/amaziograph5.jpeg" class="myImages" id="myImg" style="width:100%">
  </div>
  <div class="column">
    <img src="../assets/images/amaziograph2.jpeg" class="myImages" id="myImg" style="width:100%">
    <img src="../assets/images/amaziograph6.jpeg" class="myImages" id="myImg" style="width:100%">
  </div>
  <div class="column">
    <img src="../assets/images/amaziograph3.jpeg" class="myImages" id="myImg" style="width:100%">
    <img src="../assets/images/amaziograph7.jpeg" class="myImages" id="myImg" style="width:100%">
  </div>
  <div class="column">
    <img src="../assets/images/amaziograph4.jpeg" class="myImages" id="myImg" style="width:100%">
    <img src="../assets/images/amaziograph8.jpeg" class="myImages" id="myImg" style="width:100%">
  </div>
</div>

<div id="myModal" class="modal">
  <span class="close">&times;</span>
  <img class="modal-content" id="img01">
  <!-- <div id="caption"></div> -->
</div>

<script src="https://code.jquery.com/jquery-3.4.1.min.js" integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo=" crossorigin="anonymous"></script>
<script>
var modal = document.getElementById("myModal");
var images = document.getElementsByClassName("myImages");
var modalImg = document.getElementById("img01");

var showModal = function(){
    modal.style.display = "block";
    modalImg.src = this.src;
};

for (var i = 0; i < images.length; i++) {
    images[i].addEventListener('click', showModal);
}

var span = document.getElementsByClassName("close")[0];

span.onclick = function() {
  modal.style.display = "none";
};

$("#mondrian-refresh").click(function() {
    $("#mondrian-canvas").load(window.location.href);
  }); 
</script>

