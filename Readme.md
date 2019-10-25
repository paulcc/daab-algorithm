h1. Ambulance, Patient & Volunteer Scheduling

h2. Overview

The local charity "Daft as a Brush" operates a free
service for transporting cancer patients to important 
hospital appointments. Currently this runs in the Tyne &
Wear area, but they are keen to extend the service
to other parts of the country. The charity's founder,
Brian Burnie, is currently doing a round-the-coast
walk of GB and Ireland to raise funds and raise interest
in the scheme. He's covered all of Scotland and Ireland 
already, and is making good progress around Wales!

See https://www.daftasabrush.org.uk/ for more information.


The charity owns a fleet of around 25 ambulances, 
and relies on a group of volunteers to drive these
each week day in order to pick up patients, drive
them to hospital, sometimes stay with the patient 
during their treatment, then drive them back home. 
It makes a huge difference to patients to not have to worry 
about the logistics of getting to their treatment.

Each ambulance requires a driver and a companion, 
and can transport up to three patients at any time. 

The drivers and companions are taken from a pool
of volunteers who have indicated their availability
on certain days during a given week. 
The patients who need transport are distributed 
throughout the area, and their appointment times
range throughout the day. 

Overall, the problem is to match volunteers and 
patients to ambulances, producing a schedule for
each ambulance which details the volunteers
for each day, and the sequence of pick ups and
drop offs of the patients. 

Where possible, schedules should also not require too 
much extra driving (i.e. prefer to pick up local 
patients), make good use of capacity (combine patient 
journeys where feasible), not require too much
additional waiting time for combined journeys, 
and not ask too much of volunteers. These points 
are deliberately left vague - they will be discussed 
in more detail later. 




h1. More formally....

h2. Volunteers

Volunteers are classed as drivers or companions - including a few people 
who qualify as both (though we tend to need them as drivers more often 
than as companions). All volunteers have a location - currently derived 
from their postcodes and converted to latitude & longtitude via a 
suitable geocoding service. 

Each week, volunteers submit information about which days they can offer. 
This information selects the weekdays they can help, plus the _number_ of days
that week they are able to help. For example, some people might only offer
a single day, others might offer a maximum of M days chosen from a set of N, 
e.g. 2 days out of Monday, Tuesday, Thursday. 

Note that the M out of N cases mean for each available day, we have a choice 
about whether to use that person or not on that day - and that choice could 
potentially depend on demand elsewhere that week, i.e. we don't want to 
pick early in the week so we are short of volunteers at the end of the week. 

We also would like to spread the work amongst volunteers, so prefer to pick
volunteers who were less used in previous weeks rather than allocate work 
to the same volunteers each week. 



h2. Ambulances

The charity owns a fleet of ambulances, currently around 25. Availability of 
ambulances varies by day: some will be at the garage for maintenance, 
some may be booked for fundraising or promotional events, and at least
one will be kept as a reserve in case another ambulance breaks down. 

Generally, an ambulance will start the day in the possession of the 
driver allocated for that day. The evening before, the previous 
driver will "hand over" to the new driver, typically delivering the 
ambulance to the new driver and getting a lift back to his or her 
house. 

Sometimes, the previous and new driver are the same person. There 
are also occasions when an ambulance is not needed on a day, in which 
case we skip over the empty days to find the next or previous drivers. 
Weekends are a particular case - Friday's driver will need to hand over 
to Monday's driver at some point. 

In rare cases, ambulances may need to be collected from the charity's
HQ. 


Handover distances should normally be short, i.e. not requiring the previous 
driver to travel much further after a day of driving their normal schedule. 

Note that in order to keep driving distances short, it _might_ help
to "migrate" ambulances towards the locations of the patients with
upcoming appointments. For example, if there are patients soon in Durham, 
then picking the next volunteers closer to Durham means less driving
than picking ones towards Newcastle. But this is not absolute! 


h2. Drivers and companions

Generally, the companion will be picked after the driver. Quite often there 
will be a few suitable volunteers living near to the driver, though sometimes 
companions can be found closer to the first patient on a schedule, hence picked
up on the way to the first patient. 

Many couples do volunteer together, with one person driving and their partner 
as the companion. Generally, such couples should be allocated together or not 
at all, i.e. avoid placing these people in different ambulances or avoid 
allocating one person but not their partner. (Sometimes this rule is skipped
in emergencies, e.g. covering for a volunteer who is suddenly unavailable.)

Similarly, there are some people who prefer to avoid certain other volunteers.
Each volunteer has a list of 0 or more people with whom they should not be 
paired. 


h2. Patients and Appointments

Patients have a location and a set of scheduled appointments. When a patient
signs up for the service, we will get the series of appointments for their 
programme of treatment - typically a mix of radiotherapy, chemotherapy and 
review appointments. Most of a patient's appointments will be at the same
hospital but not always (appointments will indicate the hospital and a
room or department at that hospital). 

Appointment times are flexible to a degree, because of the nature of 
treatment. Just because someone is booked in at 10am does not mean they get
seen or treated at exactly that time: they might get in earlier if the 
treatment room or medical professional is available, or they may have to 
wait whilst another patient finishes their treatment. However, we don't 
have exact guidelines on what flexibility is allowed or is seen in practice.

Generally, we aim to get the patient to the hospital at least 20 minutes 
before their appointment time. 



h2. Combined journeys

Ambulances can carry up to three patients at a time. This allows us to 
transport patients in groups rather than make several similar, one-patient 
journeys - saving on driving time and allowing us to help more patients.
There are a few conditions and options. 

Firstly, the grouped patients need 
some similarity between their appointment windows. The times don't need to
match exactly - it's acceptable to have one patient wait for a reasonable 
period whilst the other patient is being treated, so grouping patients with 
appointment times of 2pm-2.30pm and 2.30pm-3pm is fine since it usually 
means a wait of under 30 minutes each (depending on how busy the relevant 
treatment room is). At present, we allow up to an hour of waiting on either 
side (on top of the 20 minute pre-appointment buffer). 

Grouped patients don't need to live close to each other. It's reasonable 
when driving in from picking up a further-away (from the hospital) patient 
to pick up a closer patient if the appointment windows are similar and the
detour does not add too much to the journey. For example, a journey could 
start with a patient in Darlington and then pick up a second patient in 
Durham, maybe a third patient in Washington.  At present we allow a detour 
up to 20% of the furthest patient's distance, though this is negotiable. 

It's also feasible that grouped patients will be going to different 
hospitals, if the detour to drop off the first patient won't add too 
much driving or wait time for the other patient(s). 


h2. Multiple journeys

An ambulance will often transport several groups of patients during 
a day, say a group in the morning and a group in the afternoon. There
will be some distance to drive from the first group's last drop-off and
the second group's first pickup, and driving this distance will take
time. We also allow a rest period between groups. 

Ideally, the amount of driving should be balanced between ambulances,
though this isn't always feasible, for other reasons. 


h2. Split journeys

Some appointments can last for three or more hours, possibly even up to a 
whole day - for example a complex treatment where the patient needs to 
be monitored for a few hours afterwards. Since the ambulance crew is not
required to stay with the patient through all of this time, they will often
leave and help to transport other suitably-close patients whilst waiting. 

More often than not, the crew will return later to bring the long-appointment
patient back home again.

Some patients might only need transport one way - typically when a friend or 
relative is able to help with the other part of the journey, though such cases 
are quite rare. 




h2. Distance from home

Care should be taken with the distances that drivers need to travel to 
their first patient or after dropping off their last patient. 
One particular case is where subsequent journeys take the driver further
away from home than his or her start point.

Where possible, drivers appreciate transporting patients who are close to 
them since it cuts down on driving time. In certain cases, we do allocate 
drivers to nearby patients with afternoon appointments, even if it means not
using those drivers in the morning. There is a balance to be found here. 


h2. Distance and speed

Ideally we'd use route-planning tools like Google to provide information about 
distances and driving times, possibly backed up with evidence from the satnav
boxes in the ambulances, but not got round to that and instead we're trying 
some approximations. 

We're using a simple calculation based on latitude and longtitude to estimate
the distance between two postcode points. It's basically Manhattan distance 
rather than crow-flies as a way to approximate extra distance for non-direct
road routes (but it does take account of local latitude when computing with 
longtitude). Because crossing the Tyne often involves a detour to the nearest
bridge, we add on a small distance penalty to represent the extra driving. 

Driving time depends on distance and speed. We also estimate the speed ambulances 
can go with a simple rule: short distances are done at 20mph (for city driving), 
medium distances at 30mph, and longer distances at 40mph (eg main roads). 

The above tend to over-estimate, but it does allow ambulances to get places 
without rushing! 



h2. Some thoughts about optimisation

To be continued...





