# Start from the course base image
FROM risserlin/bcb420-base-image:winter2026

# Install CRAN package
RUN R -e "install.packages('pheatmap', repos='https://cloud.r-project.org/')"

# Install Bioconductor packages
RUN R -e "if (!requireNamespace('BiocManager', quietly = TRUE)) install.packages('BiocManager'); BiocManager::install('DESeq2')"
RUN R -e "if (!requireNamespace('BiocManager', quietly = TRUE)) install.packages('BiocManager'); BiocManager::install('enrichplot')"

# Set working directory inside container
WORKDIR /home/rstudio/projects
