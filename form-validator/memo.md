## Js
* trim() 양 끝의 공백 제거한 새로운 문자열
    ``` js
    function checkRequired(inputArr) {
      inputArr.forEach(function(input) {
        if (input.value.trim() === '') {
          showError(input, `${getFiledName(input)} is required.`)
        } else {
          showSuccess(input);
        }
      });
    }
    ```

*  부모 요소로 접근해서 컨트롤
    ``` js
    function showError(input, message) {
      const formControl = input.parentElement;
      formControl.className = 'form-control error';
      const small = formControl.querySelector('small');
      small.innerText = message;
    } 
    ```
   
* 첫 글자 대문자로 변환
    ``` js
      function getFiledName(input) {
        return input.id.charAt(0).toUpperCase() + input.id.slice(1);
      }  
    ```

## HTML/CSS
* 사용자 지정 CSS 속성
    ```css
    :root {
      --succss-color: #2ecc71;
      --error-color: #e74c3c;
    }
    
    .form-control.success input {
      border-color: var(--succss-color);
    }
    .form-control.error input {
      border-color: var(--error-color);
    }
    ```