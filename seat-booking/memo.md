## Js    
* ``` js
    // 해당하는 요소가 객체로 반환
    const seats = document.querySelectorAll('.row .seat:not(.occupied)');
    const selectedSeats = document.querySelectorAll('.row .seat.selected');
  
    // 전개구문으로 배열에 담아 map, indexOf를 사용
    const seatsIndex = [...selectedSeats].map(seat => [...seats].indexOf(seat));
    console.log(typeof seats); // object
    ```
  
* ``` js
    const seats = document.querySelectorAll('.row .seat:not(.occupied)');
  ```
  
* ``` js
    if (
      e.target.classList.contains('seat') &&
      !e.target.classList.contains('occupied')
    ) {
      e.target.classList.toggle('selected');
    }
    ```
  
## HTML/CSS
* CSS 접두어, 크로스 브라우징을 위함   
    * -webkit- : 구글, 사파리
    * -moz- : 파이어폭스
    * -ms- : 익스플로러(보통 생략)
    * -o- : 오페라

* perspective, transform으로 투영점∙원근감 표현
    ``` css
    .container {
      perspective: 1000px;
    }
  
    .screen {
      background-color: #fff;
      height: 70px;
      width: 100%;
      margin: 15px 0;
      transform: rotateX(-45deg);
      box-shadow: 0 3px 10px rgba(255, 255, 255, 0.7);
    }
    ```
* 확대
    ``` css
    .seat:not(.occupied):hover {
      cursor: pointer;
      transform: scale(1.2);
    }
    ```
