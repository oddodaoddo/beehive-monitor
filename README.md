# About

This is an attempt to come up with a cheap way to monitor bee colonies in apiaries. For this we use a Raspberry Pi, the BME680 seonsor board from Sparkfun and an audio card with a good quality microphone (see parts list).

## The idea

We collect humudity, temperature, barometric pressure and CO2 concentrations (BME680). We also record the sounds of the colony. Why is this done? The hope is that providing a cheap way for people to monitor hives and contributed data to a single point in the cloud, we can then analyze this data using modern machine learning algorithms and try to predict the % of colony survival over a period of time. We can then use the produced knowledge to "feed back" to the individual collection points and help the beekeeper to a) get an idea of how their hive is doing and b) make informed decisions on how to help the colony survive (if any help is necessary).

## The cost (and parts list)

* Raspberry Pi 3 (although any Pi will do that has the GPIO pins and can run Linux) - $35
* <a href="https://www.amazon.com/gp/product/B01HCC0210/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1">Audio injector sound card</a> - $21
* <a href="https://www.amazon.com/gp/product/B088KW9SWK/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1">BME680 Sparkfun sensor board with Qwiic connector system</a> - $22.95
* <a href="https://www.amazon.com/gp/product/B07JBK2LBZ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1">Sparkfun qwiic hat for Raspberry Pi</a> - $14.50

Total cost as is: $93.45

The cost can further be reduced by not using the Qwiic system and instead just using the BME680 sensor itself, soldered on a prototyping hat - estimated total cost would then drop to ~$70 per monitoring station.

## What does this repo have?

Here we have the software/scripts to collect the data and instructions how to produce a working monitor. 

## What this repo does not have

Not contained here is the future website/dashboard where individual beekeepers with this system can login and see the status of their own hives and/or contributed hand-curated/enriched data about said hives - any event related to a monitored colony such as inspection, loss of colony, feeding, treatment (if chosen to do so) etc. etc. - really any beekeeping practice conducted by the owner of an apiary. This data can then be used to add context to the information collected by the sensors, as input to the machine learning algorithms (e.g. the recorded sound of the colony can change after an inspection and this is good information to have in the models).
