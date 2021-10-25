# Python-Classes-Medical-Insurance-Project

class Patient:
 def __init__(self, name, age, sex, bmi, num_of_children, smoker):
    self.name = name
    self.age = age
    # add more parameters here
    self.sex = sex
    self.bmi = bmi
    self.num_of_children = num_of_children
    self.smoker = smoker
 
 def estimated_insurance_cost(self):
  estimated_cost = 250 * self.age - 128 * self.sex + 370 * self.bmi + 425 * self.num_of_children + 24000 * self.smoker - 12500

  print("{}'s estimated insurance costs is {} dollars.".format(self.name, estimated_cost))
 
 def update_age(self, new_age):
  self.age = new_age
  self.estimated_insurance_cost()
  print("{} is now  is {} years old.".format(self.name, new_age))

 def patient_profile(self):
  patient_information = {}
  patient_information["Name"] = self.name
  patient_information["Age"] = self.age
  patient_information["Sex"] = self.sex
  patient_information["BMI"] = self.bmi
  patient_information["Number of Children"] = self.num_of_children
  patient_information["Smoker"] = self.smoker
  return patient_information


 def update_num_children(self, new_num_children):
  self.num_of_children = new_num_children
  self.estimated_insurance_cost()
  if self.num_of_children == 1:
   print("{} has {} child".format(self.name, self.num_of_children))
  else:
   print("{} has {} children".format(self.name, self.num_of_children))
patient1 = Patient("John Doe", 25, 1, 22.2, 0, 0)
 

 #def patient_profile(self):
  #patient_information = {}
  #patient_information["Name"] = self.name
  #patient_information["Age"] = self.age
  #patient_information["Sex"] = self.sex
  #patient_information["BMI"] = self.bmi
  #patient_information["Number of Children"] = self.num_of_children
  #patient_information["Smoker"] = self.smoker
  #return patient_information

print(patient1.name)
print(patient1.age)
print(patient1.sex) 
print(patient1.bmi)
print(patient1.num_of_children)
print(patient1.smoker)


patient1.estimated_insurance_cost()
patient1.update_age(26)
patient1.update_num_children(1)
print(patient1.patient_profile())




  