# Hand-Cricket-Game-using-Computer-Vision
Created an interactive Hand-Cricket game using OpenCV python. Hand cricket is played through gestures (called 'throws') similar to rock paper scissors. The total number of fingers extended equates to the equivalent number, with a thumb counting as 6. Throws are made simultaneously by both players, one designated as the batter and the other as the bowler. Runs scored according to the batter's throws until the bowler throws the same, in which case the batter is "out".\

## Files details:-<br /> <br />
<b>Hand_cricket_compressed.mp4</b> -- Sample Video of the Program. <br/><br/>
<b>gather_images.py</b> --- Python file which when runs collects the image data captured in the box and stores it appropriately inside the category directories.<br /><br />
<b>Directories:-</b><br />
<b>none, five, four, three, two, one<br /></b><br />
<b>train.ipynb</b> --- File used for training the deep network model. <br /><br />
<b>hand-cricket-model_2.h5</b> ---- Mode .h5 file from the above training script.<br /><br />
<b>Play2.ipynb</b> --- Jupyter notebook file used to run the game. This extracts the above model and uses the weights to detect finger gestures.<br /><br />
## Description <br />
<br />

First the <b>gather_images.py</b> script was run and the images of the hand gestures were collected according to their categories. Categories:- None, Five, Four, Three, Two, One.<br />

Used <b>train.ipynb file</b> to train the model using the images gathered from the above script.
Used Squeezenet architecture for to train the model. The layers weight were frezzed except the last layer of the squeezenet. This last layer was added with additional CNN and ended with softmax activation layer to clasify the hand gestures. The dropuouts were included at 50% rate. Also AverageGlobal2D Pooling layer was added to reduce the computation speed and complexity.<br />

<b>Squeezenet architecture</b> was used to reduce the complexity of computations and increase the speed of the program.<br/>

Saved the model trained as <b>hand-cricket-model_2.h5.<br/></b>

Loaded the model into the <b>Play.ipynb</b> file and used OpenCV library to capture and classify images accordingly. The algorithm for the game is coded in this file to make the game run without any hassle.<br/>

<B>Requirements</b><br/>
Tensorflow >= 1.15.0, Keras latest version
