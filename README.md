# deepAI_pic_restore

# Do the following on anaconda terminal, clone this repository

git clone https://github.com/jsaroni/deepAI_pic_restore/GFPGAN.git
cd GFPGAN


# Install basicsr - https://github.com/xinntao/BasicSR, we use BasicSR for both training and inference
pip install basicsr

# Install facexlib - https://github.com/xinntao/facexlib, we use face detection and face restoration helper in the facexlib package
pip install facexlib

pip install -r requirements.txt
python setup.py develop

# If you want to enhance the background (non-face) regions with Real-ESRGAN, you also need to install the realesrgan package
pip install realesrgan

# Then download a trained model GFPGANCleanv1-NoCE-C2.pth from my google drive https://drive.google.com/drive/u/0/my-drive or from https://github.com/TencentARC/GFPGAN. To restore a picture use the following. Results are stored in the results directory.
python inference_gfpgan.py --upscale 2 --test_path inputs/whole_imgs --save_root results
