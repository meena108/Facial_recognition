<h1>Facial_recognition</h1>

<p>
  Simple facial recognition demo in <strong>Google Colab</strong> using DeepFace.
  Register faces (filenames = names), upload a probe image, and see the predicted name with a visual overlay.
</p>

<p>
  <a href="https://colab.research.google.com/github/meena108/Facial_recognition/blob/main/Facial_recognition.ipynb" target="_blank" rel="noopener">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab">
  </a>
</p>

<h2>How to Use</h2>
<ol>
  <li><strong>Cell 1 – Install</strong>: installs <code>deepface</code>, <code>opencv-python-headless</code>, <code>retina-face</code>.</li>
  <li><strong>Cell 2 – Register</strong>: upload one or more clear face photos. Filenames should be the person’s name (e.g., <code>meena.jpg</code>, <code>raju.jpg</code>). Files are saved under <code>register/</code>.</li>
  <li><strong>Cell 2b – Add More (optional)</strong>: upload extra people later without restarting.</li>
  <li><strong>Cell 3 – Probe</strong>: upload the test image (e.g., <code>probe_raju.jpg</code>).</li>
  <li><strong>Cell 4 – Recognize</strong>: shows best match (or <em>Unknown</em>) and displays the image with a name overlay.</li>
  <li><strong>Cell 5 – List</strong>: prints all registered names.</li>
</ol>

<h2>Example</h2>
<ul>
  <li>Register: <code>meena.jpg</code>, <code>raju.jpg</code></li>
  <li>Probe: <code>probe_raju.jpg</code></li>
</ul>
<pre><code>This picture is of: raju (distance ≈ 0.03–0.04)
</code></pre>

<h2>Requirements</h2>
<ul>
  <li>Python 3 (provided by Colab)</li>
  <li>Libraries installed in Cell 1</li>
</ul>

<h2>Notes</h2>
<ul>
  <li>Use clear, front-facing photos; add 2–3 per person for better accuracy.</li>
  <li>If you add/rename images, delete any <code>representations_*.pkl</code> in <code>register/</code> to rebuild encodings.</li>
  <li>Default threshold = <strong>0.40</strong> (lower = stricter, higher = looser).</li>
</ul>

<h2>Author</h2>
<p>
  Meena Chand<br>
  <a href="mailto:meena.hgmd@gmail.com">meena.hgmd@gmail.com</a>
</p>
