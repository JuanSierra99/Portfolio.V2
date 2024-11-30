<script>
    export let src;
    export let alt;
    export let title;
    export let text = "";
    export let classProp = ""
  </script>
  
  <div class="card flex {classProp}">
    <div class="popup-text"><p>{text}</p></div>
    <img {src} {alt} {title} loading="lazy"/>
  </div>
  
  <style>
    .card {
      display: block;
      height: auto;
      width: 100%;
      position: relative;
      overflow: hidden;
      transition: scale 0.2s linear;
    }
  
    img {
      width: 100%;
      height: auto;
    }
  
    .popup-text {
      position: absolute;
      align-content: center;
      z-index: 1;
      width: 100%;
      height: 100%;
      text-align: center;
      transition:
        transform 0.4s ease-in,
        opacity 0.3s ease-in;
      transform: translateY(100%);
      opacity: 0;
      background-color: rgb(155, 3, 5);
      color: wheat;
      padding: 25px;
      font-size: 1.2rem;
      font-weight: bold;
      font-family: Author;
      box-sizing: border-box;
    }
  
    .card:hover .popup-text {
      transform: translateY(0);
      opacity: 1;
    }
  </style>
  