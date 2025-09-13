📄 Document Denoising using CycleGAN

A deep learning project for document restoration and denoising, built using CycleGAN (from TensorFlow examples).
The goal is to improve the quality of scanned or noisy documents by removing artifacts, stains, and distortions, making them easier to read and process with OCR systems.
🚀 Overview

Problem: Scanned and historical documents often suffer from noise, stains, or poor quality, which reduces readability and OCR accuracy.

Solution: A CycleGAN model is trained to translate noisy documents → clean documents, while enforcing cycle consistency and identity mapping to preserve original structure.

Application domains:

Digitization of historical archives

OCR preprocessing (invoices, legal docs, medical records)

Restoration of degraded scanned documents

🧠 Methodology

This project uses CycleGAN with:

Two Generators (G: Noisy → Clean, F: Clean → Noisy)

Two Discriminators (Dx, Dy)

Losses:

Adversarial Loss

Cycle Consistency Loss

Identity Loss

Key idea:

If a noisy document can be mapped to a clean version, and then back to the noisy version, the model learns a consistent and meaningful mapping.

📂 Dataset

Train set: train/ (noisy docs), train_cleaned/ (clean docs)

Test set: test/ (unseen noisy docs)

Images are resized to 512 × 512 and normalized.

(You can adapt this to your own scanned/archival datasets.)

⚙️ Installation
# Clone this repository
git clone https://github.com/your-username/document-denoising-cyclegan.git
cd document-denoising-cyclegan

# Install dependencies
pip install tensorflow tensorflow-datasets tensorflow-addons
pip install opencv-python pillow matplotlib

🏋️ Training

Unzip the datasets inside data/.

Run training:

python train.py


Checkpoints are saved under ./checkpoints/.

Intermediate results are saved in ./images/.

🧪 Future Work

Add evaluation metrics (PSNR, SSIM, OCR accuracy).

Compare against baseline filters (OpenCV, UNet autoencoders).

Train on larger datasets for better generalization.

Deploy as a web app for uploading & cleaning documents.

🙌 Acknowledgements

This project extends the official TensorFlow CycleGAN & Pix2Pix Examples
.

Thanks to the TensorFlow team for open-sourcing their research code.

👩‍💻 Author

Sahitya A

🎓 MS in Data Science (in progress)

💡 Interested in Deep Learning, Computer Vision, and AI for Social Good







