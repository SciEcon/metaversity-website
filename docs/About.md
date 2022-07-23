# About Us

## Our Team

<div class="grid-container">
    <figure><img class="origin-img" id="luyao"
            src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/luyao.jpg"width="200" />
        <figurecaption>Prof. Luyao Zhang</figurecaption>
    </figure>
    <figure><img class="origin-img" id="yulin"
            src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/yulin.jpg"width="200" />
        <figurecaption>Prof. Yulin Liu</figurecaption>
    </figure>
    <figure><img class="origin-img" id="xinyu"
            src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/xinyu.jpg"width="200" />
        <figurecaption>Xinyu Tian</figurecaption>
    </figure>
    <figure><img class="origin-img" id="zesen"
            src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/zesen.jpg"width="200" />
        <figurecaption>Zesen Zhuang</figurecaption>
    </figure>
</div>

<!-- Modals -->
<div id="luyao-modal" class="modal">

  <!-- The Close Button -->

  <!-- Modal Content (The Image) -->
  <img class="modal-content" id="luyao-modal-img">
  <span class="close">&times;</span>
</div>
<!-- Modals -->
<div id="yulin-modal" class="modal">

  <!-- The Close Button -->

  <!-- Modal Content (The Image) -->
  <img class="modal-content" id="yulin-modal-img">
  <span class="close">&times;</span>
</div>
<!-- Modals -->
<div id="xinyu-modal" class="modal">

  <!-- The Close Button -->

  <!-- Modal Content (The Image) -->
  <img class="modal-content" id="xinyu-modal-img">
</div>

<!-- Modals -->
  <span class="close">&times;</span>
<div id="zesen-modal" class="modal">

  <!-- The Close Button -->

  <!-- Modal Content (The Image) -->
  <img class="modal-content" id="zesen-modal-img">
  <span class="close">&times;</span>
</div>

<style>
.grid-container {
  display: grid; 
  grid-template-columns: 1fr 1fr 1fr 1fr; 
  grid-template-rows: 1fr; 
  gap: 20px 20px; 
  grid-template-areas: 
    ". . . ."
}

.grid-image {
  object-fit: cover;
  width: 200px;
  height: 200px;
}

/* Style the Image Used to Trigger the Modal */
.origin-img {
  border-radius: 20px;
  cursor: pointer;
  transition: 0.3s;
}

.origin-img:hover {opacity: 0.7;}

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

/* Modal Content (Image) */
.modal-content {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
}

/* Caption of Modal Image (Image Text) - Same Width as the Image */
#caption {
  margin: auto;
  display: block;
  width: 80%;
  max-width: 700px;
  text-align: center;
  color: #ccc;
  padding: 10px 0;
  height: 150px;
}

/* Add Animation - Zoom in the Modal */
.modal-content, #caption {
  animation-name: zoom;
  animation-duration: 0.6s;
  width: 600px;
  height: 600px;
}

@keyframes zoom {
  from {transform:scale(0)}
  to {transform:scale(1)}
}

/* The Close Button */
.close {
  /* position: absolute; */
  /* top: 15px;
  right: 35px; */
  margin: auto;
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

/* 100% Image Width on Smaller Screens */
@media only screen and (max-width: 700px){
  .modal-content {
    width: 100%;
  }
}
</style> 

<script>
let modalNames = ['luyao-modal', 'yulin-modal', 'xinyu-modal', 'zesen-modal'];

let modalImgNames = ['luyao-modal-img', 'yulin-modal-img', 'xinyu-modal-img', 'zesen-modal-img'];

let nftLinks = [
    'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/小篆_道_Luyao%20Zhang.png',
    'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/楷体_明_Yulin%20Liu.png',
    'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/隶书_宇_Michelle%20Tian.png',
    'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/隶书_和_Tianyu%20Wu.png',
    'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/小篆_福_Zesen%20Zhuang.png'
]

let imgNames = ['luyao', 'yulin', 'xinyu', 'zesen'];

// var images = [];
// function preload() {
//     for (var i = 0; i < arguments.length; i++) {
//         images[i] = new Image();
//         images[i].src = preload.arguments[i];
//         console.log(images[i]);
//     }
// }

// //-- usage --//
// preload(
//     'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/小篆_道_Luyao%20Zhang.png',
//     'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/楷体_明_Yulin%20Liu.png',
//     'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/隶书_宇_Michelle%20Tian.png',
//     'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/隶书_和_Tianyu%20Wu.png',
//     'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/小篆_福_Zesen%20Zhuang.png'
// )

for (let i = 0; i < 4; i++) {
    var modal = document.getElementById(modalNames[i]);
    var img = document.getElementById(imgNames[i]);
    var modalImg = document.getElementById(modalImgNames[i]);
    img.onclick = function(){
        modal.style.display = "flex";
        modal.style.flexDirection = "column";
        modalImg.src = nftLinks[i];
    }

    // Get the <span> element that closes the modal
    var span = document.getElementsByClassName("close");
    for (let i = 0; i < 4; i++)
    {
        span[i].onclick = function() {
        modal.style.display = "none";
        }
    }

    // When the user clicks on <span> (x), close the modal
    
}
</script>


---

<div style="display: flex;" markdown>
<img id="luyao" src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/luyao.jpg" onmouseover="luyaoHover();" onmouseout="luyaoOffHover();" width="200" />
<script>
let luyaoOffHover = () => {
    document.getElementById('luyao').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/luyao.jpg');
};

let luyaoHover = () => {
    document.getElementById('luyao').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/小篆_道_Luyao%20Zhang.png');
};
</script>

<div style="width: 5%">
</div>
<div markdown style="width: 70%;">
**Name**: Luyao Zhang | 张露瑶

**Title**: Founding President (Academia Primary, Industry Secondary)

**LinkedIn**: [https://www.linkedin.com/in/sunshineluyao/](https://www.linkedin.com/in/sunshineluyao/)

**Personal Website**: [http://scholars.duke.edu/person/luyao.zhang](http://scholars.duke.edu/person/luyao.zhang)

**Twitter**: [https://twitter.com/sunshineluyao](https://twitter.com/sunshineluyao)

**Facebook**: [https://www.facebook.com/sunshinestar11](https://www.facebook.com/sunshinestar11)

!!! quote "Motto in light of eastern and western philosophy"
    Dao dejing:The Dao produced One; One produced Two; Two produced Three; Three produced All things.

    道德經: 道生一，一生二，二生三，三生萬物。


    Spinoza: Passion without reason is blind; Reason without passion is dead.

    斯宾诺莎: 天人合一，道法自然

</div>
</div>

---
<div style="display: flex;" markdown>
<img id="yulin" src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/yulin.jpg" onmouseover="yulinHover();" onmouseout="yulinOffHover();" width="200" />
<script>
let yulinOffHover = () => {
    document.getElementById('yulin').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/yulin.jpg');
};

let yulinHover = () => {
    document.getElementById('yulin').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/楷体_明_Yulin%20Liu.png');
};
</script>
<div style="width: 5%">
</div>
<div markdown style="width: 70%;">
**Name**: Yulin Liu | 刘玉林

**Title**: Founding President (Industry Primary, Academia Secondary)

**LinkedIn**: [https://www.linkedin.com/in/yulineth/](https://www.linkedin.com/in/yulineth/)

**Twitter**: [https://twitter.com/YulinLiu20](https://twitter.com/YulinLiu20)

**Personal Website**: [https://www.yulinliu.me/](https://www.yulinliu.me/)

!!! quote "Motto in light of eastern and western philosophy"
    Brightness derives from day’s and night’s deduction.

    日月相推而明生焉

</div>
</div>

---

<div style="display: flex;" markdown>
<img id="xinyu" src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/xinyu.jpg" onmouseover="xinyuHover();" onmouseout="xinyuOffHover();" width="200" />
<script>
let xinyuOffHover = () => {
    document.getElementById('xinyu').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/xinyu.jpg');
};

let xinyuHover = () => {
    document.getElementById('xinyu').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/隶书_宇_Michelle%20Tian.png');
};
</script>
<div style="width: 5%">
</div>
<div markdown style="width: 70%;">
**Name**: Xinyu Tian | 田馨宇

**Title**: Interim Chair of Communication

**LinkedIn**: [https://www.linkedin.com/in/xinyu-tian-1777aa203/](https://www.linkedin.com/in/xinyu-tian-1777aa203/)

!!! quote "Motto in light of eastern and western philosophy"
    读万卷书，行万里路。

    Read more, travel more.

</div>
</div>

---
<div style="display: flex;" markdown>
<img id="zesen" src="https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/zesen.jpg" onmouseover="zesenHover();" onmouseout="zesenOffHover();" width="200" />
<script>
let zesenOffHover = () => {
    document.getElementById('zesen').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/people_thumbnail/zesen.jpg');
};

let zesenHover = () => {
    document.getElementById('zesen').setAttribute('src', 'https://raw.githubusercontent.com/SciEcon/SciEcon-Website/main/docs/nft/小篆_福_Zesen%20Zhuang.png');
};
</script>
<div style="width: 5%">
</div>
<div markdown style="width: 70%;">
**Name**: Zesen Zhuang | 庄泽森

**Title**: Interim Chair of Technology Development

**LinkedIn**: [https://www.linkedin.com/in/zesen-zhuang-624591217/](https://www.linkedin.com/in/zesen-zhuang-624591217/)

**Personal Website**: [https://www.crinstaniev.com](https://www.crinstaniev.com)

!!! quote "Motto in light of eastern and western philosophy"
    Preserve your dignity as a nobody; promote the social wellfare as a somebody.

    穷则独善其身，达则兼济天下
</div>
</div>

## About SciEcon

<figure markdown>
![logo](assets/logo-light-mode-v1.png){ width="150" }
</figure>

SciEcon CIC is an NPO registered in the UK. SciEcon exists to:

- Cultivate an integrated talent of researcher, engineer, entrepreneur, investor, philanthropist, and beyond
- Nurture leadership through focusing on interdisciplinary research, the interplay between teaching, research, and practice, and conversation between intellectuals
- Host educational events such as interdisciplinary seminars, symposiums, conferences for a hub of global students, researchers, scholars, practitioners, and beyond

Join our community on multiple platforms to partake in and contribute to intellectual conversation ever since and ever after:

- [x] LinkedIn: <https://www.linkedin.com/company/sciecon-cic>
- [x] Twitter: <https://twitter.com/SciEcon_CIC>
- [x] YouTube: <https://www.youtube.com/channel/UCQOvF-D45s09FlajFkKzoOA>
- [x] Github: <https://github.com/SciEcon>
- [x] Facebook: <https://www.facebook.com/sciecon2022>
- [x] Medium: <https://sciecon.medium.com>
    - [x] SciEcon-Research:　<https://medium.com/sciecon-research>
    - [x] SciEcon-Innovate:　<https://medium.com/sciecon-innovate>
    - [x] SciEcon-AMA: <https://medium.com/sciecon-ama>
- [x] WeChat (ID): SciEcon

<figure markdown>
  ![Image title](assets/WeChat30cm.jpg){ width="300" }
  <figcaption>SciEcon WeChat QR Code</figcaption>
</figure>

- [x] **Subscribe to our news letters** by joining our Google Group: 
<https://groups.google.com/forum/#!forum/sciecon-community/join>