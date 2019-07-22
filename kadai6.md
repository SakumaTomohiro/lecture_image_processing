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

この画像を二値画像化する。

まず128による二値化を行う。

IMG = ORG>128; % 128による二値化

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/06md128.jpg) 

図3　128による二値画像

次にディザ法による二値化を行う。

IMG = dither(ORG); % ディザ法による二値化

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/06mddiza.jpg) 

図3　ディザ法による二値画像
