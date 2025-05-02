# Visual-Feature-Attribution-in-UMAP-Clustering-Using-The-Explainable-Boosting-Machine

## Abstract / Motivation

Dimensionality reduction techniques such as Uniform Manifold Approximation and Projection (UMAP) often yield visually discernible clusters, but the interpretation of these clusters can be difficult. This report presents a hybrid visualization tool that combines UMAP with the Explainable Boosting Machine (EBM) to identify which features of a dataset contribute to clustering in UMAP space. The system enables the extraction of interpretable insights from clustered 2D embeddings by training EBMs to predict cluster membership. The implementation follows the approach proposed in Salmanian et al. 2024 and is validated on datasets including synthetic 3D separable data, coronary artery disease (CAD) patient records, penguin physiology, and cellular breast cancer data in the context of classification. The resulting system provides an interpretable and effective visualization method for attributing features to visual clustering behavior.

## Using the Tool

The Jupyter notebook auto_UMAP_EBM.ipynb holds all necessary code to load a dataset, project into UMAP space, and utilize the EBM feature. It is compatible with any dataset. Datasets scanned by the pandas read_csv() function are optimal. 

The user must have a the following python packages downloaded:

- numpy
- pandas
- matplotlib
- sklearn
- umap
  - installed using the command "pip install umap-learn"
-  interpret
-  bokeh
-  panel
-  mpl_toolkits

To run the tool, follow the steps detailed in the notebook. 

## <span style="color:red;">WARNING:</span> 

Do NOT run the EBM without first selecting a cluster in the UMAP plot and clicking the white "Save Selection" button. Verify eligability to proceed by looking for a "Saved \# indices: [0, 1, ... " string output. 

Running the EBM code with an empty "save_indices" vector can have severe consequences and may even ruin the entire python session. This has occurred when the user notices the EBM code only displays the accuracy score and classification report when the cell has completed. 

Trouble Shooting:

- Restart the kernel 
- Delete and reopen the auto UMAP EBM tab from the IDE
- Copy all code cells into a new notebook 
- All of the above
 
    
