# G-Code Generator

A web-based application that converts images to G-Code and provides a visual preview of the drawing path.

## Features

- 📁 **Image Upload**: Upload images via click or drag-and-drop (supports JPG, PNG, BMP, GIF)
- 🎨 **Image Display**: View your original image in the browser
- 🔄 **G-Code Generation**: Automatically converts images to G-Code using edge detection
- 👁️ **Visual Preview**: See a visual representation of what the G-Code drawing will look like
- 📥 **Download**: Download the generated G-Code file (.gcode)
- 📊 **Statistics**: View G-Code file information (lines and size)

## How to Use

1. Open `index.html` in a web browser
2. Click the upload box or drag and drop an image file
3. Wait for the image to be processed
4. View the original image and G-Code path preview side-by-side
5. Click "Download G-Code" to save the .gcode file
6. Click "Upload New Image" to process another image

## How It Works

1. **Image Processing**: The uploaded image is resized and converted to grayscale
2. **Edge Detection**: A Sobel edge detection algorithm identifies the edges in the image
3. **G-Code Generation**: The detected edges are converted to G-Code commands with pen up/down movements
4. **Visualization**: The G-Code path is rendered on a canvas for preview

## Technical Details

- **Pure HTML/CSS/JavaScript**: No dependencies or server required
- **Client-side Processing**: All processing happens in the browser
- **G-Code Format**: Generated code includes proper headers, footers, and movement commands
- **Responsive Design**: Works on desktop and mobile devices

## G-Code Output

The generated G-Code includes:
- Header comments with image information
- G21 (millimeters), G90 (absolute positioning)
- M3/M5 (pen/spindle control)
- G0 (rapid movement), G1 (linear movement)
- Proper pen up/down commands
- Return to origin and end program commands

## Demo

Simply open `index.html` in your browser - no installation or setup required! 
