# Acoustic-Feature-Characterisation-of-Genuine-and-Voice-Cloned-Speech-for-Spoofing-Analysis
Preview of dataset (download available upon request)
I have provided the preview of dataset with few samples in VC_Dataset_Preview file

Dataset: Acoustic Feature Characterisation of Genuine and Voice Cloned Speech for Spoofing Analysis🎙️

Description:
This work focuses on identifying low level acoustic inconsistencies between genuine and synthetic speech using a structured signal processing pipeline.

System Design and Methodology
     1. Dataset Engineering
          A key limitation in existing spoof detection research is the lack of realistic datasets. To overcome this:
           • Collected real speech recordings from public figures
           • Generated corresponding voice cloned samples using modern VC systems
           • Created a dataset of 11,778 audio segments, each of 1 second duration
👉 Why 1 second segmentation?
It enables the detection of micro level temporal and spectral anomalies that are often averaged out in longer audio signals.

     2. Signal Standardisation and Preprocessing
         To ensure consistency across samples:
           • Converted all audio to 16 kHz mono WAV format
           • Removed corrupted and silent samples
           • Balanced the dataset to avoid classification bias
           • Ensured uniform temporal representation
     This step is critical to eliminate data induced variance and focus purely on acoustic characteristics.

     3. Feature Extraction Framework
         Each audio segment is transformed into a 69 dimensional feature vector, capturing both spectral and temporal dynamics:
           a) Spectral Envelope Features
    		MFCC (20 coefficients): Capture the perceptual spectral structure of speech
  	          → Sensitive to formant smoothing in synthetic voices
           b) Temporal Dynamics
                Delta MFCC (20) and Delta-Delta MFCC (20): Represent first and second order temporal derivatives
                  → Reveal unnatural transitions and lack of micro modulation
           c) Harmonic Structure
                Chroma STFT: Encodes pitch class energy distribution
 	          → Synthetic speech often shows flattened harmonic profiles
           d) Nonlinear Energy Features
                Teager Energy Operator (TEO): Captures instantaneous energy fluctuations
                  → Genuine speech exhibits high variability, while synthetic speech is overly smooth
           e) Statistical & Spectral Descriptors
   		Spectral Centroid → frequency distribution (brightness)
   		Spectral Bandwidth → spread of spectral energy
   		Spectral Roll-off → high frequency attenuation
   		Zero Crossing Rate → signal noisiness and transitions
   		RMS Energy → amplitude dynamics

     4. Feature Representation
	 All extracted features are stored in a structured CSV format
         Each row → 1 second audio segment
         Each column → acoustic feature
         This makes the dataset directly usable for ML/DL pipelines.

Observations and Insights
    Through statistical comparison (without classifiers):
	✔️ MFCC Analysis
	     Genuine speech → high variability in lower coefficients
             Spoofed speech → smoother, compressed spectral envelope
	✔️ Chroma Features
	     Genuine speech → dynamic pitch distribution
	     Spoofed speech → uniform harmonic energy
	✔️ TEO Features
	     Genuine speech → strong nonlinear energy fluctuations
             Spoofed speech → reduced excitation variability
👉 These differences confirm that synthetic speech lacks micro-level irregularities inherent in human vocal production.

Key Takeaways
   • Short duration segmentation + rich acoustic features = highly discriminative representation
   • Handcrafted features still provide interpretability and efficiency compared to black box models
   • The dataset design bridges the gap between lab generated data and real world spoofing scenarios


Access:
Preview is available in GitHub.
To download the full dataset, send an email to:
jmrinashri@gmail.com

Include:
- Your Name
- Organization
- Purpose of use
