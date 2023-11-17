update on 11/17 (day of call!)
write my intro 
finish cycle gan implementation (1-2 hours)
<s>organize my questions for him </s>
finish podcast
<s>see if theres any other places i can find info from them</s>

goals:
- use less resources
- improve crop resilience
- improve biodiversity


measure **plant features** that were previously impossible. like what? what sort of plant features can u analyze?

large, multimodal, unstructured sets of the world’s agricultural data, sourced from satellite images, farm equipment, and public databases

crop genetics, environmental impacts, and management practices

Mineral has already surveyed and analyzed 10% of the world’s farmland and it says it will increase the number of data points pulled and analyzed from any one farm by more than 20 times by 2050, from an average of 190,000 data points per day in 2014.

trying to get more data out of one farm
	how would i do this?
		image --> get more plant features
			sides, top, ground? 
		 sensors:
			 temperature
			 humidity

have 80 different models: predict crop yields, increase production, target pests and weeds, reduce waste, minimize chemical and water use, and reduce the impact of agriculture on the planet

	rover going through fields collecting information
		what kind of backend
		is the computation being done on the robot? how does it take action to help the farmer?
		what sort of datatypes
		how much interoperation between those datatypes are needed to generate insights? obvi youd want to optimize for most amount, but getting diff types of data in the same latent space is hard? 
			well no if u can just embed it/tokenize it in the same latent space
					clip does it based on associations. sensor readings (temperature, moisture) taken at the same location should be more associated than others

80 different models, usually each model has a 
how do u have one general way of collecting information and then are able to apply it to 80 diff models? generality of models to take in information?

https://www.smithsonianmag.com/innovation/is-this-weed-spotting-yield-predicting-rover-future-of-farming-180978612/
collecting data from 10% of the worlds farmland
	ok a lot of this will be from the internet: what are the diff data sources available?
	some of this will be collected from their rover
		taking images, having sensors, over time and space
	have models for one farm that just operate on the sensor data, but best thing would be to combine that with the long time scale information they can get from satellites


how to breed better by analyzing over time which crops are more drought, heat, pest and disease resistant 
	go through the fields and model how many pests per plant
		plant specific information can be used for better breeding

Farmers today use sensors, GPS and spreadsheets to collect data on crops and generate satellite imagery of their fields
	theyre collecting a lot of information but dont know what to do with it 
	how do we take as much data as we can and break it down into


robotics, sensors, data modeling, machine learning and simulation
llms for sensor data? transformers for sensor data?



why does our rover need to be so big? bigger camera angle? 
	limit compression of the soil that would destroy bacteria

any modelling you guys are doing on microbial activity and correlating that to land management?
	using satellites to measure greenhouse gases and then also have information 
		
		
how much do u work with the farmer? how much do you know about their irrigation cycles? fertilizer usage? exact brands and ingredients?


![[Pasted image 20231115135135.png]]

https://developers.arcgis.com/python/guide/how-cyclegan-works/
comes up with simulated data about how strawberries look, but does that also come with labels?


detect these things
[rust disease](https://www.planetnatural.com/pest-problem-solver/plant-disease/common-rust/) and other plant fungal diseases
[Panama disease](https://www.britannica.com/science/Panama-disease) and [Sigatoka disease](https://www.promusa.org/Sigatoka+leaf+spot#:~:text=Sigatoka%20leaf%20spot%20(popularly%20known,in%20many%20banana%20production%20areas.)

once we've found a disease, a big farmer/a farmer with the tools would prefer to send a fungicide/pesticide through their sprinkler systems or use a small airplane to spray it over the fields. this is preventative, so the disease doesnt spread to the rest of the crops. 
	however, since we can catch diseases much earlier on, is there a way we can prevent spread of the disease and increase resilience of the whole field without needed large scale pesticide application?



what can the mineral rover do?
predict crop yields
increase production (?)
target pests and weeds --> it can identify them, but does it also have the arms/ability to apply fertilizer/pesticide inputs ?
reduce waste
predict harvest times
minimize chemical and water use
reduce the impact of agriculture on the planet
identify plant's flowering rate: essential to how a plant responds to its environment and how much 
measure leaf sizes and greeness
	greenness by taking pictures of the plant and converted the image from rgb color space to hsv 

moving through the field and taking a video or taking images at each plant?
**how do you enable the rover to see what is under the brush/leaves?**
University of illinois is doing this https://digitalag.illinois.edu/autonomous-farm/
1. Under canopy, high-throughput field phenotyping with compact robots and sensors
2. Under canopy commodity crop weeding and spraying robots and soil sensor networks
3. Urban food gardening with rail mounted and low-cost mobile robots
4. Plant manipulation in berry and nut orchards with low-cost mobile robots and soft manipulators


at different growing stages, collecting information about the plants so the farmers have a better idea of how much yield they will have
	help the plants grow, flower by
		pruning dead parts
		giving water 
		providing shade
		hand pollinating
		applying flowering stimulants
		checking for stress: water, nutrients, light, pests

crops theyve used:
	imaging soybeans, strawberries, melons, oilseeds, lettuce, oats and barley


more recently:
deeply understand plant physiology
discover more resilient crops - and do selective breeding with them
	does the rover have geospatial information (even as simple as longitude and latitude?). in which case, i see it being used for selective breeding: it discovers the most resilient crops on the field and pinpoints them for seed saving, enabling the farmer to get a better baseline for their crops each year that they use mineral
		how do u go against the limitations of using patented seeds if you were to go this route?
	 
increase production, and improve the bottom line for agribusinesses and farmers alike

observe/analyze
take action:
	microdose on pesticides and fungicides
	apply fertilizer
	inoculate and spread seeds
	harvest/prune
	improving flowers attraction to pollinators (uv marker in the inside of the flower, spraying something that attracts more pollinators)
	shaking plants so they can self pollinate better

what about analyzing rates of self pollination? to figure out which plants need more help getting pollinated
walking pollinator


Driscolls
Syngenta
	how does this partnership work? when the rover's goal is to reduce inputs, doesnt this go a bit against syngenta's whole profit model? or are we promising that the inputs we use will be syngenta's, which is a new stream of customer flow for them 
Cgiar


high-volume, high-dimensionality data from varying sources


elliot grant
36 US patents covering topics ranging from cryptography and food traceability, to satellite image analysis and plant phenotyping.


**Action Items**
listen to podcast
https://podcasts.apple.com/de/podcast/foa-345-alphabets-moonshot-to-scale-sustainable-agriculture/id1137767458?i=1000593674320
read paper
https://paperswithcode.com/paper/learning-fast-and-agile-quadrupedal#code
automating plant phenotyping

pollination:
pollen grain moves to the stigma (female counterpart) where it can move down through this tube called a pistil to fertilize an unfertilized egg 


## plant phenotyping

https://digitalag.illinois.edu/research/awards/using-computer-vision/
plants with which genes, in which environments, and under what management will be able to produce the most yeild?
	how much genotyping is going on? for each farm/crop they work on, do we have genotype information for the seeds they're planting?

generate trait data from images that scale from microscopic patterns of cells to growth of plants in large field trials.


[[robotics for plant phenotyping]]
[[cyclegan]]



things i need to do to prepare for the call
	be able to talk about the different types of people that i interacted with at loam:
		agronomists where we did gis and field sampling together
	be able to talk about my soil health analysis project and process from software to hardware
	be able to talk about how much information about plants u can collect from multispectral imaging:
		stereopi setup - dont even need to align, can also process individually


**Azure FarmBeats Data hub** - api layer that lets you aggregate
	- **Sensor data** from two sensor providers [Davis Instruments](https://www.davisinstruments.com/products/enviromonitor-gateway-us-lte), [Teralytic](https://teralytic.com/), [Pessl Instruments](https://metos.at/)
	- **Satellite imagery** from European Space Agency's [Sentinel-2](https://sentinel.esa.int/web/sentinel/home) satellite mission
	- **Drone imagery** from three drone imagery providers [senseFly](https://www.sensefly.com/) , [SlantRange](https://slantrange.com/) , [DJI](https://dji.com/)
	if u have/use any of these tools, farmbeats api helps you gain insights from it
	
	example tutorials:
		can make soil moisture maps
		can ingest historical telemetry data from data from your own IOT sensors



Implementations/ML:
[[cyclegan]]
[[cnn]]
[[paper on chrysanethemum cultivar classification]]


modelling with multimodal information? having sensor and image data in the same latent space
	https://www.mdpi.com/1424-8220/23/5/2381
	https://www.nature.com/articles/s41591-022-01981-2

# questions
[[mineral_questions]]


https://prophet.com/case-studies/mineral/


# datasets
	usda aggregating datasets collected from research papers: https://data.nal.usda.gov/search/type/dataset?query=np303
	[phenocam](https://data.nal.usda.gov/dataset/phenocam-images-arsltarmdcrresw-site-caroline-county-maryland-usa-2019)
	amazing paper with data from eddy covariance towers measuring water use efficiency, gas flux
[Assessment, Inventory, and Monitoring (AIM) terrestrial program](https://data.nal.usda.gov/dataset/ecological-site-identification-soil-observations-and-geomorphology-data-collected-assessment-inventory-and-monitoring-aim-terrestrial-program-between-2012-and-2021-western-united-states)


analyzing flux (photosynthesis and co2 exchange) from eddy covariance towers:
fluxnet paper: https://www.nature.com/articles/s41597-020-0534-3
dataset: https://fluxnet.org/data/fluxnet2015-dataset/

from neon: https://data.neonscience.org/data-products/DP4.00200.001#availabilityAndDownload

from landsat: https://landsat.gsfc.nasa.gov/data/data-access/
	landsat is 30m resolution
European Space Agency's Sentinel-5P,  instruments such as the Tropospheric Monitoring Instrument (TROPOMI)
https://jupyterhub.dataspace.copernicus.eu/ they have jupyter notebooks of how to analyze their data!!!