# image-classifier-using-Tensorflow-in-Windows
Very Simple steps for creating image classifier using Tensorflow in Windows

Step1. Download Python (Python is already available go to step2) for windows
        link:- https://www.python.org/downloads

Step2. Download TensorFlow fow windows (Install it using "native"  pip)
        link:- https://www.tensorflow.org/install/install_windows

Step3. Validate your installation (Open python shell or windows terminal/command prompt)
         Run the code :- >>> import tensorflow as tf
                         >>> hello = tf.constant('Hello, TensorFlow!')
                         >>> sess = tf.Session()
                         >>> print(sess.run(hello))
   
        Output:-  Hello, TensorFlow!

Step4.  Download Docker for Windows and install it
          link:-   https://www.docker.com

Step5. Open Docker by clicking on icon Docker Quickstart Terminal
       5.1 Run the code:- docker run hello-world
       5.2 Run the code:- docker run -it gcr.io/tensorflow/tensorflow:latest-devel 

       # You should see "root@xxxxxxx#" 
        5.3  Run the code:- python
        5.4 Run the code:- 
                                     import tensorflow as tf
                                     hello = tf.constant('Hello, TensorFlow!')
                                     sess = tf.Session()
                                     print(sess.run(hello))

                      If you see "Hello, Tensorflow!", it works!

Step6.    ctrl-D  then:
                                     cd $HOME
                                     mkdir tf_files
Step7. Download the zip file and unzip it and paste it in tf_files folder

Step8.    docker run -it -v $HOME/tf_files:/tf_files  gcr.io/tensorflow/tensorflow:latest-devel
               ls /tf_files/
               cd /tensorflow
                git pull
Step9.  Final Step run the following code

python /tf_files/label_image.py /tf_files/flower_photos/daisy/21652746_cc379e0eea_m.jpg

           Output:--
                                   daisy (score = 0.98996)
                                   sunflowers (score = 0.00788)
                                   dandelion (score = 0.00153)
                                   tulips (score = 0.00058)
                                   roses (score = 0.00004)
