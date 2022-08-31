.. Exercise documentation master file, created by
   sphinx-quickstart on Sun Aug 21 19:02:05 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Exercise's documentation!
====================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

Code: 

   import numpy as np

   def pol2cart(r,theta):
      
      Parameters:

      * r: float, vector amplitude

      * theta: float, vector angle

      Returns:

      * x: float, x coord. of vector end

      * y: float, y coord. of vector end
      

      z = r * np.exp(1j * theta)
      x, y = z.real, z.image

      return x, y

   def cart2pol(x, y):
      
      Parameters:

      * x: float, x coord. of vector end

      * y: float, y coord. of vector end

      Returns:

      * r: float, vector amplitude
      
      * theta: float, vector angle
      

      z = x + y * 1j
      r,theta = np.abs(z), np.angle(z)

      return r,theta

