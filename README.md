Facial_recognition

This repository contains a Google Colab notebook that demonstrates a simple facial recognition system using DeepFace
.

The workflow is designed like a conference registration and check-in demo:

Register delegates by uploading their photos (filenames = names).

Probe faces later to verify who they are.

Display results visually, with names shown in a dashboard-style output and label overlay on the face image.

How to Use
1. Open the notebook in Google Colab

Open in Colab

2. Run the notebook step by step
Cell 1 — Install dependencies

Installs deepface, opencv-python-headless, and required libraries.

Cell 2 — Upload registration images

Upload one or more face photos.

The filename should be the person’s name (e.g., meena.jpg, raju.jpg).

These images are stored in the register/ folder.

Cell 2b — (Optional) Add more people

Upload additional photos later without restarting.

Useful for adding new delegates as they arrive.

Cell 3 — Upload a probe image

Upload the test face (e.g., probe_raju.jpg).

This simulates checking in at the booth.

Cell 4 — Recognition and dashboard

Compares the probe face against all registered faces.

Prints whether it is a match or unknown.

Shows the face image with:

Title = predicted name

Overlay badge on the face

Cell 5 — List registered people

Prints all the names currently registered.

Example Flow

Register meena.jpg and raju.jpg.

Upload probe_raju.jpg.

The dashboard will say:

This picture is of: raju (distance=0.038)


and display the photo with “raju” written on it.

If no match is found (distance too high), it will say:

No good match → Unknown

Requirements

Python 3 (pre-installed in Colab)

Libraries (installed in Cell 1):

deepface

opencv-python-headless

retina-face

Notes

Use clear, front-facing face photos.

Add 2–3 photos per person for better accuracy.

Always delete the .pkl cache file when you add or rename images.

Recognition threshold is set at 0.40 (tune 0.35–0.45 for stricter or looser matches).

Future Work

Connect with Node-RED dashboard.

Use MQTT to trigger IoT devices (open box, print name tags).

Save recognition logs into a database (DB2, MongoDB, etc.).

Author

Meena Chand
Email: meena.hgmd@gmail.com
