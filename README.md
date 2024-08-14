# Crab Pulsar Long-term Analysis

This project is part of the Bhartiya Antariksh Hackathon 2024, addressing the challenge: "How much the Crab pulsar has slowed down since launch of AstroSat? Finding rate of spin down rate of Crab pulsar with AstroSat LAXPC and CZTI observations."

## Overview

The Crab Pulsar is a young, rapidly rotating neutron star with a rotation period of ~33 ms. It's one of the brightest X-ray sources in the sky and is used as a standard calibration source. This project analyzes the changing rotation period of the Crab pulsar using AstroSat LAXPC and CZTI data from 2016 to 2024.

## Objectives

1. Measure the change in rotation period of the Crab pulsar over time using AstroSat LAXPC and CZTI observations from 2016 to 2024.
2. Determine if the spin-down rate in 2015 is the same as in subsequent years or if it's changing with time.
3. If there's a change in spin-down rate over time, compute this rate of change and compare it against radio measurements.

## Expected Outcome

- Pulse period of Crab as a function of time for the period 2016 to 2024 with at least one data point per year.

## Dataset

AstroSat data is available for download from the AstroSat data archive portal of Indian Space Science Data Center (ISSDC) at https://astrobrowse.issdc.gov.in/astro_archive/archive/Home.jsp

For more details on data analysis, refer to the AstroSat Science Support Cell (ASSC) page at http://astrosat-ssc.iucaa.in/data_and_analysis

## Tools and Technologies

- AstroSat specific analysis software (as mentioned on the respective instrument website at the AstroSat Science Support Cell)
- Standard analysis software such as HEASoft from HEASARC
- Python 3.x
- astropy
- numpy
- matplotlib

## Methodology

1. Select long observations of Crab spanning few tens of kiloseconds in different years.
2. Perform barycentric correction on the photon arrival times to convert them to the solar system barycentre.
3. Calculate the pulse period for each observation using the Lomb-Scargle periodogram.
4. Analyze the long-term trend in the pulsar's period.
5. Calculate and visualize the spin-down rate.
6. Compare X-ray measurements with radio measurements from Jodrell Bank Observatory.

## Features

- Loads and processes FITS files from AstroSat LAXPC and CZTI instruments
- Performs barycentric correction on the observation times
- Calculates the pulse period for each observation
- Analyzes the long-term trend in the pulsar's period
- Calculates and visualizes the spin-down rate
- Compares X-ray measurements with radio measurements

## Usage

1. Mount your Google Drive containing the FITS files.
2. Update the `observations` list with the paths to your FITS files and their corresponding years.
3. Run the notebook cells in order.

## Results

The notebook generates several plots:
- Crab Pulsar Period Evolution
- Spin-down Rate Evolution
- Comparison between X-ray and Radio measurements

## Evaluation Parameters

- Accuracy: Precision of the determined pulse period for individual observation.
- Relevance: Agreement of the pulse period derivative with the historical value of the period derivative.
- User Experience: Understanding of basic X-ray astronomical data reduction and timing analysis.

## Future Work

- Incorporate more recent data up to 2024
- Improve error handling and data validation
- Implement more sophisticated period detection algorithms
- Analyze potential glitches or anomalies in the spin-down rate

## Contact

For any queries or collaborations, please reach out:

- Email: prathamjain3903@gmail.com
- LinkedIn: [Pratham Jain](https://www.linkedin.com/in/pratham-jain-56682620a/)

## License

This project is open source and available under the [MIT License](LICENSE).
