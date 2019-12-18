FROM prete/jupyter-rstudio-base:3.6.2

# Seurat 3.1.2
RUN Rscript -e 'BiocManager::install("multtest")'
RUN Rscript -e 'install.packages(c("Seurat"), dependencies = TRUE)'

# Install additional 
RUN Rscript -e 'install.packages(c("rJava", "Rmagic"), dependencies = TRUE)'
