# 블러이미지 생성하기

Next.js의 로드되는 중에 placeholder로 보여줄 블러이미지를 생성하는 코드입니다.

블러이미지 외에도 [generate a solid color Data URL ](https://png-pixel.com/) 를 통해 색상이미지를 생성할 수 있습니다. 

### 1. sharp 설치
```yarn add sharp```

### 2. bulr.js 코드 생성
```
const fs = require("fs");
const sharp = require("sharp");

(async () => {
  const buffer = await sharp("public/sbiz/bodydotfitness-enlarged.webp").resize(32).blur(2).toBuffer();
  const base64 = buffer.toString("base64");
  console.log(`data:image/webp;base64,${base64}`);
})();
```

### 3. 코드 실행
```node ./blur.js```

### 4. 결과물
터미널콘솔에 나온 Base64로 인코딩된 이미지 URL를 복사해서 blurDataURL 속성 값에 추가합니다.

```
<Image
  src="/images/large-image.jpg"
  alt="Large image"
  width={1200}
  height={800}
  placeholder="blur"
  blurDataURL="data:image/jpeg;base64,/9j/4AAQSkZJRg..." // base64 이미지
/>
```


**참고**

[Next.js placeholder](https://nextjs.org/docs/app/api-reference/components/image#placeholder)

[Next.js Image dataUrl](https://nextjs.org/docs/app/api-reference/components/image#blurdataurl)
