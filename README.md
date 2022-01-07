# deepAI_pic_restore

#download a trained model from https://drive.google.com/drive/u/0/my-drive then do the following on anaconda terminal;

#make it your directory
git clone https://github.com/jsaroni/deepAI_pic_restore/GFPGAN.git
cd GFPGAN


# Install basicsr - https://github.com/xinntao/BasicSR
# We use BasicSR for both training and inference
pip install basicsr

# Install facexlib - https://github.com/xinntao/facexlib
# We use face detection and face restoration helper in the facexlib package
pip install facexlib

pip install -r requirements.txt
python setup.py develop

# If you want to enhance the background (non-face) regions with Real-ESRGAN,
# you also need to install the realesrgan package
pip install realesrgan

# To restore a picture. Results are stored in results.
python inference_gfpgan.py --upscale 2 --test_path inputs/whole_imgs --save_root results
