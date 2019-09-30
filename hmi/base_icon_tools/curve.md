# Curve

The curve element is usually used to display and monitor continuously changing asset data and the data changing trend.

.. note:: Before using the curve element to monitor asset data, you must configure storage policy for the asset measuring point on the EnOS Console. For more information, see `Configuring TSDB Storage  </docs/data-asset/en/latest/configuring_tsdb_storage.html>`__ .

Take the following steps to insert the curve element in the graph area.

1. From the **Base Icon Tool** navigation bar, select the **Curve** element, move the cursor to the graph area, and left-click the mouse.

2. Set the properties of the curve in the pop-up **Curve Tool Parameter Settings** window.

3. Under the **Basic Settings of Curve** tab, complete the basic configuration for the curve element:

   - Curve Type: Select the type of the curve (Real-Time Trend, Sample/Plan Trend, XY Curve, or XY Power Curve)

   - Curve Number: Number of inserted curves

   - Sampling Cycle: Select or enter the time interval of data sampling

   - Complete other settings based on business needs.

     .. image:: ../media/curve.png
        :width: 400px

4. Based on the selected curve type, configure the parameters of the curve under the **Configuration** tab (taking the Real-Time Trend curve as example):

   - Click the **Connect To Database** button to select the asset measuring point to be associated.

   - Select color for the curve

   - Select or enter the number of decimal digits

     .. image:: ../media/curve_property.png
        :width: 400px

5. Click **OK** to save the settings of the curve element.

   .. image:: ../media/created_curve.png
      :width: 400px

6. To further edit the properties of the curve element, double-click the element in the graph area, and make changes in the pop-up window.

7. Repeat the above steps to insert and edit other curve elements in the graph area.
