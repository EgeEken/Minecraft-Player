# Minecraft Player

This is an AI model that can play Minecraft in real time. Reacting at an estimated speed of 10 fps (this may vary based on computer specifications). 

It reads the screen using PIL (Python Image Library) and cv2 (OpenCV), and uses numpy to perform the necessary matrix calculations for the neural network. It transforms the live screen data into a matrix of 8 bit (1 byte) integers which represent values between black and white, this helps with faster processing, easier training for the neural network and also allows for a significant reduction in memory usage (The alternative was floats which are 4 bytes each). Even with these optimizations due to the amount of raw data that is represented by each frame, it still takes up a lot of RAM to train or even run a model like this.

Current progress:

- [X] Screen reader 
- [X] Screen data to normalized video matrix for training and running the ai 
- [X] Input executer
- [X] Keyboard Input Reader

- [ ] Mouse Input reader (the biggest roadblock right now is that minecraft tabs mess with the way cursors work and this prevents most input reading methods from being able to see mouse movement properly)
- [ ] Neural Network base (I have the math written down in a piece of paper that sits on my desk all day but i haven't fully set it up in code yet, but this should be an hour's work at most)
- [ ] (OPTIONAL) Simplified texture pack to make the process easier on the ai
- [ ] Training data (This will just be me playing the game with the input and screen reader running in the background so it's not a major time loss)
