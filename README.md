# Calculated-College-Counselor
HackMHS
Want_Close_to_home = False
major = input("What major would you like to pursue? ")
WarmStates = ["AZ", "FL","TX","CA","SC","HA","GE","Al","LA"]
Weather = input("What weather would you like it to have? (Warm, Cold or Neither) ")
ColdStates = ["AK","ND","MN","ME","WY","MT","ID","VE","MI"]

maximum_tuition = input("What is the maximum amount of tuition you are willing to pay? ")
maximum_tuition = float(maximum_tuition)
LiveCloseToHome = input("Do only want to go to Univerisities close to New Jersey? ")
ClosetoNJ = ["NJ","NY","MA","PE","DE","MD","NH","RI","VA"]
LiveClosetoNJ = False
if LiveCloseToHome == "Yes" or LiveCloseToHome =="yes":
    LiveClosetoNJ = True

perfect = 0


if Weather == "Warm":
   Want_Warm = True
   Want_Cold = False
elif Weather == "Cold":
   Want_Cold = True
   Want_Warm = False
else:
   Want_Cold = False
   Want_Warm = False
colleges = []




class college:
   def __init__(self,name, tuition, acceptance_rate,state):
       global colleges
       self.name = name
       self.tuition = tuition
       self.acr = acceptance_rate
       self.st = state






   def get_name(self):
       return self.name
   def get_acr(self):
       return (100*self.acr)
   def get_tuition(self):
       return (self.tuition)
   def get_state(self):
       return self.st
   def too_expensive(self):
       global maximum_tuition
       if self.tuition > maximum_tuition:
           return True
def sell_college(name):
   global Justmajor, colleges, Want_Warm, Want_Cold, perfect


   for x in range (len(colleges)):
  
       if name == colleges[x]:
          
           if Want_Warm == True or Want_Cold == True:
               print ("")
               if perfect == 0:
                   perfect += 1
                  
                   return name.get_name() + " would be a great college for you, it fits your temperature conditions. It is in your price range, and it is one of the top universities in your respective field, I would recommend this for you "
               else:
                   return name.get_name() + " would also be a great college for you, it fits your temperature conditions. It is in your tuition range, and it is one of the top universities in your respective field, I would also reccomend this one for you "
           else:
               if perfect == 0:
                   perfect += 1
                  
                   return name.get_name() + " would be a great college for you. It is in your price range, and it is one of the top universities in your respective field, I would recommend this for you "
               else:
                   return name.get_name() + " would also be a great college for you, It is in your tuition range, and it is one of the top universities in your respective field, I would also reccomend this one for you "
def sell_expensive():
   global Justmajor
   return "If price and toughness is not a problem, I would recomend " + (Justmajor[0].get_name()) + ", because it is the highest ranked college for this field. It costs  "  
Princeton_University = college("Princeton University", 59710, 0.06, "NJ")
Massachusetts_Institute_of_Technology = college("Massachusetts Institute of Technology",60156,0.04,"MA")
Harvard_University = college("Harvard University",59076,0.03, "MA")
Standford_University = college("Standford University",62484,0.04,"CA")
Yale_University = college("Yale University", 64700,0.05, "CT")
University_of_Pennsylvania = college("University of Pennsylvania", 66104,0.07,"PA")
California_Institute_of_Technology = college("California Institute of Technology",63255,0.03,"CA")
Duke_University = college("Duke University",66172,0.06,"NC")
Brown_University = college("Brown University",68230,0.05,"RI")
Johns_Hopkins_University = college("Johns Hopkins University",63340,0.07,"MD")
Northwestern_University = college("Northwestern University",65997,0.07,"IL")
Columbia_University = college("Columbia University",65524,0.04,"NY")
Cornell_University = college("Cornell University",66014,0.07,"NY")
University_of_Chicago = college("University of Chicago",65619,0.05,"IL")
University_of_California_Berkeley = college("University of California, Berkeley",48465,0.11,"CA")
University_of_California_Los_Angeles = college("University of California, Los Angeles",46326,0.09,"CA")
Rice_University = college("Rice_University",58128,0.09,"TX")
Dartmouth_College = college("Dartmouth College",65511,0.06,"NH")
Vanderbilt_University = college("Vanderbilt University",63946,0.07,"TN")
University_of_Notre_Dame = college("University of Notre Dame",62693,0.13,"IN")
University_of_Michigan_Ann_Arbor = college("University of Michigan Ann Arbor",57273,0.18,"MI")
Georgetown_University = college("Georgetown University",65082,0.12,"DC")
University_of_North_Carolina_Chapel_Hill = college("University of North Carolina Chapel Hill",39338,0.17,"NC")
Carnegie_Mellon_University = college("Carnegie Mellon University",63829,0.11,"PA")
Emory_University = college("Emory University",60774,0.11,"GA")
University_of_Virginia = college("University of Virginia",58950,0.19,"VA")
Washington_University_in_St_Louis = college("Washington University in St Louis",62982,0.11,"MO")
University_of_California_San_Diego = college("University of California San Diego",48630,0.24,"CA")
University_of_California_Davis = college("University of California",48360,0.24,"CA")
University_of_Florida = college("University of Florida",28658,0.23,"FL")
University_of_Southern_California = college("University of Southern California",68237,0.12,"CA")
University_of_Texas_at_Austin = college("University of Texas at Austin",41070,0.31,"TX")
Georgia_Institute_of_Technology = college("Georgia Institute of Technology",32876,0.17,"GA")
University_of_California_Irvine = college("University of California Irvine",47759,0.21,"CA")
New_York_University = college("New York University",60438,0.12,"NY")
University_of_California_Santa_Barbara = college("University of California Santa Barabara",45658,0.26,"CA")
University_of_Illinois_Urbana_Champagne = college("University of Illinois Urbana Champange",36068,0.45,"IL")
University_of_Wisconsin_Madison = college("University of Wisconsin Madison",40603,0.49,"WI")
Boston_College = college("Boston College",67680,0.17,"MA")
Rutgers_University = college("Rutgers University",36001,0.66,"NJ")
Tufts_University = college("Tufts University",67844,0.10,"MA")
University_of_Washington = college("University of Washington",41997,0.48,"WA")
Boston_University = college("Boston University",65168,0.14,"MA")
Ohio_State_University = college("Ohio State University",36722,0.53,"OH")
Purdue_University = college("Purdue University",28794,0.53,"IN")
University_of_Maryland_College_Park = college("University of Maryland College Park",40306,0.44,"MD")
Lehigh_University = college("Lehigh University",62180,0.37,"PA")
Texas_AandM_University = college("Texas A&M University",40607,0.63,"TX")
University_of_Georgia = college("University of Georgia",30220,0.43,"GA")
University_of_Rochester = college("University of Rochester",64384,0.39,"NY")
Virginia_Tech = college("Virginia Tech",36090,0.57,"VA")
Wake_Forest_University = college("Wake Forest University",64758,0.21,"NC")
Case_Western_Reserve_University = college("Case Western Reserve University",62234,0.27,"OH")
Florida_State_University = college("Florida State University",21683,0.25,"FL")
Northeastern_University = college("Northeastern University",63141,0.07,"MA")
University_of_Minnesota_Twin_Cities = college("University of Minnesota Twin Cities",36402,0.75,"MN")
William_and_Mary = college("William & Mary",48841,0.33,"VA")
Stony_Brook_University = college("Stony Brook University",30350,0.49,"NY")
University_of_Connecticut = college("University of Connecticut",43034,0.55,"CT")
Brandeis_University = college("Brandeis University",62722,0.39,"MA")
Michigan_State_University = college("Michigan State University",41958,0.88,"MI")
North_Carolina_State_University = college("North Carolina State University", 31976,0.47,"NC")
Pennsylvania_State_University = college("Pennsylvania State University",38651,0.55,"PA")
Rensselear_Polytechnic_Institute = college("Rensselear Polytechnic Institute",61884,0.65,"NY")
Santa_Clara_University = college("Santa Clara University",59241,0.52,"CA")
University_of_California_Merced = college("University of California Merced",43777,0.89,"CA")
George_Washington_University = college("George Washington University",64990,0.49,"DC")
Syracuse_University = college("Syracuse University",63061,0.52,"NY")
University_of_Massachusettes_Amherst = college("University of Massachusettes Amherst",39293,0.64,"MA")
University_of_Miami = college("University of Miami",59926,0.19,"FL")
University_of_Pittsburgh = college("University of Pittsburgh",39890,0.49,"PA")
Villanova_University = college("Villanova_University",64906,0.23,"PA")
Binghamton_University_SUNY = college("Binghamton University SUNY",28203,0.42,"NY")
Indiana_University_Bloomington = college("Indiana University Bloomington",40482,0.82,"IN")
Tulane_University = college("Tulane University",65538,0.11,"LA")
Colorado_School_of_Mines = college("Colorado School of Mines",42120,0.58,"CO")
Pepperdine_University = college("Pepperdine University",66742,0.49,"CA")
Stevens_Institute_of_Technology = college("Stevens Institute of Technology",600952,0.46,"NJ")
University_at_Buffalo_SUNY = college("University_at_Buffalo_SUNY",30571,0.68,"NY")
University_of_California_Riverside = college("University of California Riverside",46266,0.69,"CA")
University_of_Delaware = college("University of Delaware",39720,0.72,"DE")
Rutgers_University_Newark = college("Rutgers_University_Newark",35348,0.74,"NJ")
University_of_California_Santa_Cruz = college("University of California Santa Cruz",47862,0.47,"CA")
University_of_Illinois_Chicago = college("University of Illinois Chicago",32833,0.79,"IL")
Worcester_Polytechnic_Institute = college("Worcester Polytechnic Institute",58870,0.57,"MA")
Clemson_University = college("Clemson University",39502,0.43,"SC")
Marquette_University = college("Marquette University",48700,0.87,"WI")
New_Jersey_Institute_of_Technology = college("New Jersey Institute of Technology",61567,0.54,"NY")
Fordham_University = college("Fordham University",61567,0.54,"NY")
Southern_Methodist_University = college("Southern Methodist University",64460,0.52,"TX")
Temple_University = college("Temple University",35956,0.80,"PA")
University_of_South_Florida = college("University of South Florida",17324,0.44,"FL")
Auburn_University = college("Auburn University",33944,0.44,"AL")
Baylor_University = college("Baylor University",54844,0.46,"TX")
Gonzaga_University = college("Gonzaga University",53500,0.70,"WA")
Loyola_Marymount_University = college("Loyola Marymount University",58489,0.41,"CA")
University_of_Iowa = college("University of Iowa",32927,0.86,"IA")
Drexel_University =  college("Drexel University",60663,0.80,"PA")
Illinois_Institute_of_Technology = college("Illinois Institute of Technology",51763,0.61,"IL")
Rochester_Institute_of_Technology = college("Rochester Institute of Technology",57016,0.67,"NY")




#The following would be the majors
Business_and_Management = [University_of_Chicago,Standford_University,Northwestern_University,Harvard_University,University_of_Pennsylvania,Dartmouth_College,Columbia_University, Massachusetts_Institute_of_Technology,Cornell_University,University_of_Michigan_Ann_Arbor,University_of_California_Berkeley,Yale_University,University_of_Virginia,Duke_University,University_of_North_Carolina_Chapel_Hill,University_of_California_Los_Angeles, Carnegie_Mellon_University, University_of_Texas_at_Austin,Indiana_University_Bloomington,New_York_University]
Nursing = [Johns_Hopkins_University,Duke_University,University_of_Washington,Rutgers_University_Newark,Emory_University,University_of_Michigan_Ann_Arbor,University_of_Minnesota_Twin_Cities,University_of_Pennsylvania,University_of_Pittsburgh,University_of_Illinois_Chicago,New_York_University,Vanderbilt_University,Case_Western_Reserve_University,University_of_North_Carolina_Chapel_Hill,Ohio_State_University,University_of_Southern_California,University_of_Iowa,Purdue_University,Boston_College]
Psychology = [Standford_University,University_of_California_Berkeley,Harvard_University,University_of_California_Los_Angeles,University_of_Michigan_Ann_Arbor,Princeton_University,University_of_Illinois_Urbana_Champagne,Yale_University,Cornell_University,Northwestern_University,University_of_Wisconsin_Madison,Columbia_University,Duke_University,Johns_Hopkins_University,University_of_California_Davis,University_of_Chicago,University_of_California_San_Diego,University_of_Minnesota_Twin_Cities,University_of_North_Carolina_Chapel_Hill,University_of_Pennsylvania,Vanderbilt_University,Brown_University]
Biology = [Harvard_University,Massachusetts_Institute_of_Technology,Standford_University,University_of_California_Berkeley,University_of_California_San_Diego,University_of_Washington,Johns_Hopkins_University,University_of_California_Los_Angeles,Cornell_University,Columbia_University,University_of_Pennsylvania,Yale_University,University_of_Michigan_Ann_Arbor, New_York_University,University_of_Washington,Duke_University,California_Institute_of_Technology,University_of_North_Carolina_Chapel_Hill,University_of_California_Davis]
Engineering = [Massachusetts_Institute_of_Technology, Standford_University,University_of_California_Berkeley,Purdue_University,Carnegie_Mellon_University,Georgia_Institute_of_Technology,California_Institute_of_Technology,University_of_Michigan_Ann_Arbor,University_of_Texas_at_Austin,Texas_AandM_University,University_of_Illinois_Urbana_Champagne,University_of_California_San_Diego,Cornell_University,Johns_Hopkins_University,University_of_Southern_California,University_of_California_Los_Angeles,Columbia_University,Northwestern_University,University_of_Maryland_College_Park,University_of_Pennsylvania,Duke_University]
Education = [Columbia_University,University_of_Wisconsin_Madison,University_of_California_Los_Angeles,University_of_Michigan_Ann_Arbor,Northwestern_University,Vanderbilt_University,University_of_Pennsylvania,Harvard_University,Johns_Hopkins_University,New_York_University,Standford_University,University_of_Texas_at_Austin,University_of_Virginia,Florida_State_University,University_of_California_Berkeley,University_of_Florida,University_of_California_Irvine,Michigan_State_University,Ohio_State_University]
Communications = [Massachusetts_Institute_of_Technology,Standford_University,University_of_Pennsylvania,Brown_University,Northwestern_University,Cornell_University,University_of_California_Berkeley,University_of_California_Los_Angeles,Vanderbilt_University,University_of_Michigan_Ann_Arbor,University_of_North_Carolina_Chapel_Hill,Emory_University,University_of_Virginia,University_of_California_San_Diego,University_of_Southern_California,University_of_Texas_at_Austin,New_York_University,University_of_California_Santa_Barbara,University_of_Illinois_Urbana_Champagne,University_of_Wisconsin_Madison]
Finance_and_Accounting = [Harvard_University,Massachusetts_Institute_of_Technology,Standford_University,University_of_Chicago,University_of_Pennsylvania,University_of_California_Berkeley,New_York_University,Columbia_University,Yale_University,University_of_California_Los_Angeles,Princeton_University,Northwestern_University,Cornell_University,University_of_Michigan_Ann_Arbor,University_of_Texas_at_Austin,Duke_University,University_of_Illinois_Urbana_Champagne,University_of_Southern_California,University_of_Washington,Ohio_State_University]
Criminal_Justice = [Rutgers_University,Boston_University,Georgia_Institute_of_Technology,Florida_State_University,Northeastern_University,Michigan_State_University,Pennsylvania_State_University,George_Washington_University,Villanova_University,Indiana_University_Bloomington,Rutgers_University_Newark,University_of_Illinois_Chicago,Temple_University,Drexel_University,Rochester_Institute_of_Technology]
Anthropology_and_Sociology = [Princeton_University,Massachusetts_Institute_of_Technology,Harvard_University,Standford_University,University_of_Pennsylvania,Duke_University,Brown_University,Johns_Hopkins_University,Columbia_University,Cornell_University,University_of_Chicago,University_of_California_Berkeley,University_of_California_Los_Angeles,Rice_University,Dartmouth_College,Vanderbilt_University,University_of_Notre_Dame,University_of_Michigan_Ann_Arbor]
Computer_Science = [Carnegie_Mellon_University,Massachusetts_Institute_of_Technology,Standford_University,University_of_California_Berkeley,University_of_Illinois_Urbana_Champagne,Cornell_University,Georgia_Institute_of_Technology,University_of_Texas_at_Austin,University_of_Washington,Princeton_University,University_of_Michigan_Ann_Arbor,Columbia_University,California_Institute_of_Technology,University_of_California_Los_Angeles,University_of_California_San_Diego,University_of_Wisconsin_Madison,Harvard_University,University_of_Maryland_College_Park,Purdue_University,Pennsylvania_State_University]
English = [University_of_California_Berkeley,Yale_University,Harvard_University,Princeton_University,Standford_University,University_of_Chicago,University_of_Pennsylvania,Columbia_University,Cornell_University,University_of_Michigan_Ann_Arbor,University_of_California_Los_Angeles,University_of_Virginia,Brown_University,Duke_University,Johns_Hopkins_University,Northwestern_University,Rutgers_University,University_of_Texas_at_Austin,New_York_University,University_of_California_Irvine]
Economics = [Harvard_University,Massachusetts_Institute_of_Technology,Standford_University,Princeton_University,University_of_California_Berkeley,University_of_Chicago,Yale_University,Northwestern_University,Columbia_University,University_of_Pennsylvania,New_York_University,University_of_California_Los_Angeles,University_of_Michigan_Ann_Arbor,California_Institute_of_Technology,Cornell_University,University_of_California_San_Diego,University_of_Wisconsin_Madison,Duke_University,University_of_Minnesota_Twin_Cities,Brown_University]
Political_Science = [Standford_University,Harvard_University,Princeton_University,University_of_California_Berkeley,University_of_Michigan_Ann_Arbor,Yale_University,Massachusetts_Institute_of_Technology,Columbia_University,University_of_California_San_Diego,Duke_University,University_of_Chicago,University_of_California_Los_Angeles,University_of_North_Carolina_Chapel_Hill,Washington_University_in_St_Louis,Cornell_University,New_York_University,Ohio_State_University,University_of_Wisconsin_Madison,Emory_University,Northwestern_University,University_of_Pennsylvania]
History = [Princeton_University,Massachusetts_Institute_of_Technology,Harvard_University,Standford_University,Yale_University,University_of_Pennsylvania,California_Institute_of_Technology,Duke_University,Brown_University,Johns_Hopkins_University,Northwestern_University,Columbia_University,Cornell_University,University_of_Chicago,University_of_California_Berkeley,University_of_California_Los_Angeles,Rice_University,Dartmouth_College,Vanderbilt_University,University_of_Notre_Dame]
Kinesiology_and_Physical_Therapy = [Washington_University_in_St_Louis,University_of_Delaware,University_of_Iowa,Emory_University,Northwestern_University,Duke_University,University_of_Southern_California,Ohio_State_University,University_of_Pittsburgh,Boston_University,University_of_Florida,University_of_Miami,University_of_North_Carolina_Chapel_Hill,Marquette_University,Columbia_University,University_of_Wisconsin_Madison,George_Washington_University,University_of_Washington,Northeastern_University,Rutgers_University_Newark,University_of_Minnesota_Twin_Cities]
Health_Professions = [Rice_University,University_of_Michigan_Ann_Arbor,University_of_North_Carolina_Chapel_Hill,Emory_University,University_of_Virginia,University_of_Florida,University_of_Illinois_Urbana_Champagne,University_of_Wisconsin_Madison,Rutgers_University,Ohio_State_University,Purdue_University,University_of_Maryland_College_Park,Texas_AandM_University,University_of_Georgia,Wake_Forest_University,Florida_State_University,University_of_Minnesota_Twin_Cities,William_and_Mary,University_of_Connecticut]
Art = [University_of_California_Los_Angeles,Yale_University,Carnegie_Mellon_University,University_of_Michigan_Ann_Arbor,Columbia_University,University_of_California_San_Diego,University_of_California_Berkeley,University_of_California_Davis,University_of_Wisconsin_Madison,Rochester_Institute_of_Technology,Rutgers_University,University_of_Iowa,University_of_Texas_at_Austin,Washington_University_in_St_Louis,Boston_University,Indiana_University_Bloomington,Ohio_State_University,Standford_University,Temple_University,University_of_Georgia,University_of_Washington]
Math = [Standford_University,Massachusetts_Institute_of_Technology,Princeton_University,Harvard_University,University_of_California_Berkeley,Columbia_University,University_of_California_Los_Angeles,University_of_Washington,New_York_University,Texas_AandM_University,University_of_Chicago,University_of_Michigan_Ann_Arbor,University_of_Wisconsin_Madison,University_of_Texas_at_Austin,University_of_Minnesota_Twin_Cities,Purdue_University,Brown_University,University_of_Pennsylvania,Pennsylvania_State_University,Duke_University]
Environmental_Science = [Harvard_University,Standford_University,University_of_California_Berkeley,Yale_University,University_of_Minnesota_Twin_Cities,University_of_Washington,University_of_California_Davis,University_of_California_Santa_Barbara,University_of_Florida,Princeton_University,Duke_University,Cornell_University,University_of_California_Los_Angeles,University_of_Wisconsin_Madison,Massachusetts_Institute_of_Technology,Columbia_University,University_of_Michigan_Ann_Arbor,Michigan_State_University,University_of_Maryland_College_Park,University_of_California_Irvine]
Foreign_Languages = [University_of_Notre_Dame,Columbia_University,Vanderbilt_University,University_of_Virginia,University_of_California_Los_Angeles,Duke_University,Georgetown_University,University_of_Southern_California,University_of_California_Berkeley,University_of_Illinois_Urbana_Champagne,University_of_Wisconsin_Madison,Brown_University,Tufts_University,Southern_Methodist_University,University_of_Florida,New_York_University,University_of_Chicago,University_of_California_Davis,University_of_Pittsburgh,University_of_Washington]
Design = [Duke_University,University_of_California_Los_Angeles,University_of_Notre_Dame,University_of_Michigan_Ann_Arbor,Carnegie_Mellon_University,Washington_University_in_St_Louis,University_of_California_Davis,University_of_Florida,University_of_Southern_California,University_of_Texas_at_Austin,University_of_California_Irvine,New_York_University,University_of_Illinois_Urbana_Champagne,University_of_Wisconsin_Madison,Rutgers_University,University_of_Washington,Boston_University,Ohio_State_University,Purdue_University,Lehigh_University,Virginia_Tech]
Trades_and_Personal_Services = [New_York_University,Johns_Hopkins_University,Cornell_University,University_of_Texas_at_Austin,University_of_Wisconsin_Madison,Florida_State_University,Purdue_University,Ohio_State_University,Loyola_Marymount_University,University_of_Minnesota_Twin_Cities,Pennsylvania_State_University,North_Carolina_State_University,Worcester_Polytechnic_Institute,Syracuse_University,Baylor_University]
International_Relations = [Standford_University,Yale_University,University_of_Pennsylvania,Brown_University,Johns_Hopkins_University,Northwestern_University,University_of_Chicago,Georgetown_University,Carnegie_Mellon_University,Emory_University,University_of_Virginia,Washington_University_in_St_Louis,University_of_California_Davis,University_of_California_San_Diego,University_of_Southern_California,Georgia_Institute_of_Technology,Northwestern_University,Tufts_University,Boston_University,Ohio_State_University,Lehigh_University]
Chemistry = [California_Institute_of_Technology,Massachusetts_Institute_of_Technology, University_of_California_Berkeley,Harvard_University,Standford_University,Northwestern_University,Princeton_University,University_of_Chicago,University_of_Illinois_Urbana_Champagne,Columbia_University,Cornell_University, Yale_University,University_of_Michigan_Ann_Arbor,University_of_Wisconsin_Madison,University_of_California_Los_Angeles,University_of_North_Carolina_Chapel_Hill,Pennsylvania_State_University,University_of_Texas_at_Austin,Georgia_Institute_of_Technology,Georgia_Institute_of_Technology,Johns_Hopkins_University]
Agricultural_Sciences = [University_of_Massachusettes_Amherst,Cornell_University,University_of_California_Davis,University_of_Florida,Harvard_University,University_of_Illinois_Urbana_Champagne,Michigan_State_University,Purdue_University,University_of_Wisconsin_Madison,Ohio_State_University,Texas_AandM_University,University_of_Minnesota_Twin_Cities,Rutgers_University,North_Carolina_State_University,Pennsylvania_State_University,University_of_Georgia,University_of_Maryland_College_Park,Tufts_University,Johns_Hopkins_University,University_of_California_Berkeley]
Technology = [Carnegie_Mellon_University,New_York_University,Georgetown_University,Georgia_Institute_of_Technology,Washington_University_in_St_Louis,George_Washington_University,Johns_Hopkins_University,University_of_Virginia,Southern_Methodist_University,Cornell_University,Columbia_University,Northeastern_University,University_of_Pittsburgh,Drexel_University,Stevens_Institute_of_Technology,University_of_Miami,Brandeis_University,University_of_Southern_California,Rochester_Institute_of_Technology, University_of_Texas_at_Austin]
Performing_Arts = [New_York_University,Rochester_Institute_of_Technology,Harvard_University,Yale_University,Columbia_University,Standford_University,Northwestern_University,University_of_Southern_California,University_of_Michigan_Ann_Arbor,University_of_California_Los_Angeles,University_of_California_Berkeley,Boston_University,Indiana_University_Bloomington,Massachusetts_Institute_of_Technology,University_of_California_San_Diego,University_of_Chicago,University_of_Texas_at_Austin,Cornell_University,Princeton_University, University_of_Illinois_Urbana_Champagne]
Food_and_Nutrition = [University_of_North_Carolina_Chapel_Hill,University_of_California_Davis,New_York_University,University_of_Illinois_Urbana_Champagne,Ohio_State_University,Virginia_Tech,Case_Western_Reserve_University,University_of_Minnesota_Twin_Cities,Syracuse_University,University_of_Delaware,Baylor_University,Rochester_Institute_of_Technology, Rutgers_University, Princeton_University, Stevens_Institute_of_Technology,New_Jersey_Institute_of_Technology]
Religious_Studies = [Princeton_University,Harvard_University,Standford_University,Yale_University,University_of_Pennsylvania,Duke_University,Brown_University,Northwestern_University,Columbia_University,Cornell_University,University_of_Chicago,University_of_California_Los_Angeles,Rice_University,Dartmouth_College,Vanderbilt_University,University_of_Michigan_Ann_Arbor,Georgetown_University,University_of_North_Carolina_Chapel_Hill,Emory_University,University_of_Virginia]
Film_and_Photography = [Yale_University,New_York_University,University_of_Southern_California,University_of_Pennsylvania,Dartmouth_College,University_of_Chicago,Washington_University_in_St_Louis,Tufts_University,University_of_California_Los_Angeles,University_of_Michigan_Ann_Arbor,Emory_University,Vanderbilt_University,University_of_Miami,University_of_California_Irvine,University_of_California_Berkeley,Loyola_Marymount_University,Boston_University,Boston_College,University_of_California_Santa_Barbara,Tulane_University]
Music = [Princeton_University,Massachusetts_Institute_of_Technology,Harvard_University,Standford_University,Yale_University,University_of_Pennsylvania,Duke_University,Brown_University,Johns_Hopkins_University,Northwestern_University,Columbia_University,Cornell_University,University_of_Chicago,University_of_California_Berkeley,University_of_California_Los_Angeles,Rice_University,Dartmouth_College,Vanderbilt_University]
Physics = [Massachusetts_Institute_of_Technology,Standford_University,California_Institute_of_Technology,Harvard_University,Princeton_University,University_of_California_Berkeley,Cornell_University,University_of_Chicago,Columbia_University,University_of_California_Santa_Barbara,University_of_Illinois_Urbana_Champagne,Yale_University,Johns_Hopkins_University,University_of_Michigan_Ann_Arbor,University_of_Pennsylvania,University_of_Texas_at_Austin,University_of_California_Los_Angeles,University_of_Maryland_College_Park,University_of_Washington]
Philosophy = [Columbia_University,Standford_University,Yale_University,Harvard_University,University_of_California_Los_Angeles,University_of_Chicago,Princeton_University,University_of_Pennsylvania,Rice_University,Duke_University,University_of_Southern_California,Dartmouth_College,Georgetown_University,Northwestern_University,University_of_Michigan_Ann_Arbor,Vanderbilt_University,New_York_University,Carnegie_Mellon_University,Brown_University]
Architecture = [Cornell_University,Rice_University,Washington_University_in_St_Louis,University_of_California_Berkeley,Yale_University,University_of_Southern_California,Virginia_Tech,Carnegie_Mellon_University,University_of_Virginia,Massachusetts_Institute_of_Technology,Texas_AandM_University,University_of_Florida,University_of_Notre_Dame,Georgia_Institute_of_Technology,Clemson_University,University_of_Miami,University_of_Michigan_Ann_Arbor,Columbia_University,University_of_Illinois_Urbana_Champagne]
Legal_Studies = [Vanderbilt_University,Northwestern_University,University_of_Miami,Tulane_University,University_of_Massachusettes_Amherst,University_of_California_Berkeley,University_of_Washington,University_of_Wisconsin_Madison,University_of_Pittsburgh,Temple_University,Purdue_University,Michigan_State_University,Pennsylvania_State_University,University_of_California_Santa_Cruz,Drexel_University,University_of_Massachusettes_Amherst,Auburn_University,New_Jersey_Institute_of_Technology,Texas_AandM_University,University_of_Georgia]
Pharmacy = [University_of_Michigan_Ann_Arbor,Northeastern_University,Ohio_State_University,University_of_California_Irvine,University_of_Pittsburgh,University_of_Georgia,Purdue_University,University_of_Connecticut,Clemson_University,University_of_Washington,University_of_Maryland_College_Park,Temple_University]




if major == "Business" or major == "Managment" or major == "Business and Management":
   listlenth = len(Business_and_Management)
   for x in range (listlenth):
       colleges.append(Business_and_Management[x])
elif major == "Nursing":
   listlenth = len(Nursing)
   for x in range (listlenth):
       colleges.append(Nursing[x])
elif major == "Psychology":
   listlenth = len(Psychology)
   for x in range (listlenth):
       colleges.append(Psychology[x])   
elif major == "Biology":
   listlenth = len(Biology)
   for x in range (listlenth):
       colleges.append(Biology[x])
elif major == "Engineering":
   listlenth = len(Engineering)
   for x in range (listlenth):
       colleges.append(Engineering[x])
elif major == "Education":
   listlenth = len(Education)
   for x in range (listlenth):
       colleges.append(Education[x])
elif major == "Communications":
   listlenth = len(Communications)
   for x in range (listlenth):
       colleges.append(Communications[x])
elif major == "Finace" or major == "Accounting" or major == "Finance and Accounting":
   listlenth = len(Finance_and_Accounting)
   for x in range (listlenth):
       colleges.append(Finance_and_Accounting[x])
elif major == "Criminal Justice":
   listlenth = len(Criminal_Justice)
   for x in range (listlenth):
       colleges.append(Criminal_Justice[x])
elif major == "Anthropology" or major == "Sociology" or major == "Anthropology and Sociology":
   listlenth = len(Anthropology_and_Sociology)
   for x in range (listlenth):
       colleges.append(Anthropology_and_Sociology[x])
elif major == "Computer Science":
   listlenth = len(Computer_Science)
   for x in range (listlenth):
       colleges.append(Computer_Science[x])
elif major == "English":
   listlenth = len(English)
   for x in range (listlenth):
       colleges.append(English[x])
elif major == "Economics":
   listlenth = len(Economics)
   for x in range (listlenth):
       colleges.append(Economics[x])
elif major == "Political Science":
   listlenth = len(Political_Science)
   for x in range (listlenth):
       colleges.append(Political_Science[x])
elif major == "History":
   listlenth = len(History)
   for x in range (listlenth):
       colleges.append(History[x])
elif major == "Kinesiology" or major == "Physical Therapy" or major == "Kinesiology and Physical Therapy":
   listlenth = len(Kinesiology_and_Physical_Therapy)
   for x in range (listlenth):
       colleges.append(Kinesiology_and_Physical_Therapy[x])
elif major == "Health Professions":
   listlenth = len(Health_Professions)
   for x in range (listlenth):
       colleges.append(Health_Professions[x])
elif major == "Art":
   listlenth = len(Art)
   for x in range (listlenth):
       colleges.append(Art[x])
elif major == "Math":
   listlenth = len(Math)
   for x in range (listlenth):
       colleges.append(Math[x])
elif major == "Enviormental Science":
   listlenth = len(Environmental_Science)
   for x in range (listlenth):
       colleges.append(Environmental_Science[x])
elif major == "Foreign Languages":
   listlenth = len(Foreign_Languages)
   for x in range (listlenth):
       colleges.append(Foreign_Languages[x])
elif major == "Design":
   listlenth = len(Design)
   for x in range (listlenth):
       colleges.append(Design[x])
elif major == "Trades" or major == "Personal Services" or major == "Trades and Personal Services":
   listlenth = len(Trades_and_Personal_Services)
   for x in range (listlenth):
       colleges.append(Trades_and_Personal_Services[x])
elif major == "International Relations":
   listlenth = len(International_Relations)
   for x in range (listlenth):
       colleges.append(International_Relations[x])
elif major == "Chemistry":
   listlenth = len(Chemistry)
   for x in range (listlenth):
       colleges.append(Chemistry[x])
elif major == "Agricultural Sciences":
   listlenth = len(Agricultural_Sciences)
   for x in range (listlenth):
       colleges.append(Agricultural_Sciences[x])
elif major == "Technology":
   listlenth = len(Technology)
   for x in range (listlenth):
       colleges.append(Technology[x])
elif major == "Performing Arts":
   listlenth = len(Performing_Arts)
   for x in range (listlenth):
       colleges.append(Performing_Arts[x])
elif major == "Food" or major == "Nutrition" or major == "Food and Nutrition":
   listlenth = len(Food_and_Nutrition)
   for x in range (listlenth):
       colleges.append(Food_and_Nutrition[x])
elif major == "Religious Studies":
   listlenth = len(Religious_Studies)
   for x in range (listlenth):
       colleges.append(Religious_Studies[x])
elif major == "Film" or major == "Photography" or major == "Film and Photography":
   listlenth = len(Film_and_Photography)
   for x in range (listlenth):
       colleges.append(Film_and_Photography[x])
elif major == "Music":
   listlenth = len(Music)
   for x in range (listlenth):
       colleges.append(Music[x])
elif major == "Physics":
   listlenth = len(Physics)
   for x in range (listlenth):
       colleges.append(Physics[x])
elif major == "Philosophy":
   listlenth = len(Philosophy)
   for x in range (listlenth):
       colleges.append(Philosophy[x])
elif major == "Architecture":
   listlenth = len(Architecture)
   for x in range (listlenth):
       colleges.append(Architecture[x])
elif major == "Legal Studies":
   listlenth = len(Legal_Studies)
   for x in range (listlenth):
       colleges.append(Legal_Studies[x])
elif major == "Pharmacy":
   listlenth = len(Pharmacy)
   for x in range (listlenth):
       colleges.append(Pharmacy[x])
for x in range (len(colleges)):
   print (colleges[x].get_name())
Justmajor = colleges
print ("")
removed = []
for x in range (len(colleges)):
   if (colleges[x]).too_expensive():
       removed.append(colleges[x])
for x in range (len(removed)):
   colleges.remove(removed[x])
for x in range (len(colleges)):
   print (colleges[x].get_name())
print("")
priceremoved = removed
removed = []
safe = []
for x in range (len(colleges)):
   if Want_Cold == True:
       for y in range (9):
           if colleges[x].get_state() == WarmStates[y]:
               removed.append(colleges[x])
   elif Want_Warm == True:
       for y in range (9):
           if colleges[x].get_state() == ColdStates[y]:
               removed.append(colleges[x])
for x in range (len(removed)):
   colleges.remove(removed[x])
if LiveClosetoNJ:
    for x in range (len(colleges)):
        for y in range (9):
            if colleges[x] == ClosetoNJ[y]:
                safe.append(colleges[x])
    colleges = []
    colleges = safe



for x in range (len(colleges)):
   print (sell_college(colleges[x]))
print( sell_expensive() )
print(Justmajor[0].get_tuition() + " dollars a year, and it also has")
print("dollars a year, and it also has a ")
print(Justmajor[0].get_acr())
print("percent acceptance rate so it might be hard to get into it")
