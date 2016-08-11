#include "opencv2/opencv.hpp"

using namespace cv;

int main(int, char**)
{
	VideoCapture cap(0); // open the default camera
	if (!cap.isOpened())  // check if we succeeded
		return -1;

	Mat image;
	namedWindow("image", 1);

	while (1) {

		cap >> image;
		flip(image, image, 1);
		imshow("image", image);
		waitKey(33);


	}
	
	return 0;
}
