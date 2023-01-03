+++ 
draft = false
date = 2019-11-19T10:13:01-04:00
title = """
  Using Drive-by Health Monitoring to Detect Bridge Damage Considering
  Environmental and Operational Effects
"""
slug = "" 
aliases = [
  "/2018/drive/"
]
authors = [
  "William Locke",
  "Justin Sybrandt",
  "Ilya Safro",
  "Sez Atamturktur",
]
venue = "Journal of Sound and Vibration"
# Add these to specify external content
[[links]]
  name = "Preprint"
  url = "https://engrxiv.org/ntfdp/"
  weight = 10
[[links]]
  name = "Code"
  url = "https://github.com/JSybrandt/HighPerformanceBridgeSim"
  weight = 20
+++

## Abstract: 

Drive-by Health Monitoring utilizes accelerometers mounted on
vehicles to gather dynamic response data that can be used to continuously
evaluate the health of bridges faster and with less equipment than traditional
structural health monitoring practices. Because vehicles and bridges create a
coupled system, vehicle acceleration data contains information about bridge
frequencies that can be used as health indicators. However, for drive-by health
monitoring to be viable, variabilities in dynamic measurements caused by
environmental and operational parameters, such as temperature, vehicle speed,
traffic, and surface roughness need to be considered. In this paper, a finite
element model of a simply supported bridge is developed considering the
aforementioned variabilities and various levels of structural damage. Vehicle
acceleration data obtained from the model is analyzed in the frequency domain
and processed using a neural network architecture. This method is used to
determine the relationships between noise inducing variables and changes in
vehicle dynamic response spectrum; these relationships are leveraged to predict
the overall health of the subject bridge. The results from this study indicate
that the proposed approach can serve as a viable health monitoring strategy and
should be further tested on physical bridge systems.
