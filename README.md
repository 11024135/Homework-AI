# AI DeepFack 南華大學
* 換臉AI

## 入門指南
* 此為入門換臉AI
  * 準備資料
  * 使用教學

## 準備資料
* 可以使用Google Colab的帳號
* shape_predictor_68_face_landmarks.dat //AI換臉模組
* FaceFake.ipynb
* Source image //自行準備至少兩張，本教學以image1當作換臉照片，image2當作被換臉照片

## 使用教學
* 第一步 創建Google雲端資料夾
  * 把FaceFake.ipynb跟shape_predictor_68_face_landmarks.dat放在同一個雲端資料夾
  * 兩張照片也放入換臉照命名為Img1，被換臉命名為Img2
* 第二步 掛載雲端硬碟
  * 按照 FaceFake.ipynb 的程序一步一步來
  * 掛載雲端硬碟
 `from google.colab import drive
 drive.mount('/content/drive')`
* 第三步 修改程式碼雲端硬碟位置
  * 用Colab開啟FaceFake.ipynb
  * 修改位置
 `model = "/content/drive/MyDrive/創建資料夾名稱/shape_predictor_68_face_landmarks.dat"`
  * 換臉照片Img1
 `image1 = cv2.imread('/content/drive/MyDrive/創建資料夾名稱/im1.jpg')  #換臉照片
 drive.m`
  * 被換臉照片Img2
 `image2 = cv2.imread('/content/drive/MyDrive/創建資料夾名稱/im2.jpg')  #被換臉照片
 drive.m1`
  * 被換臉照片Img1,Img2
` image1 = cv2.imread('/content/drive/MyDrive/創建資料夾名稱/im1.jpg')
 image2 = cv2.imread('/content/drive/MyDrive/創建資料夾名稱/im2.jpg')`
* 第四步 參數修改
  * COLOUR_CORRECT_BLUR_FRAC:此參數是將兩張圖片的顏色進行矯正，此數值越高的話兩張圖像合成的顏色差異會越明顯，越低會使合成的顏色更加接近，通常介於1~0.1
  * FEATHER_AMOUNT:此參數可以將兩張圖片合成的邊緣進行霧化處理，數值將決定邊緣進行霧化的像素數量，通常介於15~5
* 第五步 程式碼執行
  * 由上到下按照順續執行Colab程式碼即可完成
## 注意事項
* 資料夾名不要使用中文
* 為學術用途使用，請勿販賣
