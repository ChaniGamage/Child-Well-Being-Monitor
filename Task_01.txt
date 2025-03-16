CREATE DATABASE Younglifes
GO


--Clean Database

-- Add Country Column 

--Vietnam

select*
from vietnam_constructed;

alter table [dbo].[vietnam_constructed]
add Country Varchar(50);

Update [dbo].[vietnam_constructed]
Set Country='Vietnam'
WHERE country IS NULL OR country =''

Select Country
From [dbo].[vietnam_constructed]

--Ethiopia

alter table [dbo].[ethiopia_constructed]
add Country Varchar(50);

Update [dbo].[ethiopia_constructed]
Set Country='Ethiopia'
WHERE country IS NULL OR country =''

Select Country
From [dbo].[ethiopia_constructed]

SELECT *
FROM [dbo].[vietnam_constructed]


	--- Clean dataset for vietnam
UPDATE [dbo].[vietnam_constructed]
SET 
    country = COALESCE(NULLIF(country, ''), 'NA'),
    childid = COALESCE(NULLIF(childid, ''), 'NA'),
    chsex = COALESCE(NULLIF(chsex, ''), 'NA'),
	bwght = COALESCE(NULLIF(bwght, ''), 'NA'),
    agemon = COALESCE(NULLIF(agemon, ''), 'NA'),
    chweight = COALESCE(NULLIF(chweight, ''), 'NA'),
    chheight = COALESCE(NULLIF(chheight, ''), 'NA'),
    bmi = COALESCE(NULLIF(bmi, ''), 'NA'),
    zwfa = COALESCE(NULLIF(zwfa, ''), 'NA'),
    zhfa = COALESCE(NULLIF(zhfa, ''), 'NA'),
    foodsec = COALESCE(NULLIF(foodsec, ''), 'NA'),
    region = COALESCE(NULLIF(region, ''), 'NA'),
    commid = COALESCE(NULLIF(commid, ''), 'NA'),
    clustid = COALESCE(NULLIF(clustid, ''), 'NA'),
    chillness = COALESCE(NULLIF(chillness, ''), 'NA'),
    chinjury = COALESCE(NULLIF(chinjury, ''), 'NA'),
    yc = COALESCE(NULLIF(yc, ''), 'NA'),
    deceased = COALESCE(NULLIF(deceased, ''), 'NA'),
    shfam1 = COALESCE(NULLIF(shfam1, ''), 'NA'),
    shfam2 = COALESCE(NULLIF(shfam2, ''), 'NA'),
    shfam3 = COALESCE(NULLIF(shfam3, ''), 'NA'),
    shfam4 = COALESCE(NULLIF(shfam4, ''), 'NA'),
    shfam5 = COALESCE(NULLIF(shfam5, ''), 'NA'),
    shfam6 = COALESCE(NULLIF(shfam6, ''), 'NA'),
    shfam7 = COALESCE(NULLIF(shfam7, ''), 'NA'),
    shfam8 = COALESCE(NULLIF(shfam8, ''), 'NA'),
    shfam9 = COALESCE(NULLIF(shfam9, ''), 'NA'),
    shfam10 = COALESCE(NULLIF(shfam10, ''), 'NA'),
    shfam11 = COALESCE(NULLIF(shfam11, ''), 'NA'),
    shfam12 = COALESCE(NULLIF(shfam12, ''), 'NA'),
    shfam13 = COALESCE(NULLIF(shfam13, ''), 'NA'),
    shfam14 = COALESCE(NULLIF(shfam14, ''), 'NA'),
    shfam18 = COALESCE(NULLIF(shfam18, ''), 'NA'),
    hhsize = COALESCE(NULLIF(hhsize, ''), 'NA'),
    caredu = COALESCE(NULLIF(caredu, ''), 'NA'),
    hschool = COALESCE(NULLIF(hschool, ''), 'NA'),
    chalcohol = COALESCE(NULLIF(chalcohol, ''), 'NA'),
    enrol = COALESCE(NULLIF(enrol, ''), 'NA'),
    engrade = COALESCE(NULLIF(engrade, ''), 'NA'),
    levlread = COALESCE(NULLIF(levlread, ''), 'NA'),
    momid = COALESCE(NULLIF(momid, ''), 'NA'),
    momedu = COALESCE(NULLIF(momedu, ''), 'NA'),
	dadedu= COALESCE(NULLIF(dadedu, ''), 'NA'),
	chsmoke=COALESCE(NULLIF(chsmoke, ''), 'NA'),
	chhealth=COALESCE(NULLIF(chhealth, ''), 'NA'),
	typesite=COALESCE(NULLIF(typesite, ''), 'NA')

WHERE
    country IS NULL OR country = '' OR
    childid IS NULL OR childid = '' OR
    chsex IS NULL OR chsex = '' OR
	bwght IS NULL OR bwght = '' OR
    agemon IS NULL OR agemon = '' OR
    chweight IS NULL OR chweight = '' OR
    chheight IS NULL OR chheight = '' OR
    bmi IS NULL OR bmi = '' OR
    zwfa IS NULL OR zwfa = '' OR
    zhfa IS NULL OR zhfa = '' OR
    foodsec IS NULL OR foodsec = '' OR
    region IS NULL OR region = '' OR
    commid IS NULL OR commid = '' OR
    clustid IS NULL OR clustid = '' OR
    chillness IS NULL OR chillness = '' OR
    chinjury IS NULL OR chinjury = '' OR
    yc IS NULL OR yc = '' OR
    deceased IS NULL OR deceased = '' OR
    shfam1 IS NULL OR shfam1 = '' OR
    shfam2 IS NULL OR shfam2 = '' OR
    shfam3 IS NULL OR shfam3 = '' OR
    shfam4 IS NULL OR shfam4 = '' OR
    shfam5 IS NULL OR shfam5 = '' OR
    shfam6 IS NULL OR shfam6 = '' OR
    shfam7 IS NULL OR shfam7 = '' OR
    shfam8 IS NULL OR shfam8 = '' OR
    shfam9 IS NULL OR shfam9 = '' OR
    shfam10 IS NULL OR shfam10 = '' OR
    shfam11 IS NULL OR shfam11 = '' OR
    shfam12 IS NULL OR shfam12 = '' OR
    shfam13 IS NULL OR shfam13 = '' OR
    shfam14 IS NULL OR shfam14 = '' OR
    shfam18 IS NULL OR shfam18 = '' OR
    hhsize IS NULL OR hhsize = '' OR
    caredu IS NULL OR caredu = '' OR
    hschool IS NULL OR hschool = '' OR
    chalcohol IS NULL OR chalcohol = '' OR
    enrol IS NULL OR enrol = '' OR
    engrade IS NULL OR engrade = '' OR
    levlread IS NULL OR levlread = '' OR
    momid IS NULL OR momid = '' OR
    momedu IS NULL OR momedu = '' OR
    momedu IS NULL OR momedu = '' OR
	dadedu IS NULL OR dadedu = '' OR
	chsmoke IS NULL OR chsmoke = '' OR
	chhealth IS NULL OR chhealth  = '' OR
	typesite IS NULL OR typesite = '' 

--- Clean dataset for Ethiopia
UPDATE [dbo].[ethiopia_constructed]
SET
    country = COALESCE(NULLIF(country, ''), 'NA'),
    childid = COALESCE(NULLIF(childid, ''), 'NA'),
    chsex = COALESCE(NULLIF(chsex, ''), 'NA'),
	bwght = COALESCE(NULLIF(bwght, ''), 'NA'),
    agemon = COALESCE(NULLIF(agemon, ''), 'NA'),
    chweight = COALESCE(NULLIF(chweight, ''), 'NA'),
    chheight = COALESCE(NULLIF(chheight, ''), 'NA'),
    bmi = COALESCE(NULLIF(bmi, ''), 'NA'),
    zwfa = COALESCE(NULLIF(zwfa, ''), 'NA'),
    zhfa = COALESCE(NULLIF(zhfa, ''), 'NA'),
    foodsec = COALESCE(NULLIF(foodsec, ''), 'NA'),
    region = COALESCE(NULLIF(region, ''), 'NA'),
    commid = COALESCE(NULLIF(commid, ''), 'NA'),
    clustid = COALESCE(NULLIF(clustid, ''), 'NA'),
    chillness = COALESCE(NULLIF(chillness, ''), 'NA'),
    chinjury = COALESCE(NULLIF(chinjury, ''), 'NA'),
    yc = COALESCE(NULLIF(yc, ''), 'NA'),
    deceased = COALESCE(NULLIF(deceased, ''), 'NA'),
    shfam1 = COALESCE(NULLIF(shfam1, ''), 'NA'),
    shfam2 = COALESCE(NULLIF(shfam2, ''), 'NA'),
    shfam3 = COALESCE(NULLIF(shfam3, ''), 'NA'),
    shfam4 = COALESCE(NULLIF(shfam4, ''), 'NA'),
    shfam5 = COALESCE(NULLIF(shfam5, ''), 'NA'),
    shfam6 = COALESCE(NULLIF(shfam6, ''), 'NA'),
    shfam7 = COALESCE(NULLIF(shfam7, ''), 'NA'),
    shfam8 = COALESCE(NULLIF(shfam8, ''), 'NA'),
    shfam9 = COALESCE(NULLIF(shfam9, ''), 'NA'),
    shfam10 = COALESCE(NULLIF(shfam10, ''), 'NA'),
    shfam11 = COALESCE(NULLIF(shfam11, ''), 'NA'),
    shfam12 = COALESCE(NULLIF(shfam12, ''), 'NA'),
    shfam13 = COALESCE(NULLIF(shfam13, ''), 'NA'),
    shfam14 = COALESCE(NULLIF(shfam14, ''), 'NA'),
    shfam18 = COALESCE(NULLIF(shfam18, ''), 'NA'),
    hhsize = COALESCE(NULLIF(hhsize, ''), 'NA'),
    caredu = COALESCE(NULLIF(caredu, ''), 'NA'),
    hschool = COALESCE(NULLIF(hschool, ''), 'NA'),
    chalcohol = COALESCE(NULLIF(chalcohol, ''), 'NA'),
    enrol = COALESCE(NULLIF(enrol, ''), 'NA'),
    engrade = COALESCE(NULLIF(engrade, ''), 'NA'),
    levlread = COALESCE(NULLIF(levlread, ''), 'NA'),
    momid = COALESCE(NULLIF(momid, ''), 'NA'),
    momedu = COALESCE(NULLIF(momedu, ''), 'NA'),
	dadedu= COALESCE(NULLIF(dadedu, ''), 'NA'),
	chsmoke=COALESCE(NULLIF(chsmoke, ''), 'NA'),
	chhealth=COALESCE(NULLIF(chhealth, ''), 'NA'),
	typesite=COALESCE(NULLIF(typesite, ''), 'NA')
WHERE
    country IS NULL OR country = '' OR
    childid IS NULL OR childid = '' OR
    chsex IS NULL OR chsex = '' OR
	bwght IS NULL OR bwght = '' OR
    agemon IS NULL OR agemon = '' OR
    chweight IS NULL OR chweight = '' OR
    chheight IS NULL OR chheight = '' OR
    bmi IS NULL OR bmi = '' OR
    zwfa IS NULL OR zwfa = '' OR
    zhfa IS NULL OR zhfa = '' OR
    foodsec IS NULL OR foodsec = '' OR
    region IS NULL OR region = '' OR
    commid IS NULL OR commid = '' OR
    clustid IS NULL OR clustid = '' OR
    chillness IS NULL OR chillness = '' OR
    chinjury IS NULL OR chinjury = '' OR
    yc IS NULL OR yc = '' OR
    deceased IS NULL OR deceased = '' OR
    shfam1 IS NULL OR shfam1 = '' OR
    shfam2 IS NULL OR shfam2 = '' OR
    shfam3 IS NULL OR shfam3 = '' OR
    shfam4 IS NULL OR shfam4 = '' OR
    shfam5 IS NULL OR shfam5 = '' OR
    shfam6 IS NULL OR shfam6 = '' OR
    shfam7 IS NULL OR shfam7 = '' OR
    shfam8 IS NULL OR shfam8 = '' OR
    shfam9 IS NULL OR shfam9 = '' OR
    shfam10 IS NULL OR shfam10 = '' OR
    shfam11 IS NULL OR shfam11 = '' OR
    shfam12 IS NULL OR shfam12 = '' OR
    shfam13 IS NULL OR shfam13 = '' OR
    shfam14 IS NULL OR shfam14 = '' OR
    shfam18 IS NULL OR shfam18 = '' OR
    hhsize IS NULL OR hhsize = '' OR
    caredu IS NULL OR caredu = '' OR
    hschool IS NULL OR hschool = '' OR
    chalcohol IS NULL OR chalcohol = '' OR
    enrol IS NULL OR enrol = '' OR
    engrade IS NULL OR engrade = '' OR
    levlread IS NULL OR levlread = '' OR
    momid IS NULL OR momid = '' OR
    momedu IS NULL OR momedu = '' OR
    momedu IS NULL OR momedu = '' OR
	dadedu IS NULL OR dadedu = '' OR
	chsmoke IS NULL OR chsmoke = '' OR
	chhealth IS NULL OR chhealth = '' OR
	typesite IS NULL OR typesite = '' 

SELECT *
FROM [dbo].[vietnam_constructed]

SELECT *
FROM[dbo].[ethiopia_constructed]

--CREATE VIEWS
--View 01
CREATE VIEW BirthWeight_ChildHealth AS
SELECT[childid],[agemon],[chsex],[Country],[bwght],[bmi]
FROM[dbo].[vietnam_constructed]
WHERE [childid]<>' ' AND 
      [agemon]<>' ' AND
      [chsex] <>' ' AND
      [Country]<>' ' AND
      [bwght]<>' ' AND
      [bmi]<>' ' 

UNION ALL

SELECT [childid],[agemon],[chsex],[Country],[bwght],[bmi]
FROM[dbo].[ethiopia_constructed]
WHERE [childid]<>' ' AND 
      [agemon]<>' ' AND
      [chsex] <>' ' AND
      [Country]<>' ' AND
      [bwght]<>' ' AND
      [bmi]<>' ' 

SELECT *
FROM[dbo].[BirthWeight_ChildHealth]

--View 02

CREATE VIEW  edu_parents_impact AS
SELECT [childid],[agemon],[chsex],[Country],[enrol],[engrade],[levlread],[levlwrit],[momedu],[dadedu]
FROM[dbo].[vietnam_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[enrol]<>' ' AND
[engrade]<>' ' AND
[levlread]<>' ' AND
[levlwrit]<>' ' AND
[momedu]<>' ' AND
[dadedu]<>' ' 

UNION ALL

SELECT [childid],[agemon],[chsex],[Country],[enrol],[engrade],[levlread],[levlwrit],[momedu],[dadedu]
FROM[dbo].[ethiopia_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[enrol]<>' ' AND
[engrade]<>' ' AND
[levlread]<>' ' AND
[levlwrit]<>' ' AND
[momedu]<>' ' AND
[dadedu]<>' ' 

SELECT *
FROM[dbo].[edu_parents_impact]


--view 3

CREATE VIEW foodsecure_vs_childgrowth AS

SELECT [childid],[agemon],[chsex],[Country],[foodsec],[chweight],[chheight],[bmi]
FROM[dbo].[vietnam_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[foodsec]<>' ' AND
[chweight]<>' ' AND
[chheight]<>' ' AND
[bmi]<>' ' 

UNION ALL

SELECT [childid],[agemon],[chsex],[Country],[foodsec],[chweight],[chheight],[bmi]
FROM[dbo].[ethiopia_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[foodsec]<>' ' AND
[chweight]<>' ' AND
[chheight]<>' ' AND
[bmi]<>' ' 

SELECT *
FROM[dbo].[foodsecure_vs_childgrowth]

--view4
CREATE VIEW ChildIllness_HouseholdEconomicStrain AS
SELECT [childid],[agemon],[chsex],[Country],[chillness],[hhsize],[foodsec],[shfam7]
FROM[dbo].[vietnam_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[chillness]<>' ' AND
[hhsize]<>' ' AND
[foodsec]<>' ' AND
[shfam7]<>' ' 

UNION ALL

SELECT [childid],[agemon],[chsex],[Country],[chillness],[hhsize],[foodsec],[shfam7]
FROM[dbo].[ethiopia_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[chillness]<>' ' AND
[hhsize]<>' ' AND
[foodsec]<>' ' AND
[shfam7]<>' ' 
 

SELECT *
FROM[dbo].[ChildIllness_HouseholdEconomicStrain]

--view5

CREATE VIEW ChildBehavior_outcomes AS
SELECT [childid],[agemon],[chsex],[Country],[chalcohol],[chsmoke],[chhealth],[enrol][chinjury]
FROM[dbo].[vietnam_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[chalcohol]<>' ' AND
[chsmoke]<>' ' AND
[chhealth]<>' ' AND
[enrol]<>' ' AND
[chinjury]<>' ' 

UNION ALL

SELECT [childid],[agemon],[chsex],[Country],[chalcohol],[chsmoke],[chhealth],[enrol][chinjury]
FROM[dbo].[ethiopia_constructed]
WHERE [childid]<>' ' AND 
[agemon]<>' ' AND
[chsex] <>' ' AND
[Country]<>' ' AND
[chalcohol]<>' ' AND
[chsmoke]<>' ' AND
[chhealth]<>' ' AND
[enrol]<>' ' AND
[chinjury]<>' ' 


SELECT *
FROM[dbo].[ChildBehavior_outcomes]

--view6

CREATE VIEW HouseholdSize_Urban_Rural AS
SELECT [childid],[Country],[region],[typesite],[hhsize]
FROM[dbo].[vietnam_constructed]
WHERE [childid]<>' ' AND 
[Country]<>' ' AND
[Country]<>' ' AND
[region]<>' ' AND
[typesite]<>' ' AND
[hhsize]<>' '


UNION ALL

SELECT [childid],[Country],[region],[typesite],[hhsize]
FROM[dbo].[ethiopia_constructed]
WHERE [childid]<>' ' AND 
[Country]<>' ' AND
[region]<>' ' AND
[typesite]<>' ' AND
[hhsize]<>' '


SELECT *
FROM[dbo].[HouseholdSize_Urban_Rural]






