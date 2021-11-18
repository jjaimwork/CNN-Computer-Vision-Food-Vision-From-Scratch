# Food-Vision-From-Scratch
This repository is a redo of MRDBourke's Food Vision App from scratch, applying everything I learned from the course chapter in addition of making my own dataset.

## Takeaways
-----------------

**Process:** 
* Generate the Base Model first  
> If it's overfitting the training set, either add more data or augment the data  
in our case we've reached almost perfect training results using our training data,  
but our validation data isn't doing very well as a result, it overfits  
so we did augmentation to feed our model more varieties of data to learn from.  
  
* plot history on every model.  
  
* Make a new checkpoint path for every model,  
  
* Save our model as h5 (or save the model, but without adding a directory since it's bugged)
  
* We can clone our model -> load weights from checkpoint -> **compile** -> evaluate  
  
**always compile before fitting** even after loading the model    
  

-----------------

From there we can use our pretrained model for **Fine Tuning**  
  
**compile** after turning layers trainable  
  
i.e. increasing epochs, making layers trainable, and doing a lr callback

-----------------

**Preprocessing and Training:**  
Use mixed precision, it helps with training time.  
use prefetch to preload data helps with training time  

-----------------

**When overfitting**
Add more training data  
Augment your data  
Simplify your model