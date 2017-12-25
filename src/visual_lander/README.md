visual_landing practice
======================

The objective of this practice is to perform a PID reactive control capable of following the line painted on the racing circuit.

/////////////////////////////
How to launch the practice
/////////////////////////////

To launch the infrastructure of this practice, first launch the simulator with the appropriate scenario: gazebo landing.world

Then you have to execute the academic application, which will incorporate your code: python2 ./visual_lander.py visual_lander_conf.yml

////////////////////////////
How to do the practice
////////////////////////////

To carry out the practice, you have to edit the file MyAlgorithms.py and insert in it your code, which gives intelligence to the autonomous car.

///////////////////////////
Where to insert the code
//////////////////////////

  MyAlgorithm.py

    def execute(self):
        #GETTING THE IMAGES
        input_image = self.camera.getImage()

        # Add your code here
        print "Runing"

        #EXAMPLE OF HOW TO SEND INFORMATION TO THE ROBOT ACTUATORS
        self.cmdvel.sendCMDVel(0.5,0,0,0,0,0)

        #SHOW THE FILTERED IMAGE ON THE GUI,
        self.camera.setColorImage(input_image_Copy)

   API

    camera.getImage() - to get the left image of the stereo pair
    self.setImageFiltered() - allows you to view a debug image or with relevant information. It must be an image in RGB format (Tip: np.dstack())

///////////////////////
Demonstrative video
//////////////////////

	https://www.youtube.com/watch?v=GFKzw55BDm0

    Base code made by Alberto Martín (@almartinflorido)
    Code of practice performed by Pablo Moreno (@PabloMorenoVera)
    Gazebo models and worlds made by Francisco Pérez y Pablo Moreno (@fqez, @PabloMorenoVera)