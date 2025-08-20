# Image Classifier with PyTorch

This repository contains a simple image classifier built using PyTorch and the CIFAR-10 dataset. This project is ideal for beginners to learn the fundamental concepts of building and training a neural network for a computer vision task.

### Requirements

Before running the code, ensure you have a Python environment set up with the correct dependencies.

1.  **Python Version**: This project has been tested with **Python 3.11** and is highly recommended to avoid version conflicts. You can use a tool like `pyenv` to manage your Python versions.

2.  **Required Libraries**: Install the necessary packages using `pip`. It is highly recommended to do this within a virtual environment.

    ```bash
    pip install torch torchvision numpy
    ```

    * **Note**: This project specifically requires a NumPy version less than 2.0. The `pip install` command will handle this automatically, but if you encounter issues, you can explicitly downgrade NumPy with:
        ```bash
        pip install "numpy<2"
        ```

---

### How to Run the Project

Follow these steps to get the project up and running.

1.  **Clone the Repository**:
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Set Up the Python Environment**:
    It is crucial to use a compatible Python version. If you use `pyenv`, you can set the local version for the project directory:

    ```bash
    pyenv local 3.11.9  # Or your chosen Python version
    ```

    Then, create and activate a virtual environment.
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install Dependencies**:
    With your virtual environment active, install the required libraries.

    ```bash
    pip install -r requirements.txt  # If you create this file
    # OR
    pip install torch torchvision numpy
    ```

4.  **Run the Code**:
    Execute the main script. The code will automatically download the CIFAR-10 dataset, train the model, and evaluate its performance.

    ```bash
    python your_script_name.py
    ```

---

### Troubleshooting

* **`ModuleNotFoundError: No module named 'torch'`**: Make sure your virtual environment is active and that you have installed the required libraries. If you are using `pyenv`, ensure the `pyenv local` command is set and the environment is active.
* **`RuntimeError: Caught RuntimeError in DataLoader worker process...`**: This is a common multiprocessing error on macOS and Windows. The provided code includes a solution by wrapping the training loop in `if __name__ == '__main__':`. Ensure your script has this block as shown in the provided example.
* **NumPy Compatibility**: If you encounter errors related to NumPy, re-run `pip install "numpy<2"` to ensure a compatible version is installed in your environment.
