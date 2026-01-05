# CUDA Programming in Python

A learning repository for GPU programming in Python using **Numba** and **CuPy** on **Google Colab**.

## Overview

This repository contains my journey learning CUDA programming through Python, focusing on:
- **Numba**: JIT compilation and CUDA kernel development
- **CuPy**: NumPy-compatible GPU arrays and operations

Since I'm using an Apple M1 Mac (which doesn't support NVIDIA CUDA), I use **Google Colab** to access free NVIDIA GPUs for learning.

## Setup

### Using Google Colab (Recommended)

1. **Clone this repository** to your local machine:
```bash
git clone https://github.com/taosunsoftwareengineer/cuda-programming-in-python.git
cd cuda-programming-in-python
```

2. **Open any notebook in Google Colab**:
   - Go to [Google Colab](https://colab.research.google.com/)
   - Click `File → Upload notebook`
   - Upload a notebook from the `notebooks/` folder
   - Or use `File → Open notebook → GitHub` and paste the repo URL

3. **Enable GPU in Colab**:
   - Click `Runtime → Change runtime type`
   - Select `GPU` (T4, L4, or A100)
   - Click `Save`

4. **Verify GPU is available**:
```python
# Check GPU
!nvidia-smi

# Test Numba
from numba import cuda
print("CUDA Available:", cuda.is_available())

# Test CuPy
import cupy as cp
print("CuPy version:", cp.__version__)
```

### Workflow

1. **Edit locally**: Work on notebooks in your local `notebooks/` folder
2. **Run on Colab**: Upload to Colab when you need GPU execution
3. **Save results**: Download updated notebooks from Colab back to local
4. **Commit changes**: Push to GitHub to track progress

## Repository Structure

```
├── README.md           # This file
├── requirements.txt    # Reference (Colab has packages pre-installed)
└── notebooks/          # Jupyter notebooks for learning
```

## Learning Path

Topics organized in the `notebooks/` folder:
1. CUDA basics and GPU architecture
2. Numba fundamentals and CUDA kernels
3. CuPy array operations
4. Parallel programming patterns
5. Performance optimization

## Resources

- [Google Colab](https://colab.research.google.com/)
- [Numba Documentation](https://numba.readthedocs.io/)
- [CuPy Documentation](https://docs.cupy.dev/)
- [NVIDIA CUDA Documentation](https://docs.nvidia.com/cuda/)

## License

MIT
