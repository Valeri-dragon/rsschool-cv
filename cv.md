#Terebilova Valeria
Junior Developer of the external interface
Contact information:
Phone: +375 29 676 02 06
Email address: valeriya.terebilova@gmail.com
Telegram: @Valeridragon
##Briefly About Yourself:
In 2019, she started creating turbo pages for clients' websites through the freelance exchange. There was an interest in web technologies and in February 2020 I enrolled in retraining courses at the BSU Institute of Business in the specialty "Web designer programmer" In September 2021 I defended the qualification work within which the resource was created https://workal.ru /. At the moment, I am developing in front-end development and diving into the study of javascript.

I am interested in web development because this profession provides endless opportunities for professional growth,
in addition, there are a huge number of free high-quality resources for self-education and a large community of developers.

I believe that my ability to learn and acquire new skills will help me go this way and become an experienced interface developer
##Skills and mastery:
HTML5, CSS3
JavaScript Basics
GIT, GitHub
VS Code, PhP, MySQL
Adobe Photoshop, CorelDraw, Autodesk 3ds Max, Adobe Animate
Deployment of sites on cms Wordpress and joomla
##Code

```const search = () => {
const inputSearch = document.querySelector(".search-block > input");
const btnSearch = document.querySelector(".search-block > button");

const renderGoods = (goods) => {

 const containerCard = document.querySelector(".long-goods-list");
 containerCard.innerHTML = "";

 goods.forEach((good) => {


   const {
     category,
     description,
     gender,
     id,
     img,
     label,
     name,
     offer,
     price,
   } = good;
   const goodBlock = document.createElement("div");
   goodBlock.classList.add("col-lg-3");
   goodBlock.classList.add("col-sm-6");

   goodBlock.innerHTML = `

   <div class="goods-card">

           <span class="label ${label ? null : "d-none"}">${label}</span>
           <img src="db/${img}"  alt="${name}" class="goods-image"/>
           <h3 class="goods-title">${name}</h3>
           <p class="goods-description">${description}</p>
          <button class="button goods-card-btn add-to-cart" data-id="${id}">
           <span class="button-price">$${price}</span>
           </button>
         </div>

   `;
   containerCard.append(goodBlock);
 });
};

const responseServer = (value) => {
 fetch("https://willberries-shop-default-rtdb.firebaseio.com/db.json")
   .then((response) => {
     return response.json();
   })
   .then((data) => {

     const array = data.filter((item) =>
       item.name.toLowerCase().includes(value.toLowerCase())
     );


     localStorage.setItem("goods", JSON.stringify(array));

     if (window.location.pathname !== "/goods.html") {
       window.location.href = "/goods.html";
     } else {
       renderGoods(array);
     }
   });
};
try {
 btnSearch.addEventListener("click", () => {
   console.log();
   responseServer(inputSearch.value);
 });
} catch (e) {}
};search()
```

##Examples of my work
Page layout https://cosmedi.ru/peresadka-volos-v-turtsii.html . Creating a website https://workal.ru / , https://websvyaz.ru / , http://aktivprof.ru / , creating a page https://maverick.by/viza-shengen / and block programming https://maverick.by/viza-shengen/#documents Projects on github.com:

*1) Promote AUDI Q3 Sportback as part of the course work on animation https://valeri-dragon.github.io/Audi-promo/
*2) Layout of the food delivery website https://valeri-dragon.github.io/food_project/ 3) Layout of the website for choosing booking seats in the cinema https://valeri-dragon.github.io/cinema-project/

*4)page layout and functional programming: floor selection https://valeri-dragon.github.io/Residential-complex/
*5)Promo page of Mercedes-200 car https://valeri-dragon.github.io/mers-200/
*6)programming of the wildberries store https://valeri-dragon.github.io/wildberries/
*7)programming of search, filter, basket https://valeri-dragon.github.io/ozon/
