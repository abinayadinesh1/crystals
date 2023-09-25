Plant-level care at industrial farm scale. Optimizing crop yield and quality through the next generation of precision irrigation.

builds products to help the food systems keep pace with climate issues
	how aware are farmers that it is much harder to farm now than before? what do they think the reasons are for that?
		any motivating stories as to why you started this company?
orchards vs leafy greens/veggies --> variability in year to year produce?
what is the customer experience? how difficult is it to onboard 1 customer? what is the main effort for u? for them?
what scale farmers are you targetting?
what did ur early beta tests look like? how did u know this would work/be profitable/the plant would really survive/thrive with the new variable levels of 
"Save water by building custom automations through proprietary data and 3rd-party sensors"
	can i learn a bit more about the hardware you guys are using?
how much money are u saving a customer per year?
how long did this take to build out and retrofit? what does the team look like?
do you feel fulfilled/happy by this work? climate smart agriculture and its potential for remediating soils and improving plant nutrition, where do you want to see verdi going next?

customize water and fertilizer at the plant level
variable rate irrigation


abi:
2 major. metagenomics, microbial ecology. 
building hardware for farmers to optimize their water usage and fertility:
	using color +  sensors to measure soil moisture
	building cameras - microbial activity?

rgb - analyze the color space
uv - look at how many microbes


at a conference w a rlly cool startup who had a camera on a stack, pointed sideaways. u dig a hole, hammer the stick into the ground and it scans the layers of the osil as u go down. they can have their own light source, they know their camera. soil and cameras. they were trying to survey soil type based on a visual. 
	clay, silt, sand --> must send to a lab. (40-50$ per sample)
	makes sense bc its a one type scan
a lot of ppl go to college not knowing what they wanna do. 
he grew up in niagra ontario, close to ontario. had a similar experience. wine growing region, but he didnt know that until he started verdi. (for orchards and vinyards). when u think of ag, u think of the west coast (orchards, nuts, berries, vinyars) or the interior (wheat corn soybean). 

potentially volumetric content in soil. 
u have to sell them on it! or it has to be a very interesting product. 

at one point he didnt know anything abt farming, but then he talked ab a lot of people. a lot of wineries and orchards actually have a lot of phds (education). he puts farmers in 3 categories
1. the farmer, born and raised, family farmer. no official schooling. not looking to optimize things, just doing what works
2. smaller farmers that know what theyre doing and how water, soil systems, plant physiology work. 
3. has official education in ag. 
	1. these larger companies like vinyards in sonoma or napa are the ones most 
some farmers that dont see a need to improve (a minority)
talk to a few diff people across crop type, regions. i can go to **lodi** (a massive wine region), where fransdia super cheap 5-10$ bag wine (most popular wine by volume) grows here. 1,000's of acres of vv commercial vinyars w no wineries on them. lodi ( maximize volume at the lowest price) vs napa (appeal to the environmentally ) very diff goals. 

there is a group of farmers that care about organic, best practice farming and how challenging it is to be that type of farmers. not the best way to make money as a farmer. be buying local if u wanna support that kind of farmer.  a good book called 

some companies out there that gives these farms 200,000$ and say use this money to convert ur farm to organic or implement these practices and there expecting that the land value goes up and that the value of the produce is going up. thats how they pay back the initial investment plus more. solution: access to 

farmraise reminds him of an app or software that helps a farmer make sure theyre applying to all possible grants. all local resources. webflow they could go through. put in a few small details and we tell u everything thats available. 

did farmraise speak to farm consultants who do grant writing for people? ag extension?

he always gets people at verdi who say theyll help verdi get 
if u wanna access canadian tax credits, we'll do all the paperwork and ull get 20-30k but u have to pay 5-10 k . 

**grant when they just started: province of BC, BC agtech grant. 30 days, 300,000$ in the grant.** 
**canadian gov wants tech companies to be started in canada and make tech jobs in canada: they say, if ur a tech startup here and u outline a project, they will pay for 80% of technical salaries.** 
if they do a certain proj, they just need to describe the proj in the grant and set the right milestones and their gov will reimburse 80%. 

stage of dev:
they started this in their capstone project at university. arthur, cofounder just emailed someone they knew at google x for a capstone project they could work on. theyre looking to get every tree in an orchard a unique amount of water. look at satellite images, localized sensor data. if they can make something in 6 months, u can pitch in front of worlds largest wine company. they went and did it AND GOT THEIR FIRST CUSTOMER. wine company gave u 5k to implement. 
we flexed that to every other potential customer after, making it easier to get the following. 

farmers have heard ab agtech before, and a lot of the time had poor experiences. too hard to use, never gave them value, what thy paid for doesnt work. why they dont like agtech. 
OR been farming a particular way and see this as a risk. 

a lot of farmers want to try a really small trial for a year or two before spanning to the full farm. challenge in hardware : starting small and expansion is slow. thats why agtech is challenging: slow to deploy onto farms compared to traditional tech and industries. 

**even something so simple as soil moisture, he was so surprised to find a great solution for soil moisture.** 
buy probes from alibaba for a dollar, but the challenges are: dependent on the soil type, the rating means different things. probe requires calibration to the soil type. gravelly type soil, water holding capacity is very low. water sits in there like a sponge. much larger range of water fluctuation for clay. 

if u dont install them properly: the two electrodes measuring resistance have a rock or a pocket of air, it completely makes it useless. if u dont compact the soil around the probe, water flows down the stem of the soil moisture probe. theres no good soil moisture solution. in order to install it properly, it does take work. a lot of farmers bought this and realized its not useful so they discount all of agtech.  

salinity can effect it. OM u applied, fertilizer and pesticides, 

biggest technical difficulties:
	they were really excited they got the opportunity to put something they made on the farm. that was a big motivator: a product that hadnt been made before. variable rate irrigation. as eng students, they got to build something. as people into startups, an opp to make a product. 
	they got early support from 5,000 the customer paid, google x gave them 5k, eng physics at ubc gave 5,000, pitch comp gave them 5,000. kind of worked and kind of didnt. required a lot of manually effort to make it work. slowly improved it from there. slowly fixed one problem after another. 

	CUSTOMER 1 IS THE HARDEST. analogous to first job, first internship. 

		LoRaWAN - low power and long range. really popular in IOT device deployments. 
			theres a gateway and nodes that communicate to it, whereas cellular connects to a cell tower. have to deploy a gateway as well. all tech in the field communicates w that gateway. 
		if they arent using that, theyre using cell or bluetooth low energy (very long range and low power). 
		issue w cellular is its too much for just sending one data point of a sensor. 
			makes each device cheaper, lower power. 

	built off stm 32 l4. like arduino 18mega 328 by atmill (1 microcontroller). 

	software side: tti, laurawan network manager. each gateway has many communication packets from devices. what tti does is automatically ingests all packets from all gateway and makes it easy to add other gateways to the servers. now have a pool of packets on a server on the internet. 
tti allows them to easily route data from gateways onto a network server. eliminates 10's of thousands of lines of code. 
search by device id to get its data. makes it easy to send communications back to the device. 

on top of tti, they have a react webapp. started building on heroku. get data from farm to webapp, webapp sends data and commands to on field devices. 
they hired a ds and modelling person 4 months ago and theyre making sure all our data is organized in a database so its easy to call upon for diff data and modelling projects. 

when they first set things up, they dont think about how to perfectly organize data. initial goal is to build a UI to control and organize projects. it requires a diff setup.

		bluetooth, wifi, cellular are other types.

nart - data modelling hire - still in the process of reorganization and setting up this space to build up models. and theyre 2-3 months away from that, they can start researching things to do w our data. very easily in jupyter notebook test stuff out and pull data in. have a simple manual on what data exists, what type it is. 

the full time software engineer built out their whole dashboard. 
**a progressive web app** is the way to go for what theyre doing. u only need to .
	dont need to force updates. 

am i looking for funding?
once u look for funding, its important to find what u wanna build and problem u wanna solve first. before u recieve funding, u can do mockups, power points and customer interviews instead of building. instead of fully building it. that product might change and u want to only build it once instead of. 

driscolls
	primarily research. 
	dont have farms themselves. 
	research team and research farms where they figure out the best way to grow berries. provide the seeds, procedure, support research for thousands of farms. educate farmers. 
	def diff buckets. 


bunch of random arduinos and raspberry pis
ill give him a list 
	they do 

in 2 mo, if im still interested, looking at a data sci project 
other cool thing is they do have a customer pool where i can video call and 

they have one full timer in ca, arthur goes does vv often bc bunch of investors and customers. largest market. 