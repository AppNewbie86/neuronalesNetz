# neuronalesNetz
![AI](https://github.com/AppNewbie86/neuronalesNetz/assets/101304191/08c7037e-4741-4256-8415-c9af8c8c84b6)

Meine Dokumentation zu meinem ersten neuronalen Netzes


// Mache mir die Bibliotheken verfügbar 
import tensorflow as tf
from tensorflow import keras

// In dieser Zeile wird das Modell definiert. Es handelt sich um ein sequentielles Modell (Sequential), das aus einer einzigen Schicht (Layer) besteht. 
model = tf.keras.Sequential([keras.layers.Dense(units=1, input_shape=[1])])

// Hier wird das Model kompelliert
model.compile(optimizer='sgd', loss='mean_squared_error')

// Definition der Trainingsdaten 
xs = [1, 2, 3]
ys = [2, 4, 6]

// Hier wird das Modell trainiert 
// Die Methode fit wird aufgerufen und verwendet die gegebenen Eingangsdaten ('xs') und Zielwerte ('ys') für 1000 Epochen. Das Modell versucht, die optimale Gewichtung für das Neuron zu erlernen, um die gegebene lineare Beziehung abzubilden.
model.fit(xs, ys, epochs=1000)


