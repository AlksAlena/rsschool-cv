# Alyona Eley
## Frontend developer
![free avatar from photo stock](https://cdn.pixabay.com/photo/2016/04/26/07/57/woman-1353825_960_720.png)

### My motto
> My dear, here we must run as fast as we can, just to stay in place.  
> And if you wish to go anywhere you must run twice as fast as that  
> **― Lewis Carroll, Alice in Wonderland**

### Hard skills
| Skills | Level |
|:---- | :----: |
| HTML/HTML5 | 4/5 |
| CSS/CSS3 | 4/5 |
| JS/TS | 4/5 |
| Angular | 4/5 |
| RESTful | 3/5 |
| Swagger | 3/5 |
| Git | 3/5 |
| Docker | 3/5 |
| English | A1 |

### Soft skills
* Communicability
* Responsibility
* Attention to detail
* Ability for independent work and learning

### Education
- [x] NSTU - Novosibirsk State Technical University
- [x] Coursera.org: HTML, CSS, JS, Angular, Bootstrap courses
- [ ] RS school

### Projects
* [Emodji Game](https://github.com/AlksAlena/frontend_specialization/tree/master/Capstone%20project)
* [ConFusion App](https://github.com/AlksAlena/fullstack_specialization/tree/master/angular%20practice/conFusion)
* [Purr - simple analogue of Trello](https://github.com/AlksAlena/purr)

### Code
```
function Game(desk, timer, popup) {
    this.desk = desk;
    this.cardsList = [];
    this.timer = timer;
    this.popup = popup;
    this.isWin = false;
    this.init =  function(emodji) {
      var setEmodji = emodji.concat(emodji); // 12 icons
      var cards = this.desk.querySelectorAll('.card_container');
      for (var i = 0; i < cards.length; i++) {
        var icon = this.setContent(setEmodji);
        this.cardsList[i] = new Card(cards[i], i, icon);
      }
    };
    this.setContent = function(setEmodji) {
      var randomNumber = Math.floor(Math.random() * 10000) % setEmodji.length;
      var icon = setEmodji.splice(randomNumber, 1)[0];
      return icon;
    };
    this.togglePopup = function(result) {
      var message = '', text = '';
      this.popup.classList.toggle('active');
      if (result) {
        text = 'Win';
        for (var i = 0; i < 3; i++) {
          message += '<span class="message-win">' + text[i] + '</span>';
        }
      } else {
        text = 'Lose';
        for (var i = 0; i < 4; i++) {
          message += '<span class="message-lose">' + text[i] + '</span>';
        }
      }
      this.popup.firstElementChild.firstElementChild.innerHTML = message;
    };
    this.rePlay = function(emodji) {
      this.togglePopup();
      this.isWin = false;
      this.timer.innerHTML = '01:00';
      this.cardsList.forEach(function(item) {
        var card = item.elem.lastElementChild;
        if (item.isOpen) item.rotate();
        if (card.classList.contains('unequal')) card.classList.remove('unequal');
        if (card.classList.contains('equal')) card.classList.remove('equal');
      });
      this.cardsList = [];
      this.init(emodji);
    }
  }
```

### Contacts
* [LinkedIn](https://www.linkedin.com/)
* <fake@example.com>
* [GitHub](github.com/alksalena)