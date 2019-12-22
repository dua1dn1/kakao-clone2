#### inline, block, inlline-block 태그
###### block : 해당 박스옆에 아무것도 없을때 block라고 함, 블록 옆에 어떤 element도 놓을 수 없음. (block 형태가 default임)
###### inline-block : 박스들이 서로서로 바로 옆에 있을수 있게 해줌.
###### lnline :  박스의 모든 property(속성 값들)을 지움, 박스가아닌 텍스트처럼 적용이됨.
 
#### position 태그
###### static : default 값 
###### fiexd :  고정된 포지션으로 스크롤해도 사라지지않음.
###### relative : 부모태그(absoulte의 포지션을 잡기위해 부모태그로 포지션을 잡음.)
###### absolute : 부모태그(relative) 속성을 보고 이에 상응해서 포지션이 결정됨. 부모태그(relative)가 없을경우 body 태그에 상응하여 포지                     션이 결정됨
#### Element States태그
###### box:hover : 마우스 커서를 해당 박스위에 올려놓을시 hover에 설정된 액션이 나타남. 
###### box:active : 마우스로 클릭했을때 active에 설정된 액션이 나타남.
###### box:focus : 포커스 상태일때(마우스 이벤트상태, input및 textarea 태크에서 기본값상태(입력할 준비가 될 때 커서가 깜빡이는 것) 동안에                    스타일을 지정, focus 더중요하고 마지막 명령이기때문에 hover가 먹히지 않음.

#### flex 태그
###### display : flex :부모태크에만 적용
###### 예시)
```html
<html>
 <head>
  <style>
    .father{
       display : flex; (박스를 인라인 블록 형태로 지정)
       flex-direction: (column : 수직, row : 수평, row-reverse : 수평으로 반대로 출력, column-reverse 수직으로 반대로 출력)
       justify-content:  (flex-direction이 row이 경우 수평, column일 경우 수직으로 적용
                          space-between : 같은간격으로 조정, space-around : 주변까지 같은간격으로 조정, center : 중간으로 이동)
       aligin-items:  (flex-direction이 row이 경우 수직, column일 경우 수평으로 적용, 
                       flex-end : 아래로이동, flex-start : 위로이동, center : 중간으로 이동)
       flex-wrap : (wrap : 그리드가 생성, no-wrap: 밑에 새로운 줄 형성, wrap-reverse : 반대방향으로 그리드 생성)
   }
  </style>
 </head>
 <body>
   <div class = "father">
    <div class = "box">
    <div class = "box">
    <div class = "box">
   </div>
 </body>
</html>
```

#### transitions태그
##### -이동/변경 등을 멋지게 보여주는 효과, focus, active, hover에서 효과적으로 적용됨, 1개이상의 설정값을 바꾸고 싶다면 (transitions            all) 이라고 적으면됨.
###### ease-in-out : 애니매이션

#### transform(transformations)태그
##### - element들을 변경 혹은 모습이 변하는 효과를 뜻함
###### rotate: 회전, scale: 확대, skew: 기울기, translate(이동), perspective : (3d효과, 부모요소에적용)
###### matrix : perspective를 제외한 모든 요소들을 한번에 일괄 적용시킴 

#### Animations태그
##### -keyframes은 css로하여금 애니메이션을 생성했다는것을 알려줌(2가지의 스텝이 필요 (1)from, (2) to)
###### 예시(1)

```html
 <style>
  .classname {
    animation: 1.5s scaleAndRotateSquare ease-in-out; (무한반복을 하고싶다면 infinte이라고 적으면됨)
  }
  /* from-to로 트렌스포메이션이 없는 상태에서 회전1바퀴 및 작아지기*/
   @keyframes scaleAndRotateSquare{
    from{
       trnasfrom:none; 
    }
    to{
       transfrom: rotate(1turn) scale(.5, .5); :
    }
  }
  </style>
```
###### 예시(2)
```html
 <style>
  .classname {
    animation: 1.5s scaleAndRotateSquare ease-in-out; (무한반복을 하고싶다면 infinte이라고 적으면됨)
  }
  /* 0%,50%,100% 로도 할수있음.(2개이상으로 효과를 줄수있음)*/
   @keyframes scaleAndRotateSquare{
    0%{
       trnasfrom:none; 
    }
    50%{
       transfrom: rotate(1turn) scale(.5, .5); :
    }
    100%{
       trnasfrom:none; 
    }
  }
  </style>
```
#### Media Queries
##### -해상도에 맞게 화면을 조정
###### 예시)
```html
   @media screen and (min-width:320px) and (max-width:640px){ /*보이는 화면이 최소값 320, 최대값 640이라는 뜻*/
    body{
       background : blue; (최소값 320, 최대값 640이 되면 배경색이 파란색으로 바뀜) 
    }
   }
```
