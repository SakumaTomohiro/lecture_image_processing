
標準画像「gekirea_daihyo-880x585」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

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

ここから閾値を4パターン設定し、閾値処理した画像を表示する。

IMG = ORG>64; % 輝度値が64以上の画素を1，その他を0に変換

この処理から得られる画像を図３に示す．

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/03md01.jpg)  
図３　閾値を64とした場合

続いて閾値を96とする。

IMG = ORG > 96;

この処理から得られる画像を図４に示す

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/03md02.jpg)  

図４ 閾値を96とした場合

続いて閾値を128とする。

IMG = ORG > 128;

この処理から得られる画像を図５に示す。

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/03md03.jpg)  

図５ 閾値を128とした場合

続いて閾値を192とする。

IMG = ORG > 192;


この処理から得られる画像を図６に示す。

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/03md04.jpg) 

図６ 閾値を192とした場合
