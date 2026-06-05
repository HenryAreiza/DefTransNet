# DefTransNet: a transformer-based method for non-rigid point cloud registration in the simulation of soft tissue deformation [(Paper Link)](https://doi.org/10.1088/1361-6501/ade613)
Soft-tissue surgeries, such as tumor resections, are complicated by tissue deformations that can obscure the accurate location and shape of tissues. By representing tissue surfaces as point clouds and applying non-rigid point cloud registration (PCR) methods, surgeons can better understand tissue deformations before, during, and after surgery. Existing non-rigid PCR methods, such as feature-based approaches, struggle with robustness against challenges like noise, outliers, partial data, and large deformations, making accurate point correspondence difficult. Although learning-based PCR methods, particularly transformer-based approaches, have recently shown promise due to their attention mechanisms for capturing interactions, their robustness remains limited in challenging scenarios. In this paper, we present DefTransNet, a novel end-to-end transformer-based architecture for non-rigid PCR. DefTransNet is designed to address the key challenges of deformable registration, including large deformations, outliers, noise, and partial data, by inputting source and target point clouds and outputting displacement vector fields. The proposed method incorporates a learnable transformation matrix to enhance robustness to affine transformations, integrates global and local geometric information, and captures long-range dependencies among points using transformers. We validate our approach on four datasets: ModelNet, SynBench, 4DMatch, and DeformedTissue, using both synthetic and real-world data to demonstrate the generalization of our proposed method. Experimental results demonstrate that DefTransNet outperforms current state-of-the-art registration networks across various challenging conditions.

# DeformedTissue Dataset [(Data Link)](https://doi.org/10.11588/DATA/OAUXWS)
Tissue deformation is a critical issue in soft-tissue surgery, particularly during tumor resection, as it causes landmark displacement, complicating tissue orientation. The authors conducted an experimental study on 45 pig head cadavers to simulate tissue deformation, approved by the Mannheim Veterinary Office (DE 08 222 1019 21). We used 3D cameras and head-mounted displays to capture tissue shapes before and after controlled deformation induced by heating. The data were processed using software such as Meshroom, MeshLab, and Blender to create and evaluate 2½D meshes. The dataset includes different levels of deformation, noise, and outliers, generated using the same approach as the SynBench dataset. 1. Deformation_Level: 10 different deformation levels are considered. 0.1 and 0.7 are representing minimum and maximum deformation, respectively. Source and target files are available in each folder. The deformation process is just applied to target files. For simplicity, the corresponding source files to the target ones are available in this folder with the same name, but source ones start with Source_ and the target files start with Target_. The number after Source_ and Target_ represents the primitive object in the “Data” folder. For example, Target_3 represents that this file is generated from object number 3 in the “Data” folder. The two other numbers in the file name represent the percentage number of control points and the width of the Gaussian radial basis function, respectively. 2. Noisy_Data For all available files in the “Deformation_Level” folder (for all deformation levels), Noisy data is generated. They are generated in 4 different noise levels namely, 0.01, 0.02, 0.03, and 0.04 (More explanation about implementation can be found in the paper). The name of the files is the same as the files in the “Deformation_Level” folder. 3. Outlier_Data For all available files in the “Deformation_Level” folder (for all deformation levels), data with outliers is generated. They are generated in different outlier levels, in 5 categories, namely, 5%, 15%, 25%, 35%, and 45% (More explanation about implementation can be found in the paper). The name of the files is the same as the files in the “Deformation_Level” folder. Furthermore, for each file, there is one additional file with the same name but is started with “Outlier_”. This represents a matrix with the coordinates of outliers. Then, it would be possible to use these files as benchmarks to check the validity of future algorithms. Additional notes: Considering the fact that all challenges are generated under small to large deformation levels, the DeformedTissue dataset makes it possible for users to select their desired data based on the ability of their proposed method, to show how robust to complex challenges their methods are. The DeformedTissue dataset is publicly available under https://doi.org/10.11588/DATA/OAUXWS.

# SynBench Dataset [(Data Link)](https://doi.org/10.11588/data/R9IKCF)
Despite the existence of several datasets for deformable point cloud registration, the absence of a comprehensive benchmark with all challenges makes it difficult to achieve fair evaluations among different methods. SynBench, a new non-rigid point cloud registration dataset created using SimTool—a toolset for soft body simulation in Flex and Unreal Engine. SynBench provides the ground truth of corresponding points between two point sets and encompasses key registration challenges, including varying levels of deformation, noise, outliers, and incompleteness. To the best of the authors’ knowledge, compared to existing datasets, SynBench possesses three particular characteristics: 1) it is the first benchmark that provides various challenges for non-rigid point cloud registration, 2) SynBench encompasses challenges of varying difficulty levels, 3) It includes ground truth corresponding points both before and after deformation. The authors believe that SynBench makes it possible for future non-rigid point cloud registration methods to present a fair comparison of their achievements. The SynBench is publicly available under https://doi.org/10.11588/data/R9IKCF.

# SimTool [(Paper Link)](https://www.sciencedirect.com/science/article/pii/S2665963823000581), [(Code Link)](https://github.com/m-kinz/SimTool)
SynBench dataset is created using SimTool — a toolset for soft body simulation in Flex and Unreal Engine. 


# Citation
**If you use DefTransNet code, please cite:**<br />
@article{10.1088/1361-6501/ade613,<br />
	author={Monji Azad, Sara and Kinz, Marvin and kothari, Siddharth and Khanna, Robin and Mihan, Amrei Carla and Maennle, David and Scherl, Claudia and Hesser, Juergen W},<br />
	title={DefTransNet: A Transformer-based Method for Non-Rigid Point Cloud Registration in the Simulation of Soft Tissue Deformation},<br />
	journal={Measurement Science and Technology},<br />
	url={http://iopscience.iop.org/article/10.1088/1361-6501/ade613},<br />
	year={2025},<br />
  publisher={IOP Publishing}<br />
 }


**If you use DeformedTissue Dataset please cite both the paper and data:** <br />
@article{10.1088/1361-6501/ade613,<br />
	author={Monji Azad, Sara and Kinz, Marvin and kothari, Siddharth and Khanna, Robin and Mihan, Amrei Carla and Maennle, David and Scherl, Claudia and Hesser, Juergen W},<br />
	title={DefTransNet: A Transformer-based Method for Non-Rigid Point Cloud Registration in the Simulation of Soft Tissue Deformation},<br />
	journal={Measurement Science and Technology},<br />
	url={http://iopscience.iop.org/article/10.1088/1361-6501/ade613},<br />
	year={2025},<br />
  publisher={IOP Publishing}<br />
 }

@data{DATA/OAUXWS_2025,<br />
author = {Monji Azad, Sara and Scherl, Claudia and Männle, David},<br />
publisher = {heiDATA},<br />
title = {{DeformedTissue Dataset}},<br />
year = {2025},<br />
version = {V1},<br />
doi = {10.11588/DATA/OAUXWS},<br />
url = {https://doi.org/10.11588/DATA/OAUXWS}<br />
}

**If you use SynBench Dataset please cite both the paper and data:** <br />

@article{monji2024robust,<br />
  title={Robust-DefReg: a robust coarse to fine non-rigid point cloud registration method based on graph convolutional neural networks},<br />
  author={Monji-Azad, Sara and Kinz, Marvin and M{\"a}nnel, David and Scherl, Claudia and Hesser, J{\"u}rgen},<br />
  journal={Measurement Science and Technology},<br />
  volume={36},<br />
  number={1},<br />
  pages={015426},<br />
  year={2024},<br />
  publisher={IOP Publishing}<br />
}

@data{data/R9IKCF_2023,<br />
author = {Marvin Kinz},<br />
publisher = {heiDATA},<br />
title = {{SimTool-SynBench}},<br />
year = {2023},<br />
version = {V2},<br />
doi = {10.11588/data/R9IKCF},<br />
url = {https://doi.org/10.11588/data/R9IKCF}<br />
}


**If you use SimTool, please cite:**

@article{monji2023simtool,<br />
  title={SimTool: A toolset for soft body simulation using Flex and Unreal Engine},<br />
  author={Monji-Azad, Sara and Kinz, Marvin and Hesser, J{\"u}rgen and L{\"o}w, Nikolas},<br />
  journal={Software Impacts},<br />
  volume={17},<br />
  pages={100521},<br />
  year={2023},<br />
  publisher={Elsevier}<br />
}


---

## Environment Setup & Installation

To run this code locally or on a server, it is highly recommended to isolate the dependencies using a Python virtual environment. 

### 1. System Dependencies (Headless / WSL Environments)
If you are running this on a headless Linux server or within Windows Subsystem for Linux (WSL), the visualization libraries (Plotly/Kaleido) require specific shared graphical libraries to render and save 3D plots to PDF. 

Run the following to install the necessary system dependencies:
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3-venv python3-pip -y
sudo apt install libnss3 libatk1.0-0 libatk-bridge2.0-0 libcups2 libdrm2 libxkbcommon0 libxcomposite1 libxdamage1 libxrandr2 libgbm1 libasound2t64 -y

```

### 2. Initialize the Virtual Environment

Create and activate an isolated environment:

```bash
python3 -m venv deftrans_env
source deftrans_env/bin/activate

```

### 3. Install PyTorch (CUDA)

To leverage GPU acceleration, install the CUDA-enabled version of PyTorch. (The command below is for CUDA 12.1; adjust the URL if your hardware requires a different version):

```bash
pip install --upgrade pip
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

```

### 4. Install Project Requirements

Install the remaining mathematical, visualization, and dataset utilities:

```bash
pip install -r requirements.txt

```

### 5. Download the Dataset
This project utilizes the ModelNet10 dataset provided by Princeton University. You can download and extract it directly into the project root using standard command-line tools:

```bash
# Download the dataset zip file
wget http://3dvision.princeton.edu/projects/2014/3DShapeNets/ModelNet10.zip

# Extract the contents (requires the 'unzip' package)
unzip ModelNet10.zip

# Clean up the downloaded zip archive
rm ModelNet10.zip

```

*Note: Ensure the extracted folder is named `ModelNet10` and sits in the same directory as the Jupyter notebook.*

