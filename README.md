# Workflow for Algorithm

This project provides a MATLAB-based workflow for analyzing **nucleotide center of mass (COM)** calculations and **curve fitting** for molecular structures.

## 📂 Project Structure
```
Workflow_for_Algorithm/
│── src/
│   ├── main.m                      # Main execution script
│   ├── calculate_COM.m              # Function to calculate COM
│   ├── calculateAllCOM.m            # Batch processing for COM
│   ├── check_COM_of_helix.m         # Validation of COM calculations
│   ├── fitted_curve_result_new.m    # Curve fitting analysis
│   ├── Input_helices_and_nucleotide_indices.m  # Input processing
│── README.md                        # Project documentation
```

## 📦 Requirements

This project requires **MATLAB** with the following toolboxes:
- Signal Processing Toolbox (if used in curve fitting)
- Statistics and Machine Learning Toolbox (if used for data analysis)
- Bioinformatics Toolbox (if analyzing nucleotide structures)

## 🚀 Usage

### **Run the Main Script**
To perform the full workflow:
```matlab
main
```

### **Calculate Center of Mass**
To compute the COM for a given nucleotide:
```matlab
com = calculate_COM(nucleotide_data);
```

### **Curve Fitting**
To analyze the fitted curves:
```matlab
fitted_curve_result_new
```

## 📊 Expected Output
- **Computed center of mass (COM)** for molecular structures.
- **Validated helix COM calculations**.
- **Curve fitting results** for molecular analysis.

## 📝 Author
Yi-Shan Lan
