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

この画像の画素の濃度ヒストグラムを生成する。

imhist(ORG); % ヒストグラムの表示

![原画像](https://github.com/SakumaTomohiro/lecture_image_processing/blob/master/image/04histgram.jpg) 

図3　画素の濃度ヒストグラム
