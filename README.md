# Spotify Analysis

## Contents
1. [Installation](#installation) 
2. [Usage](#usage)
3. [Project Architecture](#projectarchitecture)


<a name="installation"></a>
## Installation 

#### Pre-Requisites
[Python](https://www.python.org/downloads/), [Terraform](https://www.terraform.io/downloads.html) and [Spotify](https://spotipy.readthedocs.io/en/2.13.0/).


<a name="usage"></a>
## Usage 
Run the scripts with a dictionary of your faovurite artists or playlists to gather data about them and save it locally or in S3.

<a name="projectarchitecture"></a>
## Project Architecture 

<img src="https://github.com/liamhartley/spotify_analysis/blob/master/spotify_analysis.drawio.png" width="500px">

The Terraform scripts build:
- A lambda function with the analysis code
- A cloudwatch alarm to run that function weekly
- All relevant IAM policies / roles

This will generate a datalake of Spotify data locally or in S3.
