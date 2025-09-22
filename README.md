Facial_recognition

Overview
Simple facial recognition demo in Google Colab using DeepFace.
Register faces (filenames = names), upload a probe image, and see the predicted name with a visual overlay.

Open in Colab
Open the notebook

How to Use

Cell 1 – Install
Installs deepface, opencv-python-headless, retina-face.

Cell 2 – Register
Upload one or more clear face photos. Filenames should be the person’s name (e.g., meena.jpg, raju.jpg).

Cell 2b – Add More (optional)
Upload extra people later without restarting.

Cell 3 – Probe
Upload the test image (e.g., probe_raju.jpg).

Cell 4 – Recognize
Shows best match (or Unknown) and displays the image with a name overlay.

Cell 5 – List
Prints all registered names.

Example

Register: meena.jpg, raju.jpg

Probe: probe_raju.jpg

Output: This picture is of: raju (distance ≈ 0.03–0.04)

Requirements

Python 3 (provided by Colab)

Libraries installed in Cell 1

Notes

Use clear, front-facing photos; add 2–3 per person for better accuracy.

If you add/rename images, remove any representations_*.pkl in register/ to rebuild encodings.

Default threshold = 0.40 (lower = stricter, higher = looser).

Future Work

Hook into Node-RED dashboard and MQTT to trigger devices (lock, name-tag engraver).

Store logs in a database (e.g., DB2).

Author
Meena Chand — meena.hgmd@gmail.com
