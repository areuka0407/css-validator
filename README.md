# css-validator
[CSS] &lt;input> 태그 - 정규표현식을 통한 검사 예제

----

#### CSS에서 정규표헌식을 사용하는 방법
<br>
결론부터 말하자면 CSS로 '정규표현식'을 통해 input 내에 value 값을 검사할 수는 없습니다.
하지만, HTML이 검사한 결과가 옳고 그른지에 대한 것은 알 수 있습니다.
<br><br>
기본적으로 HTML내의 input 태그는 값의 유효성을 체크하기 위한 속성을 몇가지 갖고 있습니다.
<br><br>

<pre>
<code>
 min(minlength)
 max(maxlength)
 required
 type
 .
 .
 .
</code>
</pre>

예를 들어 input에서 [minlength='5']를 설정하면 사용자가 텍스트를 5자 이상 입력하지 않으면 submit 시 경고창을 띄우며 이벤트를 막습니다. 
또한, input[type='email']을 설정하면 간단한 이메일 형식 체크를 제공하며 형식과 맞지 않으면 마찬가지로 submit이 불가합니다.
<br><br>
CSS는 이러한 HTML의 유효성 체크가 이루어지고 있는지 확인하는 selector가 존재합니다.
<br><br>
<pre>
<code>
input:valid
input:invalid
</code>
</pre>
<br><br>
valid는 유효성 체크가 성공한 input만을 선택할 수 있고, invalid는 반대로 유효성 체크가 실패했을 때의 스타일을
설정할 수 있습니다. 이를 통해 다음과 같이 스타일을 설정하면 input이 유효한 형식이 아닐 때 붉은색 테두리를 갖게 되고,
체크가 성공하면 초록색 테두리를 갖게 될 것입니다.
<br><br>

#### CSS
<pre>
<code>
input:valid {
  border: 3px solid green;
}
input:invalid 
  border: 3px solid blue;
}
  
</code>
</pre>
