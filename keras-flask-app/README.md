## This Docker Images comes with following configuration:
#### 1. centos:latest
#### 2. Packages: python3, pip3, python3-devel, tensorflow==2.4.1,  keras==2.4.3, flask, jsonify==0.5

## Run the Container:
```
#   docker run -dit -p 80:8080 mtabishk/keras-flask-app:latest
```
##  Access the Flask WebApp:
      # http://[IP ADDRESS]

## Access the API:
      # http://[IP ADDRESS]/api/predict?no_pregnant=2&plasma_glucose_conc=22&diastolic_bp=3&triceps_skinfold_thickness=5346&serum_insulin=625&bmi=4&diabetes_pedigree_fn=45&age=66

##  Get the Bash Shell of the Container:
      #  docker exec -it [container id/ name]  bash


 
