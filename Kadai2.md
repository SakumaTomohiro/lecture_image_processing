標準画像「Lennagekirea_daihyo-880x585」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('Lenna.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/gekirea1.jpg)  
図1 原画像

続いて現画像をグレースケール画像に変換する。

ORG=imread('gekirea_daihyo-880x585.jpg'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;
imagesc(ORG); axis image; % 画像の表示

グレースケールに変換した画像を図2に示す。
![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/gekirea20.jpg) 

図２　グレースケール表示画像

原画像を2階調生成するには、0-255の値を2つに分け、0-128と129-255とする。

IMG = ORG>128; %現画像を2つに分ける

2階調画像をを図３に示す．

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/gekirea2a.jpg)  
図３　2階調画像

同様に原画像を4階調画像にするには，0-255の値を4分割すればよい．すなわち，0-64,65-128,129-192,193-255のようにする。

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

4階調画像を図４に示す．

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/gekirea2b.jpg)  

図４ 4階調画像



8階調画像は

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>96;
IMG3 = ORG>128;
IMG4 = ORG>160;
IMG5 = ORG>192;
IMG6 = ORG>224;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

とすればよい。8階調画像を図５に示す。

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/gekirea2d.jpg)  

図５　8階調画像
