# FunCoNN (BETA)

Interactive map of nervous system wiring in the nematode _C. elegans_. Live at [FunCoNN.princeton.edu](https://funconn.princeton.edu/).

FunCoNN is built on top of [NemaNode](https://nemanode.org/) (NemaNode is reported in Witvliet et al., 2021) and adds Functional Connectivity data from the [Leifer Lab](http://leiferlab.princeton.edu) (citation pending) on top of the Chemical Synapse and Gap Junction data generated by the [Zhen](https://www.zhenlab.com), [Samuel](https://scholar.harvard.edu/aravisamuel), and [Lichtman](https://lichtmanlab.fas.harvard.edu) labs.

The project repositories, where you can peruse the code, request features, and report bugs are both located on GitHub:
- [FunCoNN (BETA)](https://github.com/PrincetonUniversity/neuron-graph) (this project)
- [NemaNode](https://github.com/zhenlab-ltri/NemaNode) (original project)

## Required software
- [Node.js](https://nodejs.org/en/) >= 11.15.0
- [MySQL](https://www.mysql.com/downloads/) >= 5.6
- [GCC/g++ compiler](https://packages.ubuntu.com/focal/build-essential)


## Development setup

1. Setup MySQL if first-time use: `sudo mysql_secure_installation`
2. Install app dependencies by running `npm install`
3. Setup MySQL user and database: `scripts/setup_config.sh funconn funconn_user password | sudo mysql`
4. Populate database: `npm run populate-database`


## Commands
Once setup is completed, you will be able to run the following commands in this project directory:

- `npm run watch` or `npm start`: start a app server to test alongside development (localhost:3000)
- `npm run build-prod`: build the production version of the app
- `npm run test`: run the tests
- `populate-database`: take the raw data in src/server/db/raw-data and populate the mysql db with it


## Documentation
For more information on how to do various things read the documentation
- [Understanding the data used in funconn](docs/understanding-funconn-data.md)
- [Adding new data to funconn](docs/adding-new-data.md)
- [Deployment to AWS](docs/deployment-to-aws.md)
