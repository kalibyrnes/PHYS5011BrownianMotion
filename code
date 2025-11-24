#include <opencv2/opencv.hpp>
#include <iostream>

using namespace cv;  
using namespace std;   

int main() {

    Mat frame = imread("frame.png");   // this will work on the single file in the repo, will need to change to adjsut to .tiff files

    if (frame.empty()) { // verifies that the image properly loaded
        cerr << "ERROR: Could not load image. Check path.\n";
        return -1;
    }

    Mat gray; // converts the picture to grayscale to easily spot the beads
    cvtColor(frame, gray, COLOR_BGR2GRAY);

    Mat filt; // removes shadows
    Mat kernel = getStructuringElement(MORPH_ELLIPSE, Size(35, 35));
    morphologyEx(gray, filt, MORPH_TOPHAT, kernel);

    Mat binary;
    adaptiveThreshold(
        filt,
        binary,
        255,
        ADAPTIVE_THRESH_GAUSSIAN_C,
        THRESH_BINARY_INV,
        31,   // window size
        2     // subtract constant

    Mat clean; // removes excessive noise
    Mat smallKernel = getStructuringElement(MORPH_ELLIPSE, Size(3, 3));
    morphologyEx(binary, clean, MORPH_OPEN, smallKernel);

    //show images to debug if needed
    imshow("Original", frame);
    imshow("Grayscale", gray);
    imshow("Filtered", filt);
    imshow("Binary Mask", clean);

    imwrite("../data/binary_output.png", clean);

    waitKey(0);
    return 0;
}
