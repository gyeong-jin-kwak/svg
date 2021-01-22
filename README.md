# SVG
* 벡터 기반

## HTML 문서에 SVG를 넣는 여러가지 방법
* `<img>`
* css `background`
* svg 요소들 inline 으로 삽입
* `<object>`

## SVG 파일 크기
* 스타일은 절대적으로 보여지는 크기
* `viewBox`는 상대적으로 보여지는 크기 
* 스타일을 설정하지 않고 `viewBox` 만 설정시 반응형처럼 크기 조절이 됨
```
svg {
    width: 500px;
    height: 500px
}

<svg viewBox="0 0 1000 1000">
    <rect x="0" y="0" width="1000" height="1000">
    </rect>
</svg>
```

## SVG 압축
* 'svgomg' 검색
* [svg 압축](https://jakearchibald.github.io/svgomg/)
* 'paste markup' 에 코드 붙혀넣기
* 'copy as text' 혹은 파일 다운로드 사용

## SVG Style, Script 를 SVG 태그 안으로
* 스타일을 `<svg></svg>` 태그 안으로 넣을 수 있음
* 장점: svg 단독으로 사용할 수 있음
* 안전장치 `<![CDATA[` `]]>` : 파서에서 오류나는 것을 방지
```
<style>
<!-- <![CDATA[ -->
    .face {
        position: absolute;
        top: 0;
        right: 0;
        left: 0;
        bottom: 0;
        margin: auto;
        width: 200px;
    }

    .face__hair {
        fill: blueviolet;
    }
<!-- ]]> -->
</style>
```

## SVG Option
* fill : 색을 채울 때 