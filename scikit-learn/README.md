# Dockerfile for scikit-learn

### Installs following libraries on Ubuntu:
  * Python 
  * pip libraries:
    * numpy
    * pandas
    * matplotlib
    * scikit-learn
    * Jupyter

### Starts Jupyter notebook with following configuration:
  * Notebook server runs on port 8888.
  * /workdir as working dierectory. This can be used to mount and share data files b/w native host and docker container.
  * /notebook as notebook directory. This can be used to mount and share notebook ipynb files b/w native host and docker container.

### Building and running this image:
```bash
docker build -t scikit-learn .
docker run -it -p 8888:8888 -v /path/to/work-dir:/workdir -v /path/to/notebook-dir:/notebook scikit-learn
```
