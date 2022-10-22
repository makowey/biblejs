This is a free webcomponent API. Now you can have direct access to different versions of Bibles in different languages.

_This document is still in progress._

## Code Example

Adding the simple tag in your HTML page you should see the default verse, Genesis 1:1.
	
	Script header: 	<script src="https://biblionar.ro/biblejs/cdn/bible.min.js"></script>
	
	HTML: 			<bible-js></bible-js>
	Render:			In the beginning God created the heaven and the earth.

## Motivation

:book: This project is made to facilitate access to the precious word of God. Using this library you have freedom to use much as possible. 
Keep IT simple is the motto.

## Installation
Add the following script into `<head>` tag of your HTML page.

`<script src="https://biblionar.ro/biblejs/cdn/bible.min.js"></script>`

## API Reference

There are some attributes that can be simple adjusted to perform the desired request
	
	<bible-js lang=he></bible-js>
	<bible-js book=Gen></bible-js>
	<bible-js book=Gen chapter=1></bible-js>
	<bible-js book=Gen chapter=1 verse=1></bible-js>
	<bible-js book=Gen chapter=1 verse=1 lang=es></bible-js>
	<bible-js book=Gen chapter=1 verse=1 lang=he version=alep></bible-js>
	<bible-js book=Gen chapter=1 verse=1 version=aleppo curl></bible-js>
	<bible-js book=Gen chapter=1 verse=1 version=aleppo curl icon></bible-js>

Attribute  	  | Type         									| Values								| Default 		|	Description
------------- | -------------------------------- 				| -------------							| -------------	| -------------
lang 		  | [text{2}]      									|  en, fr, es, it, ro, he, gr ...		|	[en]		|	language
book  		  | [text/number] 									|  Gen, Rev, Ex or 1, 66, 2		 		|	[Gen]		|	book of books
chapter  	  | [number]   			    						|  1, 2, 3, ...							|	[1]			|	chapter
verse	  	  | [number]   			    						|  1, 2, 3, ...							|	[1]			|	verse number
version	  	  | [text]   			    						|  kjv, bhs, asv, cornilescu ...		|	[kjv]		|	version of bible, this parameter is related to lang value.
icon	  	  | [text]   			    						|  empty								|	[book]		|	icon fa-book for the verse
curl	  	  | [text]   			    						|  empty								|	[kjv]		|	different source through curl

## Languages & Versions default API

Bellow you have the list of all versions in default, no **curl** attribute.

	Request: <bible-js lang=he book=1 chapter=1 verse=1 version=bhs></bible-js>
	Response:  בְּרֵאשִׁית בָּרָא אֱלֹהִים אֵת הַשָּׁמַיִם וְאֵת הָאָרֶץ ׃

language  	  	| lang        						|	version				| content 				
------------- 	| -------------------------------- 	| -------------			| -------------
African			| af 								| afr3353		 		| 1933/1953 Afrikaans Bybel
Arabian			| ar 								| arasvd		 		| Smith Van Dyke Arabic Bible
Bulgarian		| bg 								| bulcarigradnt 		| Tsarigrad Edition
Bulgarian		| bg 								| bulveren 				| Veren's Contemporary Bible
Chamorro		| ch 								| chamorro 				| Y Santa Biblia (1908)
Danish			| da 								| dan 	 				| Danish Version
English			| en 								| kjv 	 				| King James Version
German			| de 								| elb1871nt				| Elberfelder 1871 NT Original
German			| de 								| gerneue				| Neue Evangelistische Übersetzung
German			| de 								| albrecht1926			| Albrecht Bibel 1926
German			| de 								| fb2004				| FreeBible2004
Espaniol		| es 								| sev 	 				| Las Sagradas Escrituras
Esperando		| eu 								| basq1571 				| Basque(Navarro-Labourdin)NT
Hebrew 			| he 								| alep 		 			| Aleppo Codex
Hebrew 			| he 								| bhs 	 				| Biblia Hebraica
Romanian		| ro 								| cornilescu 			| Biblia 1923
		
## Languages & Versions in cURL mode 

Bellow you have the list of all versions in cURL mode.
List of available languages and versions, values for [lang] & [version] arguments:
	
If cURL is ON no need to specify the [lang] argument, only the version is required.

	Request: 	<bible-js book=1 chapter=2 verse=3 version=albanian curl></bible-js>
	Response: 	Dhe Perëndia bekoi ditën e shtatë dhe e shenjtëroi, sepse atë ditë Perëndia u çlodh nga gjithë vepra që kishte krijuar dhe kryer.
	
language  	  	| lang        						|	version				| content 				
------------- 	| -------------------------------- 	| -------------			| -------------
Albanian 		| sq 								| albanian 				| Bible
Amharic 		| am 								| amharic 				| NT
Arabic	 		| ar 								| smith-vandyke			| Smith & Van Dyke
Aramaic	 		| ar 								| peshitta				| NT Peshitta
Armenian 		| hy 								| easternarmenian		| (Eastern): (Genesis, Exodus, Gospels)
Armenian 		| hy 								| westernarmenian		| (Western): NT
Basque 	 		| eu 								| basque 				| Navarro-Labourdin
Breton 	 		| br 								| breton 				| Gospels
Chamorro 	 	| ch 								| chamorro 				| Psalms, Gospels, Acts
Chinese 	 	| zh 								| chinese-ncv-simplifi	| NCV (Simplified)
Chinese 	 	| zh 								| chinese-ncv-traditio	| NCV (Traditional)
Chinese 	 	| zh 								| union-simplified		| Union (Simplified)
Chinese 	 	| zh 								| union-traditional		| Union (Traditional)
Coptic 	 	 	| - 								| bohairic 				| Bohairic NT
Coptic 	 	 	| - 								| coptic 				| New Testament
Coptic 	 	 	| - 								| sahidic 				| Sahidic NT
Croatian 	 	| hr 								| croatia 				| Bible
Czech 	 		| cs 								| bkr 					| BKR
Czech 	 		| cs 								| kms 					| KMS
Czech 	 		| cs 								| nkb 					| NKB
Danish 	 		| da 								| danish 				| Bible
Dutch 	 		| nl 								| statenvertaling		| Staten Vertaling
English 	 	| en 								| akjv					| American King James Version 
English 	 	| en 								| asv					| American Standard Version 
English 	 	| en 								| amplified				| Amplified Version 
English 	 	| en 								| douayrheims			| Douay-Rheims 
English 	 	| en 								| kjv 					| King James Version 
English 	 	| en 								| nasb 					| New American Standard 
English 	 	| en 								| web 					| World English Bible 
English 	 	| en 								| ylt 					| Young’s Literal Translation 
Esperanto 	 	| eo 								| esperanto				| Bible 
Estonian 	 	| et 								| estonian				| Bible 
Finnish 	 	| fi 								| finnish1776			| Bible (1776) 
Finnish 	 	| fi 								| pyharaamattu1933		| Pyhä Raamattu (1933/1938)
French	 	 	| fr 								| darby 				| Darby
French	 	 	| fr 								| ls1910 				| Louis Segond (1910)
French	 	 	| fr 								| martin 				| Martin (1744)
French	 	 	| fr 								| ostervald				| Ostervald (1996 revision)
Georgian	 	| ka 								| georgian				| Gospels, Acts, James
German		 	| de 								| elberfelder			| Elberfelder (1871)
German		 	| de 								| elberfelder1905		| Elberfelder (1905)
German		 	| de 								| luther1545			| Luther (1545)
German		 	| de 								| luther1912			| Luther (1912)
German		 	| de 								| schlachter			| Schlachter (1951)
Gothic		 	| go 								| gothic 				| Nehemiah, NT Portions
Greek		 	| gr 								| byzantine				| NT: Byzantine/Majority Text (2000)
Greek		 	| gr 								| textusreceptus		| NT: Textus Receptus (1550/1894)
Greek		 	| gr 								| tischendorf 			| NT: Tischendorf 8th Ed.
Greek		 	| gr 								| wstcott	 			| NT: Westcott/Hort, UBS4 variants
Greek		 	| gr 								| lxx 		 			| OT: LXX [A] Accented
Greek		 	| gr 								| lxx-noaccents			| OT: LXX [A] Unaccented
Greek		 	| gr 								| moderngreek			| Modern
Hebrew		 	| he 								| aleppo				| OT: Aleppo Codex
Hebrew		 	| he 								| bhs 					| OT: BHS (Consonants & Vowels)
Hebrew		 	| he 								| bhs-novowels			| BHS (Consonants Only)
Hebrew		 	| he 								| wlc 					| OT: Westminster Leningrad Codex
Hebrew		 	| he 								| wlc2 					| OT: WLC (Consonants & Vowels)
Hebrew		 	| he 								| wlc-novowels			| OT: WLC (Consonants Only)
Hebrew		 	| he 								| modernhebrew			| Modern
Italian		 	| it 								| giovanni 				| Giovanni Diodati Bible (1649)
Italian		 	| it 								| riveduta 				| Riveduta Bible (1927)
Kabyle		 	| - 								| kabyle 				| NT
Korean		 	| ko 								| korean 				| Bible
Latin		 	| la 								| newvulgate			| Nova Vulgata
Latin		 	| la 								| vulgate				| Vulgata Clementina
Latvian		 	| lv 								| latvian				| New Testament
Lithuanian		| lt 								| lithuanian			| Bible
Manx Gaelic		| gv 								| manxgaelic			| Bible
Myanmar/Burmese	| - 								| judson 				| Judson (1835)
Norwegian		| no 								| bibelselskap			| Det Norsk Bibelselskap (1930)
Portuguese		| pt 								| almeida 				| Almeida Atualizada
Romanian		| ro 								| cornilescu			| Cornilescu
Russian 		| ru								| makarij 				| Makarij Translation (Pentateuch) (1825)
Russian 		| ru								| synodal 				| Synodal Translation (1876)
Russian 		| ru								| zhuromsky				| Victor Zhuromsky NT
Scots Gaelic	| sn								| scotsgaelic			| Gospel of Mark
Spanish 		| sp								| rv1909 				| Reina Valera (1909)
Spanish 		| sp								| rv1858 				| Reina Valera NT (1858)
Spanish 		| sp								| sagradas 				| Sagradas Escrituras (1569)
Swedish 		| sv								| swedish 				| 1917
Tagalog 		| tl								| tagalog 				| Ang Dating Biblia (1905)
Tamajaq 		| - 								| tamajaq 				| Portions
Thai 	 		| th 								| thai  				| from KJV
Ukrainian 		| uk 								| ukranian 				| NT (P.Kulish, 1871)
Uma 	 		| - 								| uma 	 				| NT
Vietnamese 		| vi 								| vietnamese			| 1934
Wolof 	 		| - 								| wolof					| Bible
Xhosa 	 		| - 								| xhosa					| Bible

## Author

:book: @Claudiu Macovei - 2016.04.02
