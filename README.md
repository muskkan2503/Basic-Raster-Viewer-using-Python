# Basic-Raster-Viewer-using-Python
Python-based raster viewer project that aims to provide a user-friendly interface for loading, displaying, and manipulating raster data. The project involves the implementation of several key features to enhance the functionality and utility of the raster viewer.

Task 1: Raster Viewer: Develop a Python-based raster viewer. Implement functionalities for loading and displaying raster data, allowing users to zoom, and pan.

        Pillow library: was installed, which is a powerful image processing library in Python.
        Image: This module from the Pillow library is used for opening, manipulating, and saving image files.
        ipywidgets: This library provided interactive widgets for the Jupyter notebook.
        display: Displayed the image in the Jupyter notebook.
        Three sliders are created using FloatSlider from ipywidgets to control zoom, pan in the X-axis, and pan in the Y-axis.
        The sliders are initialized with default values, minimum, maximum, and step size.
        The update_image function takes three parameters: zoom, pan_x, and pan_y.It resizes the original image based on the zoom factor and then pastes the zoomed image onto a new image            with an offset determined by pan_x and pan_y.
        The interactive function from ipywidgets is used to link the sliders to the update_image function.

Task 2:Band Combination Change: Enable users to dynamically change band combinations for raster images. Implement a feature that allows users to select and visualize different combinations of bands to enhance the interpretation of the raster data.

        numpy: Library is used for numerical operations, and for handling multi-dimensional arrays.
        matplotlib.pyplot: Library is used for displaying images.
        ipywidgets.interact: This function is used to create sliders in the Jupyter notebook.
        The code loads a multi-band raster image from the specified file path using the Image.open() method from the Pillow library.  The image is then converted to a NumPy array using             np.array() for easier manipulation.
        The visualize_band_combination function takes three parameters: band1, band2, and band3, representing the bands to be combined for visualization. It creates a new RGB image by
        stacking the selected bands along the last axis using np.stack().The resulting RGB image is then displayed using plt.imshow() with a title indicating the selected band
        combination.
        The interact function is used to create sliders for interactive exploration of different band combinations.

Task 3: Shapefile (Shp) File Attribute Data Chart Plotting (using Matplotlib): Implement the capability to load and process shapefile (Shp) data. Utilize the matplotlib library to
generate charts representing attribute data associated with the shapefile features. Allow users to interactively explore and analyze the attribute data through charts.

        Three libraries were installed - geopandas, matplotlib, ipywidgets.
        The code reads the shapefile data using gpd.read_file() and stores it in a GeoDataFrame (gdf).
        Users can select different attribute columns from the dropdown, and the corresponding data distribution is displayed in a bar chart, allowing for dynamic exploration of the
        shapefile's attribute data.

Task 4: Use of NumPy for Array Manipulation:  Integrate the NumPy library for efficient array manipulation. Utilize NumPy functionalities to perform operations on raster data arrays,
such as mathematical transformations, filtering, and statistical analyses. Optimize data processing using NumPy capabilities.

        Libraries: numpy, PIL, matplotlib.
        simple mathematical transformation by adjusting the brightness of the image (transformed_image = raster_image * brightness_factor).
        The code uses the gaussian_filter function from scipy.ndimage to apply a Gaussian filter to the original image, creating a smoothed or blurred version (filtered_image).
        Calculates the mean and standard deviation of pixel values in the original image (mean_value = np.mean(raster_image) and std_deviation = np.std(raster_image)).
         code uses matplotlib.pyplot to create a side-by-side comparison of the original and transformed images in a single figure.
        The left subplot displays the original image in grayscale (plt.imshow(raster_image, cmap='gray')).
        The right subplot displays the transformed image, which, in this case, represents a brightness-adjusted version.
        
