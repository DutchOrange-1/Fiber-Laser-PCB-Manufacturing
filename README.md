# Fiber-Laser-PCB-Manufacturing
Creating custom 1-2 layer PCBs by using a fibre laser. 

This project is an alternative to acid etching and CNC manufacturing of PCBs. The key benefits being the ease of use (No need to buy / expose yourself to chemicals, buy CNC parts, drill bits etc). The biggest advantage is drilling of the holes, without a drill bit, of any size. 
<br>
These advantages come with the added difficulties in the design and pre-processing phase, which will be discussed in the [Process section](#process). 
<br>
This project was developed in South Africa, PTA, University of Pretoria. The university had no input, nor any affordable resources for PCB manufacturing. Instead alternative public resources where explored, those who helped can be seen in [The Special Thanks section](#special-thanks-to). 

# Process
**Note** - a Fiber laser MUST be used, recommended with a 100 mm lense. Make sure to confirm this before anything else. 
## Design - PCB
Any program can do, but in my case I made use of Easy EDA. The key thing when designing is setting custom design rules. The minimum sizes are:


| Parameter     | ABS Minimum dimension (mm) | Recommended (mm) | Notes |
| --------      | --------                   | --------     | --------        |
| Trace width   | 0.25                       |  0.4         |                 |
| Hole Size (GPIO) | 0.7              |         0.8     |          Depending on the laser       | 
| Hole Size (Thin legs) | 0.6 | 0.7 | 1/4 W Resistors |
| Pad Size  | 1.2  | 1.3  | -  |
| Engrave item | 0.3  |  0.5  | Any feature that must be engraved  |
| Pad Distance | 0.3   | 0.4  | Surface pads - more space easier soldering |

<br>
Some other key items include:
<br>
- Use a copper pour and include islands, reduces the engraving times. 
- Use smaller holes than expected - laser will enlarge them. 


Some other things 

# Engraving Process
Currently only two machines settings have been tested. The key thing for all machines is to first do the holes, as the copper around it is first needed to remove unwanted heat. After this the trances can be engraved. 

## PLF-50H
**Traces Engraving**
| Setting           | Value    | Units |
| :---------------- | :------: | ----: |
| Speed             |   1500   | mm/s  |
| Frequency         |   30     | kHz   |
| Power             |  60-70   | %     |
| Loops             |  2       |  |

**Hole Drilling**
| Setting           | Value    | Units |
| :---------------- | :------: | ----: |
| Speed             |   1500   | mm/s  |
| Frequency         |   30     | kHz   |
| Power             |  70      | %     |
| Loops             |  30-40       |  |

## Galvo Scanner
**Traces Engraving**
| Setting           | Value    | Units |
| :---------------- | :------: | ----: |
| Speed             |   500   | mm/s  |
| Frequency         |   25     | kHz   |
| Power             |   100   | %     |
| Loops             |   3      |  |

**Hole Drilling**
| Setting           | Value    | Units |
| :---------------- | :------: | ----: |
| Speed             |   5        | mm/s  |
| Frequency         |   30      | kHz   |
| Power             |  100      | %     |
| Loops             |  1       |  |


# Results

# Manufacturing in South Africa - PTA

## Special Thanks To:
### Safari Outdoor
A special thanks to the branch in both PTA and Krugersdorp, as they where both great health. This include thanks to George, Trent, Le Roux and Lizel. <br>
They had a XT Laser Fiber - 50W (Krugersdorp), and PLF - 50H at PTA. <br>
Program: EzCad. <br>

The settings for these machines can be found [above](#)

### Sunnyside Engravers 
Thanks to Johnathan, who took the time to vectorize the initial designs, and the kind owner to do the testing from [SunnySide Engravers](https://sunnysideengravers.co.za/). <br>
The lase that was used is a **Galvo Scanner**, settings can be found [above](#galvo-scanner). <br>
A key thing he made note of, is the output of Inkscape was paths, and not objects, and many at that. The drawings must be simplified as much as possible. The background should also be transparent. 

# Other Resources:
[Laser Cutting a PCB with a CO2 / Fiber Trotec laser cutter](https://pub.fabcloud.io/tutorials/electronic_production/fiber_laser_pcb/), Which uses a **Trotec Speedy 100 flexx.**


