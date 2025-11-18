Professor Matthew Smith provided the basis for this code. Please contact him at msmith84@illinoistech.edu for the original code.

This project uses Python 3.12 and requires several libraries to run. Follow the steps below:

1.  Install a stable version of Python (like 3.12) and added to your system's PATH.

2.  Install Libraries: Open your terminal or PowerShell and run the following command:
    ```
    pip install opencv-python numpy matplotlib pandas scipy openpyxl jupyter
    ```

---------How to Run--------

1.  The test video file that Dr. Smith made is already in the `bees` folder.

2.  Open the `beeTracker_backsub.ipynb` file. In the code cells, make sure the `cv.VideoCapture('2024-10-25_1848.mp4')` lines are updated with the name of your video file. Dr. Smith's video file is the default. Then, change all lines of code with file paths to the file path that matches your local directory for the file it references. Right now, they will match mine, but that will not be the same as yours.

3.  In the bees folder (in your file explorer, when you install this project locally), create three empty folders with these exact names:
    *   `beet` (for tracked video frames)
    *   `beet2` (for movement plots)
    *   `results` (for the final output videos and data)
Your bees folder should have 3 folders after this: bees, beet, beet2, results.

4.  Run all cells in the Jupyter Notebook. The script will generate a final video with tracking IDs, a CSV file with telemetry, and a summary statistics .xlsx file. It also should generate a folder called .ipynb_checkpoints, which you can ignore.

-----------Adjustments-------------

For different videos, you may need to change the following parameters at the top of Cell 7:
*   `MIN_BEE_AREA` and `MAX_BEE_AREA` filter out objects that are too small or too large to be a bee.
*   `DISH_DIAMETER_METERS` and `DISH_DIAMETER_PIXELS`
