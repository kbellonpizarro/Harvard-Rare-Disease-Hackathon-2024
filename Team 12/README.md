# ADDRESSING CMT4J/FIG4 DEFICIENCY USING A PRESSURE-REDUCING CUSTOMIZABLE BOOT

## Background
Charcot Marie Tooth Type 4J is a rare and severe disease that presents similarly to ALS, with high levels of misdiagnosis. $^1$ After studying the physiological progression of CMT4J across patients, $^2$ we discovered that the classic arched foot and weakened leg joint phenotypes do not currently have affordable nor accessible personalized boots addressing burden of movement. $^3$
We aim to design and test a customizable brace powered with an AI app allowing for adjustment recommendations, analogous to dental aligners, for preventing muscular dystrophy specifically in patients with all forms of CMT and other foot and lower leg deformities.

## Methods
We constructed a three-pronged approach of utilities as part of our solution: (1) The physical surface model, (2) an AI-powered app to generate continuous brace adjustments, and (3) the customizable boot.

### I) Creating Surface Model

![alt text](https://github.com/kbellonpizarro/Harvard-Rare-Disease-Hackathon-2024/blob/main/Team%2012/Figure%201.png "Figure 1")

A weekly progress monitoring system was developed, creating a 3D representation of the patient’s foot geometry for generation of adjustment recommendations.  
_Pin-art inspired mold:_ A box will be constructed with an array of closely spaced pins protruding upwards from its base. The pins will be arranged in a regular grid pattern, creating a flat, pressure-sensitive surface.  
_Gridded film_: A thin, flexible sheet with a printed grid of squares or dots will be placed on top of the pins in the mold box. The material of the film will be chosen for its ability to retain the imprint of the pins when pressure is applied, allowing for a 3D reconstruction through mapping the 2D density function into a 3D surface model.  
_Foot imprinting_: Participants will be instructed to stand barefoot within the mold box, placing their full weight on the gridded film. The pins will press against the film, creating indentations that correspond to the pressure exerted on each point of the foot's surface.  
_3D surface reconstruction_: Following the imprinting process, the participant will remove the film from the mold. The film will then be scanned using a high-resolution 3D scanner. This will capture the precise variations in the film's surface caused by the pin indentations, generating a digital representation of the foot's three-dimensional shape.

### II) AI-Powered App to Generate Continguous Brace Adjustments
We develop an AI-powered platform with the following capabilities:  
_Image acquisition_: Participants will use their smartphones to capture a high-resolution image of the imprinted gridded film. The app will guide the user through the image capture process, ensuring proper lighting and alignment for optimal image quality.  
_Dot detection and clustering_: The app will utilize the Hough Transform algorithm within the OpenCV library to identify and isolate the individual dots present in the image. This algorithm is specifically designed to detect circular shapes in an image, making it ideal for accurately identifying the grid points in the film, even in cases of slight warping or distortion.  
_Heatmap generation_: Once the dots are identified, the app will employ a clustering algorithm to group neighboring dots based on their proximity. This will create a heatmap visualization, where the intensity of each pixel reflects the density of dots in that region. Areas with higher dot density correspond to deeper imprints in the film, indicating areas of greater pressure experienced by the foot.  
_Deep Q-learning for pressure optimization_: A pre-trained Deep Q-learning model will translate from the generated heatmap data into boot pressure adjustment commands. Deep Q-learning with asynchronous off-policy updates is a reinforcement learning technique well-suited for robotic manipulation due to its ability to learn optimal actions through trial and error within a simulated environment. $^4$ In this case, the model will be trained using simulated foot pressure data to learn the optimal sequence of pressure adjustments within the customizable brace that minimizes localized pressure and discomfort on the foot.

### III) Customizable Boot

Current braces prioritize mobility and pure functionality over muscular dystrophy prevention. Addressing limitations of existing braces: The design of the customizable boot will address the shortcomings identified in existing non-adjustable braces. Existing braces often come in predetermined sizes, which can lead to improper fit and pressure distribution on individual feet. The human foot exhibits significant anatomical variation, making a one-size-fits-all approach ineffective and potentially harmful. The resulting improper pressure distribution within a brace can contribute to the development of blisters, calluses, and even fractured bones in severe cases. $^{2,3}$
Our customizable boot will be equipped with adjustable straps with adjustments instructed through the AI model within the app, dynamically modifying the pressure distribution within the boot based on the individual's foot morphology and pressure distribution data obtained from the surface model (see Figure 2).

![alt text](https://github.com/kbellonpizarro/Harvard-Rare-Disease-Hackathon-2024/blob/main/Team%2012/boot.png "Figure 2")  
Figure 2: 3D render of customizable boot  


The boot will address the following key physiological challenges $^3$:  
_Angular equilibrium and ankle stability_: The boot will incorporate inflatable compartments mimicking the function of the Peroneus Brevis and Tibialis Posterior muscles, providing targeted pressure to restore proper ankle alignment and stability.  
_High arch prevention and foot drop_: An inflatable compartment mimicking the Tibialis Anterior muscle will be strategically positioned to prevent the development of a high arch and foot drop, both common complications in certain foot conditions.  
_Claw toe prevention_: By addressing the underlying issues of ankle instability and arch deformities, the boot will indirectly help prevent the clawing of toes, a common consequence of these conditions.  
_Comfort and efficacy_: The boot will incorporate a viscoelastic sole material known for its pressure-redistributing properties. This, in conjunction with the AI-powered adjustments, will aim to minimize pressure points and enhance overall comfort while maintaining the effectiveness of the supportive function.  
_Artificial Achilles Tendon_: The boot will also integrate an artificial Achilles tendon component. This will mimic the natural elasticity of the Achilles tendon, allowing for a more natural and fluid gait. This feature is crucial in existing braces, allowing for full mobility.

## Conclusions
The current solutions in the market are not only inaccessible, they are not affordable. Due to the progressive worsening of this phenotype, physicians are left with no choice but to resort to an invasive, expensive, and technically challenging surgery to alleviate the burden of or even allow for walking for patients. In order to prevent the need for these drastic solutions, we propose this customizable brace powered with an AI app.
This solution requires very little R&D costs, so it will be a much more efficient and a quicker-to-scale solution than pharmaceutical companies will develop. Because they are profit-driven and this rare disease has such a low prevalence rate, they are not willing to take the actions necessary to affordably treat CMT4J/FIG4 deficiency. 
Although this brace is custom-designed for addressing the physiological progression of CMT4J, it has the potential to treat patients with any form of CMT or any muscular dystrophy in the lower leg and foot.

## Sources
1. https://www.curecmt4j.org/cmt4j/
2. https://www.youtube.com/watch?v=PB_qko3KkCw&ab_channel=CharcotMarieToothAssociation
3. https://medschool.cuanschutz.edu/docs/librariesprovider65/courtney-grimsrud/patient-handouts/charcot-marie-tooth-disease-foot-deformities.pdf?sfvrsn=768f92ba_2
4. https://arxiv.org/abs/1610.00633
