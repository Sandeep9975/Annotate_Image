# Annotate_Image
The above code is a Python script that allows users to annotate an image by adding a subtitle to it. The script uses the OpenCV library to load and manipulate the image and the Pillow library to add text to the image.

The main functions of the code include:

1. `adjust_font_size`: This function dynamically adjusts the font size of the subtitle text to ensure it fits within the image frame while maintaining readability.

2. `annotate_image`: This function takes an input image, a subtitle text, and an output path. It annotates the image by adding the subtitle text at the bottom-center of the image. The text is wrapped to fit within the image frame.

3. `browse_input_image` and `browse_output_path`: These functions handle the file dialog to allow users to select the input image and the output path for the annotated image.

4. `annotate_button_click`: This function is triggered when the "Annotate Image" button is clicked. It reads the input image path, output path, and subtitle text from the corresponding entry fields and calls the `annotate_image` function to generate the annotated image.

The script uses the tkinter library to create a simple graphical user interface (GUI) where users can interact with the application. The GUI provides input fields to select the input image, specify the output path, and enter the subtitle text. Upon clicking the "Annotate Image" button, the annotated image is generated and saved at the specified location.

With this script, users can easily add subtitles to their images and save the modified images with the subtitle positioned at the bottom-center, ensuring a visually appealing result.

Below are the steps for the above code:

1. Import the necessary libraries: `cv2` for image processing, `numpy` for numerical operations, `PIL` for working with images, `tkinter` for GUI, and `textwrap` for wrapping text.

2. Define a function `adjust_font_size` that takes the annotation text, font path, maximum font size, image width, and image height as inputs. This function adjusts the font size to fit the wrapped text within the image frame.

3. Define a function `annotate_image` that takes the input image path, output image path, annotation text, maximum font size, and font color as inputs. This function annotates the image with the given text and saves the annotated image.

4. In the `annotate_image` function, load the input image using OpenCV and get its dimensions.

5. Convert the input image from BGR to RGB format using OpenCV, as Pillow uses RGB format.

6. Load the font (customizable path) and adjust its size using the `adjust_font_size` function to fit the wrapped text within the image frame.

7. Wrap the annotation text to fit within the image frame using `textwrap.fill` with a maximum width of 20 characters.

8. Create a Pillow draw object and calculate the position to place the text at the bottom-center of the image, leaving some margin at the bottom.

9. Draw the wrapped text on the image using the Pillow draw object.

10. Convert the Pillow image back to a NumPy array (BGR format for OpenCV).

11. Save the annotated image to the specified output path using OpenCV.

12. Define functions `browse_input_image` and `browse_output_path` to browse and select the input image file and output path for the annotated image, respectively.

13. Define the function `annotate_button_click` to handle the "Annotate Image" button click event. It retrieves the input image path, output image path, and annotation text from the respective entry fields and calls the `annotate_image` function.

14. Create the main application window using tkinter.

15. Create and position the widgets for input image selection: a label, an entry field, and a browse button.

16. Create and position the widgets for output path selection: a label, an entry field, and a browse button.

17. Create and position the widget for entering the annotation text: a label and an entry field.

18. Create and position the "Annotate Image" button.

19. Start the main event loop using `app.mainloop()`, allowing the application to run and respond to user interactions.

By following these steps, the code creates a GUI application that allows users to select an input image, specify the output path, and enter the subtitle text. The annotated image will be saved with the subtitle starting from the left side and wrapping accordingly.
