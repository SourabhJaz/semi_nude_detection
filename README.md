An extension to Yahoo's open NSFW model. NSFW model is suitable to classify pornographic/nude images. This project is to add one more layer to NSFW model and classify semi-nude images. To do this skin area exposed in image is used.

Steps to run semi-nude classifier

1. Git clone the semi_nude_detection repo
`git clone https://github.com/SourabhJaz/semi_nude_detection.git`

2. Get docker image of caffe_cv2
`docker pull sourabhjaz/caffe_cv2`

3. Go to semi_nude_detection folder

4. Run the following command to test:
`docker run --volume=$(pwd):/workspace sourabhjaz/caffe_cv2:latest python ./classify_nsfw.py --model_def nsfw_model/deploy.prototxt --pretrained_model nsfw_model/resnet_50_1by2_nsfw.caffemodel YOUR_IMAGE_NAME.JPG`

Replace `YOUR_IMAGE_NAME.JPG` with the image you want to test.
