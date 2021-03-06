# Projectile_Prediction

This program will use existing projectile test data to predict future test parameters required to reach a velocity target.

[![Build Status](https://travis-ci.org/coeyl/Projectile_Prediction.svg?branch=master)](https://travis-ci.org/coeyl/Projectile_Prediction)

[![DOI](https://zenodo.org/badge/181944492.svg)](https://zenodo.org/badge/latestdoi/181944492)

PyPi website:
https://test.pypi.org/project/ProP/

## Installation

The easiest way to install ProP is from PyPI with

    > pip install -i https://test.pypi.org/simple/ ProP


## Usage
Once the ProP is installed, a list of functions that can be used is provided with 'prop -h' or 'prop --help'

The sole interaction of ProP 1.0.2 is using 'prop -d' or 'prop --doc' followed by the title of the excel file
that will be used for the software. Note, the title does NOT include ".xlsx".

## Example
Before the program is executed, the an excel sheet is filled with known test data of a system that will be
modeled. The first column is a list of velocities measured, and the remaining columns are test parameters
that were captured.

On the second page of the same document, test parameters of predicted system need to be stated. Note that
all parameters on the second sheet must match the ones included on the first sheet. Because the gunpowder
for the second sheet is unknown, it can be left blank or filled in with one's.

The software is then executed using the following command:

    > python prop.py -d cube_data

Following the execution of the software, the user will then need to open the second excel file named "Prediciton.xlsx".
Inside the file on the first folder, the software will have generated a list of proposed gun powder loads for the shots of interest based on
the prediction data included in the "Cube_data" file on the second sheet.
