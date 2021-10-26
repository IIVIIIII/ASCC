# Additive Synthesis of a Climate Crisis

Additive Synthesis of a Climate Crisis involves a digitally manipulated recording of Jimi Hendrix performing “The Star Spangled Banner" at Woodstock in 1969. The number of sinusoids representing the frequency content of this recording increases through the duration of its playback at a rate corresponding to the cumulative sum of the United State’s carbon emissions as measured at the beginning of each year from 1969 to 2019. The piece aims to interpret Earth’s atmosphere as a spectral domain and carbon dioxide as sinusoids which enhance the resolution of our dire situation.

Within the selected span of years as scaled to the duration of the audio recording, individual years can be heard as slight oscillations in total signal gain. Starting at zero and concluding with a total of 70,730 million tonnes, each year’s cumulative sum of carbon emissions is rescaled to be represented by a range of sinusoid quantities from 32 to 1,048,576. This piece’s audio synthesis uses the Fast Fourier Transform (FFT) algorithm. Because the number of sinusoids in an FFT window must be a power of two, the relationship between tonnes of carbon and number of sinusoids is not precisely proportional. Instead, the relationship is conveyed through the gradual passing of certain thresholds defined by possible FFT sizes. At various moments during the audio’s playback, the time elapsed corresponds to a year during which rescaled carbon levels are equal to or greater than a previously unsurpassed power of two. During such an occurrence, the audio becomes represented by a number of sinusoids equal to the just surpassed power of two. This quantity of sinusoids is maintained until the rescaled CO2 levels correspond to the next viable quantity of sinusoids. This process is visualized in the image below:

![alt text](https://github.com/IIVIIIII/ASCC/blob/main/resources/photos/emissons_and_fft.png?raw=true)

This results in the final audio being comprised of eight different files with the following properties:

![alt text](https://github.com/IIVIIIII/ASCC/blob/main/resources/photos/jimis.png?raw=true)

The files above are manipulations of the source audio made through a program called Spear. The frequency resolution of a file is chosen as the lowest integer that will result in the desired FFT size according to Spear's algorithm. When the desired FFT size requires a frequency resolution less than one, the largest tenth is chosen instead. The file is resynthesized according to the parameters shown in the table pictured above (Minimum Amplitude Threshold and Amplitude Threshold Under Peak are left at their default settings). The specified parameters must be entered by hand as shown in the image below:

![alt text](https://github.com/IIVIIIII/ASCC/blob/main/resources/photos/spear.png?raw=true)

The recording of Jimi Hendrix’s interpretation of “The Star Spangled Banner” at Woodstock was chosen for its political implications. Furthermore, the performance occurred in 1969 which, for a data set that extends to 2019, delineates a convenient timespan of fifty years. More importantly, Hendrix’s performance offered a depiction of the United States’ collective anxieties which, at the time, mostly stemmed from the war in Vietnam. Additive Synthesis of a Climate Crisis appropriates the core expression of Hendrix’s “Star Spangled Banner” and applies it to the most severe crisis facing our contemporary world: climate change.

Additive Synthesis of a Climate Crisis was included as a submission to a research article by climate scientist Dr. Mika Tosca. The article, "Reimagining futures: Collaborations Between Artists, Designers, and Scientists as a Roadmap to Help Solve the Climate Crisis," was published in the UC Press's climate journal, Elementa. To read the article follow this link: https://online.ucpress.edu/elementa/article/9/1/00016/118297/Reimagining-futuresCollaborations-between-artists

This repository presents a recreation of the project with a data calculation process that has been automated and adjusted to achieve greater efficiency and accuracy. The included "notebook" folder contains the jupyter notebook used to calculate the data.

The carbon data and sampled audio used are available at these links:
- Carbon Data: https://www.icos-cp.eu/science-and-impact/global-carbon-budget/2019
- Sampled Audio: https://www.youtube.com/watch?v=sjzZh6-h9fM

Tools required:
- Python
- Pandas
- NumPy
- Matplotlib
- Max
- Spear

