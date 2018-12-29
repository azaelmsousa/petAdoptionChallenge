# petAdoptionChallenge

Millions of stray animals suffer on the streets or are euthanized in shelters every day around the world. If homes can be 
found for them, many precious lives can be saved — and more happy families created. PetFinder.my has been Malaysia’s leading 
animal welfare platform since 2008, with a database of more than 150,000 animals. PetFinder collaborates closely with animal 
lovers, media, corporations, and global organizations to improve animal welfare.

Animal adoption rates are strongly correlated to the metadata associated with their online profiles, such as descriptive text 
and photo characteristics. As one example, PetFinder is currently experimenting with a simple AI tool called the Cuteness 
Meter, which ranks how cute a pet is based on qualities present in their photos.

Kaggle is now hosting a challenge to predict the rate of addoptness of a pet according to a variaty of features, including photo, 
breed, adoption fee and health. The rate is divided into 5 categories (0, 1, 2, 3 and 4). The main goal of this repository is
the development and experimentation of methods to address this problem.

## Data

To predict the pet's addoptness, a profile of each pet is given by the PetFinder. Sometimes a profile represents a group of 
pets. In this case, the speed of adoption is determined by the speed at which all of the pets are adopted. The data included 
text, tabular, and image data. See below for details.

### Data Fields

`PetID` - Unique hash ID of pet profile
`AdoptionSpeed` - Categorical speed of adoption. Lower is faster. This is the value to predict. See below section for more info.
`Type` - Type of animal (1 = Dog, 2 = Cat)
`Name` - Name of pet (Empty if not named)
`Age` - Age of pet when listed, in months
`Breed1` - Primary breed of pet (Refer to BreedLabels dictionary)
`Breed2` - Secondary breed of pet, if pet is of mixed breed (Refer to BreedLabels dictionary)
`Gender` - Gender of pet (1 = Male, 2 = Female, 3 = Mixed, if profile represents group of pets)
`Color1` - Color 1 of pet (Refer to ColorLabels dictionary)
`Color2` - Color 2 of pet (Refer to ColorLabels dictionary)
`Color3` - Color 3 of pet (Refer to ColorLabels dictionary)
`MaturitySize` - Size at maturity (1 = Small, 2 = Medium, 3 = Large, 4 = Extra Large, 0 = Not Specified)
`FurLength` - Fur length (1 = Short, 2 = Medium, 3 = Long, 0 = Not Specified)
`Vaccinated` - Pet has been vaccinated (1 = Yes, 2 = No, 3 = Not Sure)
`Dewormed` - Pet has been dewormed (1 = Yes, 2 = No, 3 = Not Sure)
`Sterilized` - Pet has been spayed / neutered (1 = Yes, 2 = No, 3 = Not Sure)
`Health` - Health Condition (1 = Healthy, 2 = Minor Injury, 3 = Serious Injury, 0 = Not Specified)
`Quantity` - Number of pets represented in profile
`Fee` - Adoption fee (0 = Free)
`State` - State location in Malaysia (Refer to StateLabels dictionary)
`RescuerID` - Unique hash ID of rescuer
`VideoAmt` - Total uploaded videos for this pet
`PhotoAmt` - Total uploaded photos for this pet
`Description` - Profile write-up for this pet. The primary language used is English, with some in Malay or Chinese.
