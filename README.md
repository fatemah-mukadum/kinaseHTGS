# Overview

Using a SMILES string, this program will perform a minimal conformational search, compute 2D properties and compare against a ML trained model on solubility to determine if the molecule has high, low, or no solubility in water. 

## To install
```sh
# To install/update the project's dependencies
$> pip install -r requirements.txt

# To start the server
$> python -m flask run
```
### `app.py`

Runs the flask application to connect front-end html to chemistry.py

### `templates/base.html`

Using Bootstrap, a frontend toolkit, we created a polished UI where a user can input a string and then navigate to a page with moelcular properties. 
We've included a base Jinja template that we recommend extending in any of your own templates (learn more about extending templates [here](https://jinja.palletsprojects.com/en/stable/templates/#template-inheritance)):

### `chemistry.py`

Used RDKit, a cheminformatics package, to perform a conformational search and analysis that computes the molecular properties of any inputed valid SMILES string. 

## Future functionality 

Being able to generate more 3D descriptors to factor into our solubility prediction and automatically using Pymol to diplay 3D images, removing the need for manual image generation. 
