# Sawt-El-Djazair
Sawt-El-Djazair Sawt El-Djazaïr is an Algerian Colloquial Speech corpus, collected from both Web-based speech dataset and speaker’s phone recording.

Sawt-El-Djazair is composed of two parts; Web based corpus and Volunteers corpus. In web based corpus, the data was collected from different web resource, specifically YouTube and Facebook.

The second part of the corpus called Volunteers corpus is collected from telephone conversations using cellular calls and VoIP applications such as Viber, WhatsApp and Google Meet.

# Provided data:

1/ Sawt El-Djazair is collected from major Algerian Arabic and Tamazight sub-dialects:

•	Tamazight, including Kabyle, Chaouia, Chenoua and Mzab. 

•	Arabic, including Pre-hilali, Hilali-Saharan, Hilali-Tellian, Hilali-plains, Ma 'qilian, Sulaymite, Algiers Blanks, and Sahel-Tell. 

2/ The form contains all demographic information of speaker such as age, gender, dialect and languages spoken…etc. The form was launched on social networks in order to have a large number of speakers to cover as much Algerian sub-dialect varieties as possible.
Link of the Form:
https://docs.google.com/forms/d/e/1FAIpQLSfjQLO6jlR5EVWXYib6pTOb-8ueMN3gvbdnpQV78dSBsoTa1Q/viewform?fbclid=IwAR2B-kvltzmotk5AmHRXcoerAnPVTO426gchqfUwY21AJbQQ77iwKS0hLMM

3/ A detailed technical sheet of Salah Ougrout.

4/ Java script for Web based corpus harvest.
 
 function myFunction() {
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  var ActiveSheet = ss.getActiveSheet();
  
  var modRes = sr.items.map(function(vid){ return [ vid.snippet.resourceId.videoId , vid.snippet.title, vid.contentDetails.videoPublishedAt]; });
  //Logger.log (modRes);
  
  var ids = modRes.map ( function(res){ return res[0]; }).join(",");
  //Logger.log (ids);
  var stats = YouTube.Videos.list("snippet,contentDetails,status",{id:ids});
 
  var statss = stats.items.map(function(vidd){ return [ vidd.id ,vidd.snippet.channelTitle,vidd.contentDetails.duration, vidd.snippet.defaultAudioLanguage, vidd.contentDetails.definition,
  vidd.snippet.categoryId, vidd.fileDetails]; });
 

5/ A sample volunteer call recording is available 
