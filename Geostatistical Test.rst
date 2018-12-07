
.. code:: ipython3

    import requests
    import json
    
    overpass_url = "http://overpass-api.de/api/interpreter"
    overpass_query = """
    [out:json];
    area["ISO3166-1"="DE"][admin_level=2];
    (node["amenity"="biergarten"](area);
     way["amenity"="biergarten"](area);
     rel["amenity"="biergarten"](area);
    );
    out center;
    """
    response = requests.get(overpass_url, 
                            params={'data': overpass_query})
    data = response.json()
    data




.. parsed-literal::

    {'version': 0.6,
     'generator': 'Overpass API 0.7.55.5 2ca3f387',
     'osm3s': {'timestamp_osm_base': '2018-12-06T16:57:02Z',
      'timestamp_areas_base': '2018-12-06T15:57:03Z',
      'copyright': 'The data included in this document is from www.openstreetmap.org. The data is made available under ODbL.'},
     'elements': [{'type': 'node',
       'id': 23662384,
       'lat': 50.5112014,
       'lon': 6.9939896,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 25338407,
       'lat': 49.9534891,
       'lon': 10.8750469,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 26584878,
       'lat': 48.4582678,
       'lon': 11.8325645,
       'tags': {'amenity': 'biergarten',
        'created_by': 'JOSM',
        'name': 'Schlossallee',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 26865440,
       'lat': 52.4333644,
       'lon': 13.190734,
       'tags': {'amenity': 'biergarten',
        'name': 'Spinnerbrücke',
        'note': 'Motorradtreff',
        'toilets:wheelchair': 'no',
        'website': 'http://www.spinner-bruecke.de/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 26870913,
       'lat': 50.0110113,
       'lon': 8.3917604,
       'tags': {'addr:city': 'Flörsheim',
        'addr:postcode': '65439',
        'amenity': 'biergarten',
        'email': 'Info@gasthofwiesenmuehle.de',
        'fax': '+49 6145 2641',
        'name': 'Gasthof Wiesenmühle',
        'opening_hours': 'We-Su 11:00-23:00; Mo,Tu off',
        'operator': 'Familie Idstein, Laudes und Olbert',
        'phone': '+49 6145 7166; +49 6145 1083',
        'source': 'http://www.gasthof-wiesenmuehle.de/',
        'website': 'http://www.gasthof-wiesenmuehle.de/',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 27159163,
       'lat': 48.9693881,
       'lon': 8.3903784,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 27318009,
       'lat': 52.420095,
       'lon': 13.176351,
       'tags': {'addr:city': 'Berlin',
        'addr:housenumber': '260',
        'addr:postcode': '14109',
        'addr:street': 'Kronprinzessinnenweg',
        'amenity': 'biergarten',
        'name': 'Loretta',
        'phone': '+49 30 80105333',
        'website': 'http://www.loretta-berlin.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 27352197,
       'lat': 50.3638373,
       'lon': 7.5769021,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 27787909,
       'lat': 52.9822191,
       'lon': 8.845254,
       'tags': {'amenity': 'biergarten',
        'name': 'Schwarzbiergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 29812167,
       'lat': 49.4814353,
       'lon': 10.993033,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 29821140,
       'lat': 48.3974836,
       'lon': 11.7378821,
       'tags': {'amenity': 'biergarten',
        'name': 'Lindenkeller',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 32628620,
       'lat': 47.9927509,
       'lon': 7.8558873,
       'tags': {'addr:city': 'Freiburg im Breisgau',
        'addr:housenumber': '3',
        'addr:postcode': '79098',
        'addr:street': 'Schlossbergring',
        'amenity': 'biergarten',
        'contact:email': 'info@kastaniengarten-freiburg.de',
        'contact:fax': '+49 761 289602',
        'contact:phone': '+49 761 32728',
        'contact:website': 'http://www.kastaniengarten-freiburg.de/',
        'name': 'Kastaniengarten',
        'opening_hours': 'Mo-Su 11:00-24:00',
        'phone': '+49 761 32728',
        'toilets:wheelchair': 'no',
        'website': 'http://www.greiffenegg.de/kastaniengarten.html',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 33128217,
       'lat': 49.9322248,
       'lon': 11.5720575,
       'tags': {'amenity': 'biergarten',
        'name': 'Röhrensee',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 34483100,
       'lat': 48.0124776,
       'lon': 7.8149142,
       'tags': {'addr:street': 'Gerhart-Hauptmann-Straße',
        'amenity': 'biergarten',
        'contact:phone': '+49 761 4565526',
        'contact:website': 'http://www.biergartenseepark-freiburg.de/',
        'name': 'Biergarten am Seepark',
        'opening_hours': 'Mo-Sa 11:30-00:00; Su 11:00-00:00',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 34821030,
       'lat': 47.9207025,
       'lon': 11.7554223,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Graf Arco',
        'cuisine': 'regional',
        'name': 'Zum Bartewirt',
        'note': 'http://www.merkur.de/lokales/region-holzkirchen/valley/kreuzstrasse-bartewirt-sucht-einen-neuen-paechter-5135548.html',
        'opening_hours': 'closed',
        'operator': 'vacant',
        'wheelchair': 'yes',
        'wheelchair:description:de': 'Behindertentoilette vorhanden'}},
      {'type': 'node',
       'id': 54020544,
       'lat': 50.9313358,
       'lon': 6.9369729,
       'tags': {'addr:city': 'Köln',
        'addr:housenumber': '30',
        'addr:postcode': '50674',
        'addr:street': 'Rathenauplatz',
        'amenity': 'biergarten',
        'cuisine': 'german',
        'name': 'www.rathenauplatz.de',
        'outdoor_seating': 'yes',
        'website': 'http://www.rathenauplatz.de',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 54050453,
       'lat': 51.0910202,
       'lon': 6.8805055,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 59229391,
       'lat': 49.6057522,
       'lon': 10.8848653,
       'tags': {'addr:city': 'Heßdorf',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:place': 'Obermembach',
        'addr:postcode': '91093',
        'addr:street': 'Obermembach',
        'amenity': 'biergarten',
        'brewery': 'tucher',
        'name': 'Gasthaus Gumbrecht',
        'opening_hours': 'We-Mo 10:00-22:00',
        'outdoor_seating': 'yes',
        'phone': '09135 3140',
        'smoking': 'outside',
        'website': 'http://www.gasthaus-gumbrecht.de/Home'}},
      {'type': 'node',
       'id': 59316621,
       'lat': 48.9988621,
       'lon': 8.0705867,
       'tags': {'amenity': 'biergarten',
        'email': 'info@bienwaldmuehle.de',
        'name': 'Bienwaldmühle',
        'opening_hours': 'We-Su 11:00-22:00',
        'operator': 'Philipp Roth',
        'phone': '+49-6340-276',
        'website': 'http://www.bienwaldmuehle.de/'}},
      {'type': 'node',
       'id': 60586274,
       'lat': 49.4612223,
       'lon': 12.4195553,
       'tags': {'amenity': 'biergarten',
        'name': 'Deyerl',
        'opening_hours': 'off',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 69119734,
       'lat': 49.0014062,
       'lon': 8.397165,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Krušovice',
        'name': 'Alter Brauhof',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 89240328,
       'lat': 49.0722096,
       'lon': 8.1927674,
       'tags': {'amenity': 'biergarten',
        'name': 'Fun Forest',
        'tourism': 'theme_park',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 92666829,
       'lat': 48.1044802,
       'lon': 11.5347169,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '6',
        'addr:postcode': '81379',
        'addr:street': 'Zielstattstraße',
        'amenity': 'biergarten',
        'brewery': 'Augustiner',
        'capacity': '2500',
        'contact:email': 'info@augustiner-schützengarten.de',
        'contact:fax': '+49 89 724 680 89',
        'contact:phone': '+49 89 724 680 88',
        'contact:website': 'http://www.augustiner-schuetzengarten.de',
        'cuisine': 'bavarian',
        'name': 'Augustiner Schützengarten',
        'opening_hours': 'Mo-Su 11:00-23:00',
        'operator': 'Christian Schretzlmeier',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 99382490,
       'lat': 48.1832729,
       'lon': 11.2739914,
       'tags': {'amenity': 'biergarten', 'name': 'Gräz'}},
      {'type': 'node',
       'id': 106494678,
       'lat': 49.0517594,
       'lon': 12.0450613,
       'tags': {'addr:city': 'Lappersdorf',
        'addr:country': 'DE',
        'addr:housenumber': '3',
        'addr:postcode': '93138',
        'addr:street': 'Karether Weg',
        'amenity': 'biergarten',
        'name': 'Huf',
        'phone': '+49 9404 1410'}},
      {'type': 'node',
       'id': 107316782,
       'lat': 48.8003651,
       'lon': 9.315582,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten'}},
      {'type': 'node',
       'id': 107871683,
       'lat': 50.0612104,
       'lon': 10.8635908,
       'tags': {'amenity': 'biergarten',
        'name': 'Sonnenbräu',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 118252923,
       'lat': 48.149801,
       'lon': 11.5855374,
       'tags': {'addr:city': 'München',
        'addr:housenumber': '6',
        'addr:postcode': '80539',
        'addr:street': 'Königinstraße',
        'amenity': 'biergarten',
        'contact:email': 'info@milchhaeusl.de',
        'contact:fax': '+49 89 517297199',
        'contact:phone': '+49 89 517297180',
        'name': 'Milchhäusl',
        'note': 'open in winter',
        'opening_hours': 'Mo-Su 10:00-22:00',
        'organic': 'only',
        'source': 'survey by BenE München',
        'toilets:wheelchair': 'no',
        'website': 'http://www.milchhaeusl.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 162723561,
       'lat': 48.1631633,
       'lon': 11.5323979,
       'tags': {'amenity': 'biergarten',
        'name': 'Taxisgarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 165143743,
       'lat': 50.114989,
       'lon': 11.0551054,
       'tags': {'amenity': 'biergarten',
        'name': 'Brauerei Trunk Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 167013475,
       'lat': 52.4916944,
       'lon': 13.4389954,
       'tags': {'addr:city': 'Berlin',
        'addr:country': 'DE',
        'addr:housenumber': '14c',
        'addr:postcode': '10999',
        'addr:street': 'Ratiborstraße',
        'addr:suburb': 'Kreuzberg',
        'amenity': 'biergarten',
        'internet_access': 'wlan',
        'name': 'Jockel',
        'opening_hours': 'Mo-Su 10:00-22:00',
        'phone': '+49 30 69598060',
        'website': 'http://www.biergarten-jockel.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 181437706,
       'lat': 48.0812535,
       'lon': 8.1596569,
       'tags': {'addr:city': 'Furtwangen im Schwarzwald',
        'addr:country': 'DE',
        'addr:housenumber': '5',
        'addr:postcode': '78120',
        'addr:street': 'Auf dem Brend',
        'amenity': 'biergarten',
        'capacity': '48',
        'name': 'Natufreundehaus Brend',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'L 038',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'hostel',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 182872843,
       'lat': 48.1827857,
       'lon': 11.2525293,
       'tags': {'addr:city': 'Fürstenfeldbruck',
        'addr:country': 'DE',
        'addr:housenumber': '41',
        'addr:postcode': '82256',
        'addr:street': 'Augsburger Straße',
        'amenity': 'biergarten',
        'website': 'http://www.brauhaus-bruck.de'}},
      {'type': 'node',
       'id': 196197259,
       'lat': 50.8805997,
       'lon': 11.6000326,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Saaleterrasse'}},
      {'type': 'node',
       'id': 196216198,
       'lat': 48.1329449,
       'lon': 11.5890485,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '81667',
        'addr:street': 'Zellstraße',
        'amenity': 'biergarten',
        'brewery': 'Hofbräu München',
        'capacity': '300',
        'contact:phone': '+49 89 458 750 10',
        'contact:website': 'http://www.muffathalle.de/Gastronomie/Biergarten.html',
        'name': 'Biergarten an der Muffathalle',
        'note': 'Öko-Betrieb',
        'opening_hours': 'Mo-Th 17:00+; Fr-Su 12:00+',
        'organic': 'only',
        'source': 'survey by BenE München',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 203547647,
       'lat': 51.3629651,
       'lon': 12.3430979,
       'tags': {'amenity': 'biergarten', 'name': 'Neuer Weg'}},
      {'type': 'node',
       'id': 204491889,
       'lat': 48.341065,
       'lon': 9.9398521,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 221529884,
       'lat': 49.0426808,
       'lon': 12.0161756,
       'tags': {'amenity': 'biergarten',
        'name': 'Prössl-Bräu Adlersberg',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 221531459,
       'lat': 49.0176795,
       'lon': 12.0294204,
       'tags': {'addr:city': 'Pettendorf',
        'addr:housenumber': '20',
        'addr:postcode': '93186',
        'addr:street': 'Naabstraße',
        'addr:suburb': 'Mariaort',
        'amenity': 'biergarten',
        'contact:email': 'gasthof@gasthof-krieger.de',
        'contact:fax': '+49 941 892124',
        'contact:phone': '+49 941 84278',
        'contact:website': 'http://www.gasthof-krieger.de/',
        'name': 'Krieger',
        'source': 'http://www.gasthof-krieger.de/'}},
      {'type': 'node',
       'id': 227749643,
       'lat': 51.8608757,
       'lon': 10.8150651,
       'tags': {'addr:city': 'Wernigerode',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '38855',
        'addr:street': 'Rothe Mühle',
        'amenity': 'biergarten',
        'name': 'Rothe Mühle Bier- und Kaffeegarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 242546252,
       'lat': 51.3246689,
       'lon': 9.4449248,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 244011558,
       'lat': 50.5434406,
       'lon': 8.5335935,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 245011188,
       'lat': 48.6620761,
       'lon': 9.3178861,
       'tags': {'amenity': 'biergarten', 'name': 'Lindenhöfe'}},
      {'type': 'node',
       'id': 245938860,
       'lat': 48.7609994,
       'lon': 9.0916049,
       'tags': {'amenity': 'biergarten',
        'name': 'Bärenschlössle',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 246763435,
       'lat': 50.9684636,
       'lon': 6.9490882,
       'tags': {'amenity': 'biergarten', 'source': 'survey'}},
      {'type': 'node',
       'id': 246851272,
       'lat': 51.052279,
       'lon': 13.809103,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.7',
        'name': 'Schillergarten',
        'opening_hours': 'Mo-Su 11:00-01:00',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 248819042,
       'lat': 49.6696258,
       'lon': 10.9307287,
       'tags': {'amenity': 'biergarten',
        'heritage': '4',
        'heritage:operator': 'BLfD',
        'historic': 'yes',
        'name': "Sauer's Keller",
        'opening_hours': 'May-Sep: 11:00+',
        'ref:BLfD': 'D-5-72-149-10'}},
      {'type': 'node',
       'id': 249755600,
       'lat': 51.0567441,
       'lon': 6.8512195,
       'tags': {'amenity': 'biergarten',
        'name': 'Krebelshof',
        'source': 'survey'}},
      {'type': 'node',
       'id': 250535861,
       'lat': 51.3314765,
       'lon': 12.4111614,
       'tags': {'amenity': 'biergarten',
        'name': 'Reudnitz Terrassen',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 250813040,
       'lat': 49.5904803,
       'lon': 10.7610548,
       'tags': {'amenity': 'biergarten',
        'name': 'Felsenkeller Geyer',
        'operator': 'Brauereigasthof Geyer'}},
      {'type': 'node',
       'id': 250957178,
       'lat': 47.990399,
       'lon': 7.8586445,
       'tags': {'addr:housenumber': '4',
        'amenity': 'biergarten',
        'name': 'Ganter Biergarten'}},
      {'type': 'node',
       'id': 251662991,
       'lat': 47.8051395,
       'lon': 9.6418742,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 251827084,
       'lat': 48.2912447,
       'lon': 11.6243318,
       'tags': {'amenity': 'biergarten', 'name': 'SCE-Sportgaststätte'}},
      {'type': 'node',
       'id': 252112706,
       'lat': 49.81615,
       'lon': 10.9863455,
       'tags': {'amenity': 'biergarten', 'name': 'Brauerei Kraus'}},
      {'type': 'node',
       'id': 252382933,
       'lat': 51.195365,
       'lon': 11.9350775,
       'tags': {'amenity': 'biergarten', 'name': 'Güldene Hufe'}},
      {'type': 'node',
       'id': 253131440,
       'lat': 51.2972237,
       'lon': 12.0596469,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 254104727,
       'lat': 50.8356077,
       'lon': 8.3380138,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 254945660,
       'lat': 48.1992312,
       'lon': 11.5545614,
       'tags': {'amenity': 'biergarten',
        'name': 'Eschengarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 255049657,
       'lat': 52.4337259,
       'lon': 13.1642419,
       'tags': {'amenity': 'biergarten',
        'name': 'Haus Sanssouci',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 255138050,
       'lat': 49.8997417,
       'lon': 8.6933536,
       'tags': {'amenity': 'biergarten', 'created_by': 'Potlatch 0.8a'}},
      {'type': 'node',
       'id': 255466916,
       'lat': 48.6326899,
       'lon': 9.2077907,
       'tags': {'amenity': 'biergarten', 'name': 'Kelter'}},
      {'type': 'node',
       'id': 255559627,
       'lat': 51.3282424,
       'lon': 12.3434343,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'mexican',
        'name': 'Taverna tabasco'}},
      {'type': 'node',
       'id': 255628825,
       'lat': 48.3136854,
       'lon': 11.9100098,
       'tags': {'amenity': 'biergarten',
        'email': 'info@sommergarten-erding.de',
        'name': 'Sommergarten',
        'opening_hours': 'Mo-Fr 16:00-23:00, Sa-Su 11:30-23:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 255761704,
       'lat': 51.3965811,
       'lon': 7.1474739,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Deutschen'}},
      {'type': 'node',
       'id': 256666912,
       'lat': 48.7407947,
       'lon': 8.877328,
       'tags': {'amenity': 'biergarten', 'name': 'Gaststätte Säge'}},
      {'type': 'node',
       'id': 256910526,
       'lat': 50.1252149,
       'lon': 8.1687389,
       'tags': {'addr:city': 'Taunusstein',
        'addr:housenumber': '1',
        'addr:postcode': '65232',
        'addr:street': 'Eiserne Hand',
        'addr:suburb': 'Hahn',
        'amenity': 'biergarten',
        'email': 'info@waldgeist-xxl.de',
        'fax': '+49 6128 3108',
        'name': 'Waldgeist',
        'phone': '+49 6128 488911',
        'smoking': 'outside',
        'source': 'http://www.waldgeist-xxl.de/',
        'source:date': '2015-02-26',
        'website': 'http://www.waldgeist-xxl.de/'}},
      {'type': 'node',
       'id': 257405785,
       'lat': 48.2158609,
       'lon': 7.6613839,
       'tags': {'amenity': 'biergarten', 'name': 'Kiosk Rheinblick'}},
      {'type': 'node',
       'id': 257708389,
       'lat': 52.5406075,
       'lon': 13.2066054,
       'tags': {'addr:city': 'Berlin',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '13585',
        'addr:street': 'Neuendorfer Straße',
        'addr:suburb': 'Spandau',
        'amenity': 'biergarten',
        'capacity': '400',
        'name': 'Brauhaus Spandau',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 257800089,
       'lat': 49.5221304,
       'lon': 11.2759492,
       'tags': {'addr:city': 'Lauf a.d. Pegnitz',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '91207',
        'addr:street': 'Kunigundenberg',
        'addr:suburb': 'Kunigundenberg',
        'amenity': 'biergarten',
        'name': 'Biergarten Kunigundenberg',
        'operator': 'Jürgen Eichenmüller',
        'phone': '+49 179 5156157',
        'website': 'http://www.kunigundenberg.de/'}},
      {'type': 'node',
       'id': 259090434,
       'lat': 47.6078227,
       'lon': 11.3700084,
       'tags': {'addr:city': 'Jachenau',
        'addr:housenumber': '1',
        'addr:postcode': '83676',
        'addr:street': 'Sachenbach',
        'amenity': 'biergarten',
        'name': 'Kiosk Sachenbach',
        'note': 'Eigentlich nur Brotzeithütte, nur in der Hochsaison offen',
        'phone': '+49 8851 359',
        'toilets:wheelchair': 'no',
        'website': 'http://www.sachenbacher-walchensee.de/kiosk.html',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 259140678,
       'lat': 49.994239,
       'lon': 11.6851525,
       'tags': {'amenity': 'biergarten', 'name': 'Schwarzer Adler'}},
      {'type': 'node',
       'id': 259194341,
       'lat': 49.7320934,
       'lon': 6.6429046,
       'tags': {'addr:city': 'Trier',
        'addr:postcode': '54295',
        'addr:suburb': 'Feyen-Weismark',
        'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 259226099,
       'lat': 51.1383169,
       'lon': 7.1237864,
       'tags': {'amenity': 'biergarten', 'name': 'Tierheim Glüder'}},
      {'type': 'node',
       'id': 260193088,
       'lat': 48.3465235,
       'lon': 10.911171,
       'tags': {'addr:city': 'Augsburg',
        'addr:housenumber': '10e',
        'addr:street': 'Prof.-Steinbacher-Straße',
        'amenity': 'biergarten',
        'name': 'Parkhäusl',
        'toilets:wheelchair': 'no',
        'website': 'http://www.parkhaeusl.de/',
        'wheelchair': 'yes',
        'wheelchair:description': 'Biergarten mit Kiesboden, Stufen zur Essensausgabe'}},
      {'type': 'node',
       'id': 260795719,
       'lat': 49.0230659,
       'lon': 12.0958397,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10f',
        'name': 'Linde',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 260796705,
       'lat': 48.1204274,
       'lon': 11.6071809,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:postcode': '81671',
        'addr:street': 'Anzinger Straße',
        'amenity': 'biergarten',
        'delivery_hours': 'Mo-Su 17:00-21:30',
        'name': 'Wienerwald Biergarten',
        'opening_hours': 'Mo-Su 10:00-22:00',
        'phone': '+49 89 400767',
        'toilets:wheelchair': 'no',
        'website': 'http://www.wienerwald.de',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 261027014,
       'lat': 50.3248611,
       'lon': 11.9183497,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.8c',
        'name': 'Meinels Bas',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 261113086,
       'lat': 50.495037,
       'lon': 12.1317381,
       'tags': {'amenity': 'biergarten',
        'name': 'Vogtland-Garten',
        'opening_hours': 'Mo-Su 11:00-22:00; We 10:00-22:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 261602374,
       'lat': 51.4627777,
       'lon': 12.6732804,
       'tags': {'amenity': 'biergarten', 'created_by': 'JOSM'}},
      {'type': 'node',
       'id': 261754270,
       'lat': 48.7163316,
       'lon': 10.3749814,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 261758334,
       'lat': 47.9695378,
       'lon': 11.7697154,
       'tags': {'addr:city': 'Aying',
        'addr:country': 'DE',
        'addr:housenumber': '34',
        'addr:postcode': '85653',
        'addr:street': 'Bahnhofstraße',
        'amenity': 'biergarten',
        'brewery': 'Ayinger',
        'email': 'info@kastanienhof-aying.de',
        'fax': '+49 8095 872098',
        'name': 'Kastanienhof',
        'opening_hours': 'Tu-Su 11:00-23:00',
        'operator': 'Bekim Pergjegjaj',
        'phone': '+49 8095 9299',
        'source': 'survey',
        'website': 'http://www.kastanienhof-aying.de'}},
      {'type': 'node',
       'id': 262011127,
       'lat': 49.713587,
       'lon': 6.6282565,
       'tags': {'addr:city': 'Trier',
        'addr:housenumber': '88',
        'addr:postcode': '54296',
        'addr:street': 'Peter-Scholzen-Straße',
        'addr:suburb': 'Feyen-Weismark',
        'amenity': 'biergarten',
        'contact:phone': '+49 651 9914580',
        'name': 'Zum Römersprudel'}},
      {'type': 'node',
       'id': 262235326,
       'lat': 47.6355188,
       'lon': 9.8105981,
       'tags': {'amenity': 'biergarten',
        'food': 'yes',
        'name': 'Manfreds Bikermühle',
        'tourism': 'guest_house',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 262242827,
       'lat': 50.3907085,
       'lon': 6.7279463,
       'tags': {'amenity': 'biergarten', 'name': 'Alte Oelmühle'}},
      {'type': 'node',
       'id': 262310516,
       'lat': 51.5445569,
       'lon': 14.7222076,
       'tags': {'FIXME': 'Standort bitte prüfen',
        'amenity': 'biergarten',
        'name': 'Muskauer Hof',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 262359455,
       'lat': 50.8054003,
       'lon': 7.175791,
       'tags': {'amenity': 'biergarten',
        'created_by': 'JOSM',
        'name': 'Biergarten und Bootverleih'}},
      {'type': 'node',
       'id': 262372895,
       'lat': 51.1189102,
       'lon': 6.9425804,
       'tags': {'amenity': 'biergarten',
        'name': 'Bistro Marwil',
        'source': 'survey'}},
      {'type': 'node',
       'id': 262521564,
       'lat': 53.0070053,
       'lon': 13.3222681,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 262861161,
       'lat': 50.1873761,
       'lon': 10.8418844,
       'tags': {'amenity': 'biergarten',
        'name': 'Roter Ochse',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 262990426,
       'lat': 50.6475041,
       'lon': 8.7491489,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 263389412,
       'lat': 48.1147203,
       'lon': 11.614455,
       'tags': {'amenity': 'biergarten',
        'name': 'Alter Wirt',
        'opening_hours': 'Mo-Su 10:00-00:00'}},
      {'type': 'node',
       'id': 263563576,
       'lat': 50.6451408,
       'lon': 7.2071153,
       'tags': {'addr:postcode': '53424',
        'amenity': 'biergarten',
        'name': 'Siebengebirgsblick'}},
      {'type': 'node',
       'id': 263700591,
       'lat': 49.3504644,
       'lon': 8.1829873,
       'tags': {'amenity': 'biergarten',
        'name': 'Rothenbuschklause',
        'website': 'http://www.rothenbusch-klause.de/'}},
      {'type': 'node',
       'id': 263884191,
       'lat': 49.0379445,
       'lon': 8.3058099,
       'tags': {'amenity': 'biergarten',
        'name': 'Rheinterrasse',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 263904864,
       'lat': 48.1140705,
       'lon': 11.6137928,
       'tags': {'amenity': 'biergarten',
        'name': 'Zar',
        'opening_hours': 'Mo 11:00-00:00; Tu-Th 11:00-01:00; Fr 11:00-02:00; Sa 10:00-02:00; Su 11:00-00:00'}},
      {'type': 'node',
       'id': 264010995,
       'lat': 50.3555579,
       'lon': 11.6948462,
       'tags': {'amenity': 'biergarten', 'created_by': 'Potlatch 0.9a'}},
      {'type': 'node',
       'id': 264012141,
       'lat': 48.1303725,
       'lon': 11.6159096,
       'tags': {'amenity': 'biergarten', 'name': 'Padova', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 264072975,
       'lat': 48.0923177,
       'lon': 11.708083,
       'tags': {'amenity': 'biergarten',
        'name': 'Zur Einkehr',
        'source': 'survey'}},
      {'type': 'node',
       'id': 264073278,
       'lat': 48.0957588,
       'lon': 11.7274113,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthof Gut Keferloh',
        'opening_hours': 'Apr-Oct Mo-Su 11:00-18:00+',
        'source': 'Besuch am 24.07.2016',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 264349848,
       'lat': 48.66609,
       'lon': 9.1431816,
       'tags': {'addr:city': 'Leinfelden-Echterdingen',
        'addr:housenumber': '1',
        'addr:postcode': '70771',
        'addr:street': 'Schlösslesmühle',
        'amenity': 'biergarten',
        'name': 'Schlösslesmühle',
        'opening_hours': 'We-Fr 12:00-20:00, Sa-Su 11:00-19:00',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 264401775,
       'lat': 47.6290717,
       'lon': 7.5951422,
       'tags': {'amenity': 'biergarten', 'name': 'Löwen'}},
      {'type': 'node',
       'id': 264525151,
       'lat': 52.1073248,
       'lon': 11.6437569,
       'tags': {'amenity': 'biergarten',
        'name': 'Mückenwirt',
        'phone': '+49 391 5209337',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.mueckenwirt.de/',
        'wheelchair': 'yes',
        'wheelchair:description': 'Von hinten kann man mit dem Rollstuhl reinfahren und es gibt auch eine rollstuhlgerechte Toilette. Schlüssel beim Personal erfragen.'}},
      {'type': 'node',
       'id': 264527916,
       'lat': 48.1732593,
       'lon': 11.3959707,
       'tags': {'amenity': 'biergarten',
        'name': 'Waldwirtschaft Bienenheim',
        'opening_hours:old': 'Tu-Su 11:30-21:00; Mo off',
        'smoking': 'yes'}},
      {'type': 'node',
       'id': 265589528,
       'lat': 49.9940224,
       'lon': 8.360402,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten am Brunnen'}},
      {'type': 'node',
       'id': 265602713,
       'lat': 51.3059087,
       'lon': 13.3097325,
       'tags': {'addr:housenumber': '14a',
        'addr:street': 'Elbstraße',
        'amenity': 'biergarten',
        'name': 'Costa Riesa',
        'opening_hours': 'Mo-Su 11:30-23:30',
        'phone': '+49 3525518188'}},
      {'type': 'node',
       'id': 265939718,
       'lat': 49.2195972,
       'lon': 8.3702405,
       'tags': {'amenity': 'biergarten', 'name': 'Germania', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 266401191,
       'lat': 50.7885502,
       'lon': 7.2824538,
       'tags': {'amenity': 'biergarten', 'name': 'Sieglinde', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 266520713,
       'lat': 51.1220224,
       'lon': 6.1504373,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 266550133,
       'lat': 50.2848558,
       'lon': 11.909684,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 266679033,
       'lat': 51.3131027,
       'lon': 9.4881054,
       'tags': {'addr:city': 'Kassel',
        'addr:country': 'DE',
        'addr:housenumber': '8',
        'addr:postcode': '34117',
        'addr:street': 'Königstor',
        'amenity': 'biergarten',
        'name': 'Lohmann',
        'opening_hours': 'Su-Fr 11:00+; Sa 16:00+',
        'website': 'http://www.lohmann-kassel.de',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 266837599,
       'lat': 51.3044885,
       'lon': 12.2521618,
       'tags': {'amenity': 'biergarten',
        'name': 'Rotes Haus',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 266879031,
       'lat': 50.9610496,
       'lon': 14.1100983,
       'tags': {'addr:city': 'Bad Schandau',
        'addr:country': 'DE',
        'addr:housenumber': '36b',
        'addr:postcode': '01814',
        'addr:street': 'Waltersdorfer Mühle',
        'amenity': 'biergarten',
        'name': 'Waltersdorfer Mühle',
        'opening_hours': 'Tu-Su'}},
      {'type': 'node',
       'id': 267030617,
       'lat': 49.772716,
       'lon': 8.6282809,
       'tags': {'addr:city': 'Seeheim- Jugenheim',
        'addr:country': 'DE',
        'addr:housenumber': '27',
        'addr:postcode': '64342',
        'addr:street': 'Außerhalb',
        'amenity': 'biergarten',
        'email': 'info@seeheimer-waldgarten.de',
        'name': 'Seeheimer Waldgarten',
        'opening_hours': 'Mo-Th 15:00-23:00; Fr 15:00-24:00; Sa 11:00-24:00; Su 11:00-23:00',
        'phone': '+496257969497',
        'website': 'http://www.seeheimer-waldgarten.de'}},
      {'type': 'node',
       'id': 267045560,
       'lat': 51.8967292,
       'lon': 11.0741901,
       'tags': {'amenity': 'biergarten', 'name': 'Heine Bräu'}},
      {'type': 'node',
       'id': 267395860,
       'lat': 48.302824,
       'lon': 11.6149508,
       'tags': {'amenity': 'biergarten',
        'name': 'Echinger Gasthof',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 267411185,
       'lat': 49.2463497,
       'lon': 6.8790205,
       'tags': {'amenity': 'biergarten', 'name': 'Prellbock'}},
      {'type': 'node',
       'id': 267418965,
       'lat': 51.5117601,
       'lon': 11.9392392,
       'tags': {'addr:city': 'Halle (Saale)',
        'addr:country': 'DE',
        'addr:housenumber': '36',
        'addr:postcode': '06120',
        'addr:street': 'Fuchsbergstraße',
        'amenity': 'biergarten',
        'email': 'kgv_am_fuchsberg@t-online.de',
        'name': 'Haus am Fuchsberg',
        'phone': '+49-345-6 82 15 66',
        'website': 'http://www.kgv-am-fuchsberg-ev.de/vereinslokal.php'}},
      {'type': 'node',
       'id': 267466138,
       'lat': 50.8056648,
       'lon': 7.5888535,
       'tags': {'addr:housename': "Elmore's",
        'addr:housenumber': '5',
        'addr:street': 'Schönecker Weg',
        'amenity': 'biergarten',
        'name': "Elmore's"}},
      {'type': 'node',
       'id': 267620586,
       'lat': 49.7836344,
       'lon': 12.3096975,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 267620587,
       'lat': 49.7835532,
       'lon': 12.3067334,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 267620588,
       'lat': 49.7834219,
       'lon': 12.3082493,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 267779472,
       'lat': 50.7157826,
       'lon': 13.6063686,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 267952501,
       'lat': 49.047277,
       'lon': 7.8995461,
       'tags': {'amenity': 'biergarten',
        'name': 'Waldrestaurant Sankt Germanshof'}},
      {'type': 'node',
       'id': 267962781,
       'lat': 47.9626373,
       'lon': 11.3154101,
       'tags': {'amenity': 'biergarten',
        'name': 'Kiosk Schloßpark',
        'shop': 'kiosk'}},
      {'type': 'node',
       'id': 267963417,
       'lat': 48.1360261,
       'lon': 12.1615559,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Blümöd'}},
      {'type': 'node',
       'id': 267983226,
       'lat': 51.3071135,
       'lon': 12.2539762,
       'tags': {'amenity': 'biergarten', 'name': 'Strandhütte'}},
      {'type': 'node',
       'id': 267983229,
       'lat': 51.2951013,
       'lon': 12.2476127,
       'tags': {'amenity': 'biergarten',
        'name': 'Bratstübl',
        'outdoor_seating': 'yes'}},
      {'type': 'node',
       'id': 267983234,
       'lat': 51.3043263,
       'lon': 12.2608737,
       'tags': {'amenity': 'biergarten', 'name': 'Formel 1'}},
      {'type': 'node',
       'id': 268124660,
       'lat': 50.137172,
       'lon': 8.6460278,
       'tags': {'amenity': 'biergarten',
        'name': 'Zur Markus Quelle',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 268385274,
       'lat': 48.8252206,
       'lon': 11.7814578,
       'tags': {'addr:city': 'Bad Gögging',
        'addr:country': 'DE',
        'addr:postcode': '93333',
        'amenity': 'biergarten',
        'fixme': 'opening_hours=bis 21:57 ... wann bis wann?',
        'internet_access': 'no',
        'name': "Röll'n Biergarten",
        'smoking': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 268482990,
       'lat': 51.4184679,
       'lon': 7.0238896,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 268495953,
       'lat': 52.3526025,
       'lon': 10.5573915,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 268510904,
       'lat': 52.1914671,
       'lon': 9.0793483,
       'tags': {'addr:city': 'Rinteln',
        'addr:country': 'DE',
        'addr:housenumber': '8',
        'addr:postcode': '31737',
        'addr:street': 'Dankerser Straße',
        'amenity': 'biergarten',
        'food': 'yes',
        'name': 'Biergarten Am Weseranger',
        'outdoor_seating': 'yes',
        'website': 'http://www.biergarten-rinteln.de',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 268670315,
       'lat': 48.8988677,
       'lon': 11.8195244,
       'tags': {'amenity': 'biergarten',
        'description': '17.März – 29.März 2018\ntäglich 11:00 – 17:00 Uhr\n\n30.März – 31.Oktober 2018\ntäglich 09:30 – 19:00 Uhr',
        'name': 'Klosterschenke Weltenburg',
        'opening_hours': 'Mo-Su 09:30-19:00; Mo-Su 11:00-17:00',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 268819409,
       'lat': 49.2758015,
       'lon': 11.0198011,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Odorfer'}},
      {'type': 'node',
       'id': 268829794,
       'lat': 48.1368337,
       'lon': 11.2110195,
       'tags': {'amenity': 'biergarten', 'name': "Biergarten Zum unter'n Wirt"}},
      {'type': 'node',
       'id': 268849578,
       'lat': 48.5642089,
       'lon': 12.5975861,
       'tags': {'amenity': 'biergarten', 'name': 'Seehüttn', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 268944689,
       'lat': 50.5464917,
       'lon': 8.7387659,
       'tags': {'amenity': 'biergarten', 'name': 'Loukas'}},
      {'type': 'node',
       'id': 269039761,
       'lat': 48.3362467,
       'lon': 8.9501314,
       'tags': {'amenity': 'biergarten',
        'name': 'Hofgut Domäne',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.hofgut-domaene.de',
        'wheelchair': 'yes',
        'wheelchair:description': 'rollstuhlgerecht im Biergarten,\r\nRollstuhlgerechte Toilette im Restaurant La Paz (falls geschlossen: Schlüssel bei Bedienung erfragen)'}},
      {'type': 'node',
       'id': 269160343,
       'lat': 48.4272065,
       'lon': 10.0428404,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 269186770,
       'lat': 50.5257713,
       'lon': 10.5309345,
       'tags': {'amenity': 'biergarten', 'source': 'survey'}},
      {'type': 'node',
       'id': 269209697,
       'lat': 52.6375628,
       'lon': 9.9858235,
       'tags': {'addr:city': 'Hambühren',
        'addr:housenumber': '9',
        'addr:postcode': '29313',
        'addr:street': 'Im Dorfe',
        'amenity': 'biergarten',
        'email': 'luessmannshof@t-online.de',
        'name': 'Lüßmanns Hof',
        'phone': '(05084) 5343',
        'url': 'http://www.luessmannshof.de'}},
      {'type': 'node',
       'id': 269301642,
       'lat': 48.6905288,
       'lon': 11.804528,
       'tags': {'amenity': 'biergarten',
        'name': 'Schloßgarten Ratzenhofen',
        'opening_hours': 'Fr 15:00+, Sa 14:00+, PH Su 10:00+, Oct-Mar off',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.ratzenhofen.de/biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 269321998,
       'lat': 51.3031918,
       'lon': 12.2598853,
       'tags': {'amenity': 'biergarten',
        'description': 'ältester Biergarten in Leipzig',
        'name': 'Lausener Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 269413159,
       'lat': 48.4166153,
       'lon': 11.7274612,
       'tags': {'amenity': 'biergarten', 'name': 'Plantage', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 269414830,
       'lat': 49.7424356,
       'lon': 8.4813473,
       'tags': {'addr:city': 'Gernsheim',
        'addr:housenumber': '1',
        'addr:postcode': '64579',
        'addr:street': 'Auf der Hammeraue',
        'amenity': 'biergarten',
        'name': 'Treff am Badesee',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 269452007,
       'lat': 50.1048811,
       'lon': 8.6759384,
       'tags': {'amenity': 'biergarten',
        'name': 'maincafé',
        'website': 'http://www.maincafe.net',
        'wheelchair': 'limited',
        'wheelchair:description': 'im Sommer kann man barrierefrei draußen sitzen mit Blick auf die Skyline'}},
      {'type': 'node',
       'id': 269516700,
       'lat': 49.4415185,
       'lon': 8.6618083,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 269735681,
       'lat': 52.3595349,
       'lon': 9.7851541,
       'tags': {'amenity': 'biergarten',
        'name': 'Bischhofshol',
        'toilets:wheelchair': 'no',
        'website': 'http://www.hotel-bischofshol.de/',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 269774529,
       'lat': 49.2511906,
       'lon': 6.7319373,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 269784140,
       'lat': 51.6988532,
       'lon': 6.886951,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 269844229,
       'lat': 50.9767917,
       'lon': 11.0228553,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 269906748,
       'lat': 49.6185167,
       'lon': 11.1612102,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.9c',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 269951768,
       'lat': 50.9580523,
       'lon': 10.6716982,
       'tags': {'amenity': 'biergarten',
        'name': 'Berggarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 270127795,
       'lat': 50.1072608,
       'lon': 8.6822526,
       'tags': {'amenity': 'biergarten', 'name': 'Strandperle'}},
      {'type': 'node',
       'id': 270334040,
       'lat': 50.5606366,
       'lon': 12.7672382,
       'tags': {'amenity': 'biergarten', 'name': 'Hämmerle'}},
      {'type': 'node',
       'id': 270380204,
       'lat': 53.0774251,
       'lon': 8.8005416,
       'tags': {'amenity': 'biergarten',
        'name': 'Paulaner',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 270508798,
       'lat': 48.797856,
       'lon': 9.800424,
       'tags': {'amenity': 'biergarten',
        'atm': 'no',
        'internet_access': 'no',
        'name': 'Biergarten am Zeiselberg',
        'outdoor_seating': 'yes',
        'smoking': 'outside',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 270664185,
       'lat': 51.0427717,
       'lon': 11.6792331,
       'tags': {'amenity': 'biergarten',
        'email': 'post@saalerastplatz.de',
        'fax': '+49 34621 24728',
        'name': 'Saalerastplatz',
        'phone': '+49 36421 24736',
        'tourism': 'camp_site',
        'website': 'http://www.saalerastplatz.de'}},
      {'type': 'node',
       'id': 271236134,
       'lat': 48.1073692,
       'lon': 11.6548707,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.9c',
        'name': 'Zum Löwen',
        'opening_hours': 'Mo-Su,PH 09:00-24:00'}},
      {'type': 'node',
       'id': 271340144,
       'lat': 51.1584875,
       'lon': 12.8019146,
       'tags': {'amenity': 'biergarten', 'name': 'Sportlerheim'}},
      {'type': 'node',
       'id': 271376225,
       'lat': 49.7681294,
       'lon': 11.0569891,
       'tags': {'addr:city': 'Eggolsheim',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '91301',
        'addr:street': 'Bammersdorfer Straße',
        'amenity': 'biergarten',
        'name': 'Schwarzes Kreuz',
        'phone': '+49 176 43066637'}},
      {'type': 'node',
       'id': 271407244,
       'lat': 48.5085025,
       'lon': 12.1789652,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Berndorf',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 271417019,
       'lat': 51.0646416,
       'lon': 6.582904,
       'tags': {'amenity': 'biergarten', 'name': 'Kleinfelder Hof'}},
      {'type': 'node',
       'id': 271449962,
       'lat': 50.7261247,
       'lon': 7.1242361,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Blauen Affen',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 271754578,
       'lat': 48.5752308,
       'lon': 12.2267646,
       'tags': {'addr:street': 'Gretlmühle',
        'amenity': 'biergarten',
        'check_date': '2016-01-20',
        'name': 'Gretlmühle',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited',
        'wheelchair:description': 'Zugang nur mit Hilfe über Kies, unterfahrbare Tische (Biertische)'}},
      {'type': 'node',
       'id': 271791853,
       'lat': 51.3787234,
       'lon': 6.9812069,
       'tags': {'amenity': 'biergarten',
        'contact:email': 'info@12apostel-essen.de',
        'contact:phone': '+49 201 4902424',
        'name': 'Zwölf Apostel am Staadt Essen',
        'opening_hours': '11:00-24:00',
        'toilets:wheelchair': 'no',
        'website': 'http://www.12apostel-essen.de',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 271810351,
       'lat': 47.8258287,
       'lon': 11.3020283,
       'tags': {'amenity': 'biergarten',
        'name': 'Würmseestüberl',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 271892302,
       'lat': 52.0000352,
       'lon': 7.5595829,
       'tags': {'amenity': 'biergarten', 'note': 'geschlossen'}},
      {'type': 'node',
       'id': 271937565,
       'lat': 48.9171173,
       'lon': 9.3089293,
       'tags': {'amenity': 'biergarten',
        'name': 'Sieben Eichen',
        'opening_hours': 'tu-fr 16:00-23:00; sa 13:00-23:00; su 11:00-22:00',
        'phone': '+49 151 40140440',
        'toilets:wheelchair': 'no',
        'tourism': 'viewpoint',
        'website': 'http://www.7-eichen.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 272007561,
       'lat': 49.2688638,
       'lon': 6.8729897,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 272587842,
       'lat': 51.3667227,
       'lon': 6.9819107,
       'tags': {'addr:housenumber': '21',
        'addr:street': 'Zum Timpen',
        'amenity': 'biergarten',
        'name': 'Oefter Wald',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 273098855,
       'lat': 52.2872243,
       'lon': 7.9725462,
       'tags': {'amenity': 'biergarten',
        'name': 'Atterheide',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 273481350,
       'lat': 53.5349351,
       'lon': 9.8590725,
       'tags': {'amenity': 'biergarten', 'name': 'Holsten-Stube'}},
      {'type': 'node',
       'id': 273500587,
       'lat': 51.5640058,
       'lon': 6.8754476,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 273796068,
       'lat': 52.2016972,
       'lon': 8.7284499,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 273930476,
       'lat': 48.9504799,
       'lon': 9.428019,
       'tags': {'amenity': 'biergarten',
        'name': 'Hofgut Hagenbach',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes',
        'wheelchair:description': 'Platz ist geshottert.'}},
      {'type': 'node',
       'id': 274298709,
       'lat': 48.3888208,
       'lon': 9.998797,
       'tags': {'addr:city': 'Neu-Ulm',
        'addr:country': 'DE',
        'addr:housenumber': '6',
        'addr:postcode': '89231',
        'addr:street': 'Caponniere',
        'amenity': 'biergarten',
        'internet_access': 'wlan',
        'internet_access:fee': 'no',
        'microbrewery': 'yes',
        'name': 'Barfüßer-Biergarten im Glacis',
        'opening_hours': 'Mo-Fr 11:00-22:00; Sa-Su,PH 10:30-22:00 || off "Bei Dauerregen oder Kälte geschlossen"',
        'phone': '+49 731 4006630',
        'smoking': 'yes',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.biergarten-glacis.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 274343496,
       'lat': 51.2022144,
       'lon': 6.8021635,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 274668722,
       'lat': 48.7981687,
       'lon': 10.1096156,
       'tags': {'amenity': 'biergarten',
        'name': 'Kolpinghütte',
        'opening_hours': 'Su 10:00-20:00',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 274730904,
       'lat': 49.7775795,
       'lon': 11.1030142,
       'tags': {'amenity': 'biergarten',
        'ele': '410.605591',
        'name': 'Schwarzer Keller',
        'opening_hours': '"Nur im Sommer. 2017 jedoch mangels Pächter nicht in Betrieb."'}},
      {'type': 'node',
       'id': 274818965,
       'lat': 48.6745824,
       'lon': 10.1545161,
       'tags': {'addr:city': 'Heidenheim an der Brenz',
        'addr:country': 'DE',
        'addr:housenumber': '35',
        'addr:postcode': '89522',
        'addr:street': 'St. Pöltener Straße',
        'amenity': 'biergarten',
        'name': 'Gesellschaftsgarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 274858984,
       'lat': 48.5739317,
       'lon': 12.1062245,
       'tags': {'amenity': 'biergarten',
        'image': 'http://commons.wikimedia.org/wiki/File:GstaudachHuberwirt.jpg',
        'name': 'Huberwirt Gstaudach',
        'opening_hours': 'Mo-Sa 12:00-23:00; Su,PH 11:00-23:00; We off; "Küche bis 22 Uhr"',
        'toilets:wheelchair': 'yes',
        'url': 'http://www.huberwirt-gstaudach.de/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 274960638,
       'lat': 50.1657638,
       'lon': 9.0277267,
       'tags': {'amenity': 'biergarten',
        'name': 'Surfshop',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 274993140,
       'lat': 48.7946613,
       'lon': 9.2098864,
       'tags': {'addr:city': 'Stuttgart',
        'addr:housenumber': '26',
        'addr:street': 'Rudolfstraße',
        'amenity': 'biergarten',
        'name': 'Berger Plätzle',
        'operator': 'Männergesangsverein Stuttgart Berg 1856 e.V.'}},
      {'type': 'node',
       'id': 275039500,
       'lat': 48.6771886,
       'lon': 10.1547604,
       'tags': {'addr:city': 'Heidenheim an der Brenz',
        'addr:country': 'DE',
        'addr:housenumber': '18',
        'addr:postcode': '89518',
        'addr:street': 'Brenzstraße',
        'amenity': 'biergarten',
        'name': 'stattGarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 275228629,
       'lat': 49.3178442,
       'lon': 8.6780371,
       'tags': {'amenity': 'biergarten',
        'created_by': 'JOSM',
        'name': 'Zum Wiesenblick'}},
      {'type': 'node',
       'id': 275228670,
       'lat': 49.3147101,
       'lon': 8.6791668,
       'tags': {'amenity': 'biergarten',
        'created_by': 'JOSM',
        'name': 'Schützenverein'}},
      {'type': 'node',
       'id': 275346145,
       'lat': 50.5400966,
       'lon': 8.3804603,
       'tags': {'amenity': 'biergarten',
        'name': 'Campingplatz Schohleck',
        'website': 'http://www.lahntours.de/'}},
      {'type': 'node',
       'id': 275359278,
       'lat': 48.7280523,
       'lon': 11.1305468,
       'tags': {'amenity': 'biergarten', 'name': 'Fischerheim Beutmühle'}},
      {'type': 'node',
       'id': 275362085,
       'lat': 48.3596718,
       'lon': 10.9025093,
       'tags': {'amenity': 'biergarten',
        'name': "Murdock's Irish Pub",
        'opening_hours': 'Mo-Th 17:00-01:00, Fr,Sa 17:00-02:00, Su 11:00-24:00',
        'website': 'https://www.murdocks.de/',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 275556390,
       'lat': 49.4013475,
       'lon': 8.5786984,
       'tags': {'amenity': 'biergarten',
        'name': 'Welde Lustgarten',
        'opening_hours': 'Mo-Sa 15:00+; Su 10:00+'}},
      {'type': 'node',
       'id': 275631869,
       'lat': 51.1901464,
       'lon': 6.919967,
       'tags': {'amenity': 'biergarten', 'name': 'Sandbar'}},
      {'type': 'node',
       'id': 275662691,
       'lat': 48.7189715,
       'lon': 10.8476541,
       'tags': {'amenity': 'biergarten',
        'name': 'Schweizerhof',
        'phone': '+49-906-1816',
        'place': 'hamlet'}},
      {'type': 'node',
       'id': 275664368,
       'lat': 48.7193023,
       'lon': 10.8484681,
       'tags': {'amenity': 'biergarten',
        'email': 'info@roedter.de',
        'facebook': 'https://www.facebook.com/Biergarten-Schweizerhof-577064359077638',
        'name': 'Schweizerhof',
        'operator': 'Doris & Günter Rödter',
        'phone': '+49 906 1816',
        'smoking': 'outside',
        'website': 'http://biergarten-schweizerhof.com/'}},
      {'type': 'node',
       'id': 275961964,
       'lat': 49.790511,
       'lon': 8.6102416,
       'tags': {'amenity': 'biergarten',
        'name': 'Reiterschänke',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 276049769,
       'lat': 53.4512882,
       'lon': 7.8394399,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 276055530,
       'lat': 51.3042872,
       'lon': 12.56573,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.9c',
        'name': 'Gasthof Albrechtshain'}},
      {'type': 'node',
       'id': 276082848,
       'lat': 48.8056644,
       'lon': 9.0159261,
       'tags': {'addr:housenumber': '6',
        'addr:street': 'Strohgäustraße',
        'amenity': 'biergarten',
        'food': 'yes',
        'name': 'Paulaner Biergarten'}},
      {'type': 'node',
       'id': 276134997,
       'lat': 52.4297781,
       'lon': 13.3540651,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 276412486,
       'lat': 49.6037316,
       'lon': 11.3398291,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 276517177,
       'lat': 51.7706754,
       'lon': 9.3804845,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 276550285,
       'lat': 48.7079995,
       'lon': 9.5756381,
       'tags': {'amenity': 'biergarten',
        'name': 'Gerber Bräu',
        'operator': 'Gerber Bräu Gastronomie GmbH',
        'website': 'http://www.gerberbraeu.de'}},
      {'type': 'node',
       'id': 276694834,
       'lat': 50.1730442,
       'lon': 9.0384145,
       'tags': {'amenity': 'biergarten',
        'name': 'Dragonerbau',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 276806741,
       'lat': 51.0737553,
       'lon': 13.7013567,
       'tags': {'amenity': 'biergarten', 'operator': 'Wirtshaus Lindenschänke'}},
      {'type': 'node',
       'id': 276817787,
       'lat': 48.500759,
       'lon': 11.4522495,
       'tags': {'addr:city': 'Scheyern',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '85298',
        'addr:street': 'Schyrenplatz',
        'amenity': 'biergarten',
        'name': 'Klosterschenke',
        'phone': '+49844127890',
        'toilets:wheelchair': 'yes',
        'website': 'http://klosterschenke-scheyern.de/',
        'wheelchair': 'yes',
        'wheelchair:description': 'Die rollstuhlgerechte Toilette ist von links befahrbar.'}},
      {'type': 'node',
       'id': 276939031,
       'lat': 49.1554754,
       'lon': 11.7576758,
       'tags': {'FIXME': 'name', 'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 277028388,
       'lat': 50.6334205,
       'lon': 10.7407213,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 277244525,
       'lat': 51.6776608,
       'lon': 8.3467697,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 277271647,
       'lat': 48.426221,
       'lon': 11.5179079,
       'tags': {'amenity': 'biergarten',
        'name': 'Schloss Hohenkammer',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 277281040,
       'lat': 48.0881684,
       'lon': 9.209634,
       'tags': {'amenity': 'biergarten',
        'name': 'Bootshaus - Café - Restaurant',
        'opening_hours': 'Mo-Su,PH 10:00-22:00',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 277836007,
       'lat': 49.0321995,
       'lon': 8.2884844,
       'tags': {'amenity': 'biergarten', 'name': 'Bajazzo'}},
      {'type': 'node',
       'id': 278017774,
       'lat': 51.7115601,
       'lon': 12.2968747,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Bootshaus',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 278086562,
       'lat': 48.8122668,
       'lon': 8.210062,
       'tags': {'amenity': 'biergarten', 'name': 'Rantastic'}},
      {'type': 'node',
       'id': 278212261,
       'lat': 51.5626488,
       'lon': 7.4153404,
       'tags': {'amenity': 'biergarten',
        'name': 'Gut Königsmühle',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 278347762,
       'lat': 53.9960695,
       'lon': 11.4382656,
       'tags': {'amenity': 'biergarten', 'name': 'Zur Insel'}},
      {'type': 'node',
       'id': 278364067,
       'lat': 48.1155366,
       'lon': 11.541413,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '65',
        'addr:postcode': '81371',
        'addr:street': 'Wackersberger Straße',
        'amenity': 'biergarten',
        'name': 'Zum blauen Stern',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 278901866,
       'lat': 48.143627,
       'lon': 11.417126,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '7',
        'addr:postcode': '81249',
        'addr:street': 'Gößweinsteinplatz',
        'amenity': 'biergarten',
        'brewery': 'Augustiner Bräu München',
        'contact:fax': '089 872995',
        'contact:phone': '089 875581',
        'contact:website': 'http://www.aubinger-einkehr-muenchen.de/',
        'cuisine': 'regional',
        'name': 'Zur Aubinger Einkehr',
        'opening_hours': 'Mo-Fr 16:00-22:00; Sa-Su 12:00-22:30',
        'operator': 'Lydia Krajnik',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 279443892,
       'lat': 51.4733441,
       'lon': 7.0839142,
       'tags': {'amenity': 'biergarten',
        'name': 'Wolperding',
        'website': 'http://www.gaststaette-wolperding.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 279475415,
       'lat': 51.677775,
       'lon': 8.3457876,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 279715960,
       'lat': 48.2815722,
       'lon': 10.3312159,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10',
        'name': 'Gasthaus Hirsch Inh. Schafnitzel'}},
      {'type': 'node',
       'id': 279823301,
       'lat': 48.2027985,
       'lon': 7.9741735,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 279860478,
       'lat': 50.1304742,
       'lon': 8.7051121,
       'tags': {'amenity': 'biergarten',
        'name': 'Cafe im Günthersburgpark',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 279874223,
       'lat': 50.7112663,
       'lon': 7.0336685,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 279973149,
       'lat': 52.8233706,
       'lon': 12.0735408,
       'tags': {'amenity': 'biergarten',
        'name': 'Zur Alten Post',
        'toilets:wheelchair': 'no',
        'website': 'http://www.biergartenpension.de/tag.html',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 279989979,
       'lat': 51.0436024,
       'lon': 13.7898043,
       'tags': {'amenity': 'biergarten',
        'name': 'el Horst',
        'opening_hours': 'Oct-Apr: Mo-Fr 17:00-18:00+, Oct-Apr: Sa,PH 11:30-18:00+, May-Sep: Mo-Fr 15:00-18:00+, May-Sep: Sa,PH 11:30-18:00+'}},
      {'type': 'node',
       'id': 280079134,
       'lat': 51.6111935,
       'lon': 12.2423877,
       'tags': {'amenity': 'biergarten', 'name': 'Gartenlokal'}},
      {'type': 'node',
       'id': 280119904,
       'lat': 49.9039212,
       'lon': 6.541409,
       'tags': {'amenity': 'biergarten',
        'name': "Schilling's biergarten",
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 280589004,
       'lat': 52.5978619,
       'lon': 13.2750843,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 280726956,
       'lat': 48.221842,
       'lon': 10.1101378,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Schlossbräuhaus',
        'website': 'http://www.schloss-brauhaus.de',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 281053044,
       'lat': 50.1009692,
       'lon': 10.8559391,
       'tags': {'amenity': 'biergarten', 'name': 'Altes Brauhaus'}},
      {'type': 'node',
       'id': 281106162,
       'lat': 49.4375105,
       'lon': 8.6751244,
       'tags': {'addr:city': 'Heidelberg',
        'addr:housenumber': '30',
        'addr:postcode': '69121',
        'addr:street': 'Wiesenweg',
        'amenity': 'biergarten',
        'name': 'Züchterklause'}},
      {'type': 'node',
       'id': 281188615,
       'lat': 49.2816121,
       'lon': 8.1291462,
       'tags': {'amenity': 'biergarten',
        'name': 'König Ludwig Keller (Sommergarten)',
        'smoking': 'outside'}},
      {'type': 'node',
       'id': 281218337,
       'lat': 48.0771305,
       'lon': 11.7140129,
       'tags': {'amenity': 'biergarten',
        'name': 'Alter Wirt',
        'source': 'survey'}},
      {'type': 'node',
       'id': 281249773,
       'lat': 48.7158761,
       'lon': 10.7725964,
       'tags': {'amenity': 'biergarten', 'name': 'Kronenbiergarten'}},
      {'type': 'node',
       'id': 281328723,
       'lat': 51.3552029,
       'lon': 12.4407534,
       'tags': {'amenity': 'biergarten', 'name': 'Ostende'}},
      {'type': 'node',
       'id': 281436557,
       'lat': 51.4757159,
       'lon': 7.2159701,
       'tags': {'amenity': 'biergarten',
        'name': 'KAP',
        'opening_hours': '24/7',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 281437517,
       'lat': 48.7957118,
       'lon': 11.4393563,
       'tags': {'amenity': 'biergarten', 'name': 'Kastaniengarten'}},
      {'type': 'node',
       'id': 281505272,
       'lat': 47.5834311,
       'lon': 10.6855848,
       'tags': {'amenity': 'biergarten', 'name': 'Segelflugplatz'}},
      {'type': 'node',
       'id': 281563277,
       'lat': 50.2263485,
       'lon': 8.5786161,
       'tags': {'addr:city': 'Oberursel (Taunus)',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '61440',
        'addr:street': 'Friedrichstraße',
        'amenity': 'biergarten',
        'name': 'Zur Tante Anna',
        'source': 'survey'}},
      {'type': 'node',
       'id': 281728772,
       'lat': 51.5439768,
       'lon': 7.2376576,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10',
        'name': 'Treppchen',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 281729142,
       'lat': 50.7270826,
       'lon': 6.4548198,
       'tags': {'addr:city': 'Kreuzau',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '52372',
        'addr:street': 'Burgplatz',
        'amenity': 'biergarten',
        'fax': '+492422503701',
        'name': 'Gaststätte Hassert',
        'phone': '+4924227888',
        'source': 'survey'}},
      {'type': 'node',
       'id': 281787056,
       'lat': 47.9814488,
       'lon': 11.8638689,
       'tags': {'amenity': 'biergarten',
        'name': 'Wirtshaus an der Wiesmühle',
        'source': 'survey'}},
      {'type': 'node',
       'id': 281842059,
       'lat': 47.9972306,
       'lon': 11.1673493,
       'tags': {'amenity': 'biergarten',
        'name': 'Seewinkel',
        'opening_hours': 'Mo-Su 09:00-23:00',
        'outdoor_seating': 'yes',
        'shop': 'kiosk',
        'website': 'http://www.strandbad-herrsching.de/'}},
      {'type': 'node',
       'id': 281868811,
       'lat': 49.7286265,
       'lon': 11.0756969,
       'tags': {'addr:housenumber': '36',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Glocken-Keller',
        'tourism': 'attraction',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 281872588,
       'lat': 49.2245319,
       'lon': 9.2124805,
       'tags': {'amenity': 'biergarten', 'name': 'Reiterstüble'}},
      {'type': 'node',
       'id': 281890665,
       'lat': 51.1539676,
       'lon': 14.9840459,
       'tags': {'amenity': 'biergarten', 'name': 'Theater-Klause'}},
      {'type': 'node',
       'id': 282051363,
       'lat': 52.1579765,
       'lon': 11.6126341,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 282255306,
       'lat': 47.5897962,
       'lon': 9.5750301,
       'tags': {'amenity': 'biergarten', 'name': 'Dorfkrug Tunau'}},
      {'type': 'node',
       'id': 282374077,
       'lat': 53.1074808,
       'lon': 8.1308625,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 282433133,
       'lat': 48.9754559,
       'lon': 10.9043987,
       'tags': {'amenity': 'biergarten',
        'capacity': '1000',
        'food': 'yes',
        'name': 'Wettelsheimer Keller',
        'opening_hours': 'May-Sep Th-Su 10:00-sunset; Jul-Aug Mo-We 16:00-sunset'}},
      {'type': 'node',
       'id': 282517306,
       'lat': 52.1176879,
       'lon': 11.638457,
       'tags': {'amenity': 'biergarten',
        'name': 'Württemberg',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 282827235,
       'lat': 53.1691255,
       'lon': 8.6210436,
       'tags': {'amenity': 'biergarten', 'name': 'Strandlust Biergarten'}},
      {'type': 'node',
       'id': 282895845,
       'lat': 48.8078476,
       'lon': 9.1416676,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 283383076,
       'lat': 50.1021891,
       'lon': 8.5681277,
       'tags': {'addr:city': 'Frankfurt am Main',
        'addr:country': 'DE',
        'addr:housenumber': '16',
        'addr:postcode': '65934',
        'addr:street': 'Oeserstraße',
        'addr:suburb': 'Nied',
        'amenity': 'biergarten',
        'contact:fax': '+49 69 93998610',
        'contact:phone': '+49 69 396211',
        'contact:website': 'http://www.zur-waldlust.de/',
        'cuisine': 'regional',
        'name': 'Zur Waldlust',
        'source': 'http://www.zur-waldlust.de/',
        'source:date': '2017-07-17',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 283430892,
       'lat': 48.4796065,
       'lon': 10.929428,
       'tags': {'amenity': 'biergarten', 'name': 'Schloss Scherneck'}},
      {'type': 'node',
       'id': 283430896,
       'lat': 48.4785522,
       'lon': 10.9291168,
       'tags': {'amenity': 'biergarten', 'name': 'Bögenhof'}},
      {'type': 'node',
       'id': 283694750,
       'lat': 50.5185398,
       'lon': 7.0211529,
       'tags': {'amenity': 'biergarten', 'name': 'Saffenburg'}},
      {'type': 'node',
       'id': 284233342,
       'lat': 49.4149136,
       'lon': 8.6636299,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 285748237,
       'lat': 50.6266427,
       'lon': 6.9471805,
       'tags': {'amenity': 'biergarten', 'name': 'Brauhaus'}},
      {'type': 'node',
       'id': 285774180,
       'lat': 50.8712761,
       'lon': 8.0138662,
       'tags': {'amenity': 'biergarten', 'name': 'Hammerhütte'}},
      {'type': 'node',
       'id': 285957181,
       'lat': 53.0690439,
       'lon': 8.8112557,
       'tags': {'addr:city': 'Bremen',
        'addr:housenumber': '58-60',
        'addr:postcode': '28199',
        'addr:street': 'Werderstraße',
        'amenity': 'biergarten',
        'name': 'Beachclub White Pearl',
        'website': 'http://www.white-pearl-beach.de/start.html',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 285989986,
       'lat': 49.491274,
       'lon': 11.8199093,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthof Kopf'}},
      {'type': 'node',
       'id': 286065873,
       'lat': 50.8814204,
       'lon': 9.7433712,
       'tags': {'addr:city': 'Bad Hersfeld',
        'addr:housenumber': '1',
        'addr:postcode': '36251',
        'addr:street': 'Gut Oberrode',
        'amenity': 'biergarten',
        'contact:facebook': 'https://www.facebook.com/BiergartenZurWeissenDame',
        'contact:google_plus': 'https://plus.google.com/105236482377394601299',
        'contact:mobile': '+49 1777 868573',
        'name': 'Zur weißen Dame'}},
      {'type': 'node',
       'id': 286428202,
       'lat': 52.0232229,
       'lon': 8.8232639,
       'tags': {'addr:city': 'Lemgo',
        'addr:country': 'DE',
        'addr:housenumber': '201',
        'addr:postcode': '32657',
        'addr:street': 'Bielefelder Straße',
        'amenity': 'biergarten',
        'name': 'Fricke'}},
      {'type': 'node',
       'id': 286611675,
       'lat': 49.9535555,
       'lon': 10.8608686,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Merkaartor 0.11',
        'name': "Leicht's Keller"}},
      {'type': 'node',
       'id': 286678130,
       'lat': 48.334483,
       'lon': 10.8264065,
       'tags': {'amenity': 'biergarten',
        'name': 'Wellenburger Biergarten',
        'opening_hours': 'Mo-Fr 11:00-24:00; Sa,Su 10:00-24:00',
        'website': 'http://www.schlossgaststaette-wellenburg.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 286806232,
       'lat': 49.6391427,
       'lon': 11.3550459,
       'tags': {'amenity': 'biergarten',
        'name': 'Hopfengärten',
        'smoking': 'yes'}},
      {'type': 'node',
       'id': 287062955,
       'lat': 51.7326654,
       'lon': 11.0249859,
       'tags': {'amenity': 'biergarten', 'name': 'Harzer Biergarten'}},
      {'type': 'node',
       'id': 287088708,
       'lat': 52.3612414,
       'lon': 9.7351541,
       'tags': {'addr:city': 'Hannover',
        'addr:country': 'DE',
        'amenity': 'biergarten',
        'contact:phone': '+49 511 8060610',
        'name': 'See Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 287109008,
       'lat': 50.9310092,
       'lon': 12.0154233,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Köstritzer',
        'cuisine': 'german',
        'name': 'Zum Frosch',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 287158256,
       'lat': 49.6403074,
       'lon': 10.5933638,
       'tags': {'amenity': 'biergarten',
        'drink:club-mate': 'yes',
        'name': 'Brauerei Loscher'}},
      {'type': 'node',
       'id': 287223905,
       'lat': 50.9258256,
       'lon': 6.9656214,
       'tags': {'amenity': 'biergarten', 'source': 'photography'}},
      {'type': 'node',
       'id': 287252734,
       'lat': 51.8700972,
       'lon': 13.9703984,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Am Spreeschlößchen',
        'phone': '+49 3542 403712'}},
      {'type': 'node',
       'id': 287394655,
       'lat': 48.3944503,
       'lon': 7.8091687,
       'tags': {'amenity': 'biergarten', 'name': 'Seeterrass'}},
      {'type': 'node',
       'id': 287454428,
       'lat': 51.7859767,
       'lon': 10.9667491,
       'tags': {'amenity': 'biergarten', 'name': 'Großvater'}},
      {'type': 'node',
       'id': 287505176,
       'lat': 49.7285264,
       'lon': 11.0760855,
       'tags': {'addr:housenumber': '15',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'name': 'Stäffala-Keller',
        'tourism': 'attraction',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 287505177,
       'lat': 49.7289506,
       'lon': 11.0775953,
       'tags': {'addr:housenumber': '13',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'name': 'Schlößla-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 287505209,
       'lat': 49.7282355,
       'lon': 11.0765791,
       'tags': {'addr:housenumber': '17',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'name': 'Eichhorn-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 287505223,
       'lat': 49.7281187,
       'lon': 11.0763543,
       'tags': {'addr:housenumber': '19',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Weiß-Tauben-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 287505235,
       'lat': 49.7278597,
       'lon': 11.076588,
       'tags': {'addr:housenumber': '21',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'name': 'Hoffmanns-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 287598521,
       'lat': 47.5479891,
       'lon': 10.2175291,
       'tags': {'amenity': 'biergarten',
        'created_by': 'xybot',
        'name': 'Berghütte'}},
      {'type': 'node',
       'id': 287745810,
       'lat': 48.9258909,
       'lon': 9.0780985,
       'tags': {'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Enzeckstüble',
        'opening_hours': 'Su 09:00-19:00;PH 09:00-19:00'}},
      {'type': 'node',
       'id': 288163177,
       'lat': 50.0516981,
       'lon': 11.3221875,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 288263249,
       'lat': 53.5155834,
       'lon': 9.9988306,
       'tags': {'addr:city': 'Hamburg',
        'addr:country': 'DE',
        'addr:housenumber': '123',
        'addr:postcode': '21107',
        'addr:street': 'Vogelhüttendeich',
        'amenity': 'biergarten',
        'food': 'yes',
        'name': 'Zum Anleger',
        'opening_hours': 'Mo-Fr 11:30+; Sa-Su 10:00+',
        'phone': '+49 40 86687781',
        'website': 'http://www.zum-anleger.de/biergarten/index.html',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 288463354,
       'lat': 50.9811296,
       'lon': 7.0242762,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 288718686,
       'lat': 51.7398631,
       'lon': 11.0196959,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 288894075,
       'lat': 50.5642997,
       'lon': 6.9669973,
       'tags': {'amenity': 'biergarten',
        'name': 'Cafe in der alten Scheune',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 288957193,
       'lat': 48.9784262,
       'lon': 8.1825416,
       'tags': {'amenity': 'biergarten',
        'name': 'Bayrischer Hof',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 289139510,
       'lat': 52.2412496,
       'lon': 13.1514555,
       'tags': {'amenity': 'biergarten', 'created_by': 'Merkaartor 0.11'}},
      {'type': 'node',
       'id': 289192491,
       'lat': 49.4510853,
       'lon': 11.0910124,
       'tags': {'amenity': 'biergarten',
        'name': "Wies'n Biergarten",
        'opening_hours': 'Mo-Fr 10:00-22:00; Sa 13:00-22:00; Su 10:00-22:00; Oct-Apr: off',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.wiesn-biergarten.de',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289240522,
       'lat': 51.43035,
       'lon': 11.974891,
       'tags': {'amenity': 'biergarten',
        'name': 'An der Broihanschenke (Schuppen)',
        'opening_hours': 'Tu-We 15:00-20:00; Th 15:00-20:30; Fr 15:00-21:00; Sa 15:00-22:00; Su 16:00-20:00',
        'operator': 'R. Gaßmann',
        'phone': '+49 345 7709592',
        'postal_code': '06132'}},
      {'type': 'node',
       'id': 289352212,
       'lat': 49.7277317,
       'lon': 11.0768287,
       'tags': {'addr:housenumber': '23',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Schwanenkeller',
        'tourism': 'attraction',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 289352754,
       'lat': 49.7275653,
       'lon': 11.0769059,
       'tags': {'addr:housenumber': '25',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Neder-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289352834,
       'lat': 49.7272099,
       'lon': 11.0775276,
       'tags': {'addr:housenumber': '27',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Schützenhaus-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289353800,
       'lat': 49.7295974,
       'lon': 11.0748857,
       'tags': {'addr:housenumber': '9',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Greif-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289354021,
       'lat': 49.7295039,
       'lon': 11.0754972,
       'tags': {'addr:housenumber': '28',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Schindler-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 289354132,
       'lat': 49.729566,
       'lon': 11.075887,
       'tags': {'addr:housenumber': '30',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'name': 'Nürnberger-Tor-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 289354225,
       'lat': 49.7294197,
       'lon': 11.0750316,
       'tags': {'addr:housenumber': '24',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Schäffbräu-Keller',
        'tourism': 'attraction',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 289354226,
       'lat': 49.7293122,
       'lon': 11.0748814,
       'tags': {'addr:housenumber': '22',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Hebendanz-Keller',
        'tourism': 'attraction',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 289354231,
       'lat': 49.7292186,
       'lon': 11.0747473,
       'tags': {'addr:housenumber': '12a',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Kronen-Keller',
        'tourism': 'attraction',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 289354314,
       'lat': 49.729158,
       'lon': 11.0745488,
       'tags': {'addr:housenumber': '18',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Fritz-Schneider-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 289354315,
       'lat': 49.7290713,
       'lon': 11.0744134,
       'tags': {'addr:housenumber': '14',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Rappen-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 289354646,
       'lat': 49.7291416,
       'lon': 11.0739631,
       'tags': {'addr:housenumber': '7',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Winterbauer-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289354669,
       'lat': 49.728809,
       'lon': 11.0742127,
       'tags': {'addr:housenumber': '12',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Löwenbräu-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 289354709,
       'lat': 49.7289031,
       'lon': 11.0736529,
       'tags': {'addr:housenumber': '3',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Fäßla-Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 289354815,
       'lat': 49.7287035,
       'lon': 11.0740144,
       'tags': {'addr:housenumber': '8',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'building': 'yes',
        'cuisine': 'regional',
        'name': 'Kaiser-Keller',
        'tourism': 'attraction',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 289354915,
       'lat': 49.7286077,
       'lon': 11.0737328,
       'tags': {'addr:housenumber': '2a',
        'addr:street': 'Auf den Kellern',
        'amenity': 'biergarten',
        'name': 'Kupfer-Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289499087,
       'lat': 52.3769308,
       'lon': 9.7115922,
       'tags': {'addr:city': 'Hannover',
        'addr:housenumber': '3',
        'addr:postcode': '30451',
        'addr:street': 'Zur Bettfedernfabrik',
        'amenity': 'biergarten',
        'drink:club-mate': 'served',
        'name': 'Gretchen',
        'smoking': 'outside',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 289696138,
       'lat': 51.1932318,
       'lon': 6.9969863,
       'tags': {'amenity': 'biergarten',
        'name': 'Zur Brücke',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 289705336,
       'lat': 48.5369997,
       'lon': 12.1494071,
       'tags': {'amenity': 'biergarten',
        'lastcheck': '2015-12-14',
        'note': "kein name tag, weil der zu 'zur Insel gehoert'"}},
      {'type': 'node',
       'id': 289736561,
       'lat': 51.5473909,
       'lon': 7.68657,
       'tags': {'amenity': 'biergarten',
        'name': 'Cafe im Kurpark',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 289742037,
       'lat': 54.4737343,
       'lon': 13.4478765,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 290005552,
       'lat': 51.5046876,
       'lon': 7.0276221,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10f',
        'name': 'Fun'}},
      {'type': 'node',
       'id': 290098167,
       'lat': 51.4244039,
       'lon': 7.487431,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 290098205,
       'lat': 51.4372553,
       'lon': 7.570048,
       'tags': {'amenity': 'biergarten',
        'name': 'Rohrmeisterei',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 290098300,
       'lat': 51.4639246,
       'lon': 7.5575486,
       'tags': {'amenity': 'biergarten',
        'name': 'Freischütz',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 290595745,
       'lat': 50.8676188,
       'lon': 6.0991242,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10b',
        'name': 'Zum Seehof'}},
      {'type': 'node',
       'id': 290679380,
       'lat': 48.2903093,
       'lon': 11.6350709,
       'tags': {'amenity': 'biergarten', 'name': 'Kiosk Echinger See'}},
      {'type': 'node',
       'id': 290696756,
       'lat': 52.4113223,
       'lon': 9.3803453,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Dorfkrug',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 290713960,
       'lat': 47.7410953,
       'lon': 9.1326662,
       'tags': {'amenity': 'biergarten', 'name': 'Ziegelhofstube'}},
      {'type': 'node',
       'id': 290723117,
       'lat': 49.3167592,
       'lon': 8.4502045,
       'tags': {'addr:city': 'Speyer',
        'addr:country': 'DE',
        'addr:housenumber': '1 c',
        'addr:postcode': '67346',
        'addr:street': 'Leinpfad',
        'amenity': 'biergarten',
        'name': 'Zur Schiffbrücke / Alter Hammer',
        'website': 'http://www.alter-hammer.de',
        'wheelchair:description': 'Biergarten ebenerdig und schwellenlos erreichbar'}},
      {'type': 'node',
       'id': 290766308,
       'lat': 50.9197424,
       'lon': 6.1182358,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten & Schänke',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 290786680,
       'lat': 52.2614488,
       'lon': 10.3749865,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 290865734,
       'lat': 49.993228,
       'lon': 8.6579873,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 290944791,
       'lat': 49.9854241,
       'lon': 8.3180682,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 291046129,
       'lat': 51.1509821,
       'lon': 13.8060997,
       'tags': {'amenity': 'biergarten', 'name': 'Lausaer Biergarten'}},
      {'type': 'node',
       'id': 291078184,
       'lat': 52.0036197,
       'lon': 11.7236908,
       'tags': {'addr:city': 'Schönebeck (Elbe)',
        'addr:housenumber': '4',
        'addr:postcode': '39218',
        'addr:street': 'Elmener Straße',
        'amenity': 'biergarten',
        'brewery': 'yes',
        'name': 'Alt-Salzer Stube',
        'outdoor_seating': 'yes'}},
      {'type': 'node',
       'id': 291167509,
       'lat': 53.5575095,
       'lon': 9.9676227,
       'tags': {'amenity': 'biergarten', 'name': 'Pförtnerhäuschen Bar'}},
      {'type': 'node',
       'id': 291431854,
       'lat': 49.9247466,
       'lon': 11.5993304,
       'tags': {'amenity': 'biergarten',
        'name': 'Storchenkeller',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 291874114,
       'lat': 47.8685617,
       'lon': 12.6211988,
       'tags': {'amenity': 'biergarten',
        'name': 'Angerbauer Hof',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 292140659,
       'lat': 48.9121649,
       'lon': 9.1831313,
       'tags': {'amenity': 'biergarten',
        'name': 'Ständle am alten Bahnhof',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 292309963,
       'lat': 52.3352273,
       'lon': 9.7717554,
       'tags': {'ID_SLH_IMPORT': '21218',
        'addr:city': 'Hannover',
        'addr:country': 'DE',
        'addr:housenumber': '293',
        'addr:postcode': '30519',
        'addr:street': 'Hildesheimer Straße',
        'amenity': 'biergarten',
        'entrance': 'yes',
        'level': '0',
        'name': 'Döhrener Biergarten',
        'note': "Position is precisely entrance of building, please don't move position but transfer information from duplicate node to here / embed in building polygon and connect footways. Testing area for blind user's navigation software LoroDux! Contact: Lulu-Ann",
        'source': 'Selbstbestimmt Leben Hannover e.V. Import 1',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 292643941,
       'lat': 50.9332727,
       'lon': 11.879591,
       'tags': {'addr:city': 'Weißenborn',
        'addr:housenumber': '12',
        'addr:postcode': '07639',
        'addr:street': 'Mühltal',
        'amenity': 'biergarten',
        'contact:phone': '+49 36601 555 950',
        'contact:website': 'http://www.meuschkensmuehle-muehltal.de/',
        'name': 'Meuschkensmühle',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 292713493,
       'lat': 49.9280068,
       'lon': 9.8029223,
       'tags': {'addr:postcode': '97267',
        'addr:street': 'Mainstraße',
        'amenity': 'biergarten',
        'name': 'Downtown',
        'phone': '+49 160 92107152',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 292847724,
       'lat': 51.4698958,
       'lon': 6.9034879,
       'tags': {'addr:city': 'Mülheim an der Ruhr',
        'addr:country': 'DE',
        'addr:housenumber': '58',
        'addr:postcode': '45475',
        'addr:street': 'Hexberg',
        'amenity': 'biergarten',
        'name': 'Liebling im Mühlenbach',
        'website': 'http://www.liebling-mh.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 292910957,
       'lat': 48.1429303,
       'lon': 11.5785962,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '18',
        'addr:postcode': '80539',
        'addr:street': 'Odeonsplatz',
        'amenity': 'biergarten',
        'name': 'Tambosi Hofgarten',
        'opening_hours': 'Su-Th 07:00-01:00; Sa-Su 07:00-03:00',
        'operator': 'Tambosi Crocamo GmbH',
        'phone': '+49 89 23069360',
        'wheelchair': 'no',
        'wheelchair:description': 'Eingang zum Restaurant mit 5cm Stufe o.k., aber keine rollstuhlgerechten Toiletten vorhanden. Zugang zum Buergarten ebenerdig.'}},
      {'type': 'node',
       'id': 292948666,
       'lat': 49.6861564,
       'lon': 8.9956758,
       'tags': {'addr:housenumber': '38',
        'addr:postcode': '64720',
        'addr:street': 'Schloßstraße',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Nicks Biergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 292956676,
       'lat': 51.8955757,
       'lon': 12.2060288,
       'tags': {'amenity': 'biergarten', 'name': 'Die kleine Kneipe'}},
      {'type': 'node',
       'id': 293020035,
       'lat': 48.3456677,
       'lon': 10.3805271,
       'tags': {'amenity': 'biergarten', 'name': "Heiner's Waldschenke"}},
      {'type': 'node',
       'id': 293224485,
       'lat': 51.3619551,
       'lon': 6.9526653,
       'tags': {'amenity': 'biergarten', 'name': 'KTG'}},
      {'type': 'node',
       'id': 293236329,
       'lat': 48.528934,
       'lon': 12.201967,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthaus Rahbauer',
        'opening_hours': 'Sa 12:00-00:00; Su 11:00-00:00'}},
      {'type': 'node',
       'id': 293391192,
       'lat': 51.6493049,
       'lon': 12.3041508,
       'tags': {'amenity': 'biergarten', 'name': "Pepp's Bierstuben"}},
      {'type': 'node',
       'id': 293638075,
       'lat': 49.3735516,
       'lon': 7.0820037,
       'tags': {'amenity': 'biergarten',
        'name': 'Wachdersch',
        'opening_hours': 'Tu-Su,PH 18:00-01:00+',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 294194541,
       'lat': 48.5890072,
       'lon': 11.7615164,
       'tags': {'amenity': 'biergarten', 'name': 'Kirchenwirt'}},
      {'type': 'node',
       'id': 294562731,
       'lat': 48.6874852,
       'lon': 9.0073992,
       'tags': {'amenity': 'biergarten', 'name': 'Femy', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 294973408,
       'lat': 47.7364434,
       'lon': 9.2350551,
       'tags': {'amenity': 'biergarten',
        'email': 'info@moeking.de',
        'name': 'Möking',
        'phone': '+49 7556 6010',
        'website': 'http://www.bodenseeferienwohnung.com/',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 295000228,
       'lat': 52.3277313,
       'lon': 9.7769052,
       'tags': {'addr:city': 'Hannover',
        'addr:country': 'DE',
        'addr:housenumber': '380',
        'addr:postcode': '30519',
        'addr:street': 'Hildesheimer Straße',
        'amenity': 'biergarten',
        'name': 'Wülfeler Biergarten',
        'phone': '0511 876060',
        'website': 'http://www.wuelfeler-biergarten.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 295023126,
       'lat': 48.1571718,
       'lon': 12.8214208,
       'tags': {'amenity': 'biergarten', 'name': 'St. Johann'}},
      {'type': 'node',
       'id': 295905741,
       'lat': 51.3961365,
       'lon': 7.4313029,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 296012524,
       'lat': 48.1636774,
       'lon': 11.5356055,
       'tags': {'amenity': 'biergarten',
        'name': 'Zur Geyerwally',
        'opening_hours': 'Tu-Su 11:00-18:00+',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 296061362,
       'lat': 51.9432537,
       'lon': 7.1671898,
       'tags': {'amenity': 'biergarten',
        'name': 'Haselhoff',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 296076280,
       'lat': 49.638041,
       'lon': 8.9799009,
       'tags': {'amenity': 'biergarten',
        'name': 'Zur Hütte',
        'opening_hours': 'Fr-Sa 16:00-19:00;Su 10:00-19:00'}},
      {'type': 'node',
       'id': 296080652,
       'lat': 49.6365098,
       'lon': 8.9767147,
       'tags': {'addr:housenumber': '3',
        'addr:street': 'Geißbergweg',
        'amenity': 'biergarten',
        'name': "Berndl's Pilsstube"}},
      {'type': 'node',
       'id': 296152930,
       'lat': 48.403727,
       'lon': 10.4628403,
       'tags': {'amenity': 'biergarten', 'name': 'Holgenwirt'}},
      {'type': 'node',
       'id': 296520346,
       'lat': 52.3772124,
       'lon': 9.7130914,
       'tags': {'amenity': 'biergarten', 'name': 'Strandleben'}},
      {'type': 'node',
       'id': 296957931,
       'lat': 48.1405917,
       'lon': 11.6824418,
       'tags': {'amenity': 'biergarten',
        'name': 'Prinzregenten-Garten',
        'operator': 'Hotel Prinzregent an der Messe'}},
      {'type': 'node',
       'id': 297055270,
       'lat': 48.7978163,
       'lon': 9.1523584,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten im Tal',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 297164456,
       'lat': 50.0987299,
       'lon': 8.2295159,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 297233488,
       'lat': 52.5697896,
       'lon': 13.3942046,
       'tags': {'amenity': 'biergarten',
        'name': 'Rosengarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 297254100,
       'lat': 49.4180456,
       'lon': 8.7418856,
       'tags': {'addr:city': 'Heidelberg',
        'addr:country': 'DE',
        'addr:housenumber': '130/1',
        'addr:postcode': '69118',
        'addr:street': 'In der Neckarhelle',
        'addr:suburb': 'Ziegelhausen',
        'amenity': 'biergarten',
        'contact:facebook': 'https://www.facebook.com/Steffis-Klause-438885742972134/',
        'name': "Steffi's Klause",
        'old_name': "Hucky's Klause",
        'phone': '+49 1525 9075605',
        'source': 'survey'}},
      {'type': 'node',
       'id': 297303348,
       'lat': 49.8714952,
       'lon': 9.1846728,
       'tags': {'amenity': 'biergarten', 'name': 'Waldeck'}},
      {'type': 'node',
       'id': 297494989,
       'lat': 51.067774,
       'lon': 13.777873,
       'tags': {'amenity': 'biergarten',
        'name': 'Brauhaus am Waldschlößchen',
        'opening_hours': 'Mo-Su 11:00-01:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 297675029,
       'lat': 49.1835468,
       'lon': 11.1832262,
       'tags': {'addr:city': 'Hilpoltstein',
        'addr:country': 'DE',
        'addr:housenumber': '8',
        'addr:postcode': '91161',
        'addr:street': 'Dieselstraße',
        'amenity': 'biergarten',
        'brewery': 'Hofmühl',
        'name': 'Bistro',
        'phone': '+49 9174 48483'}},
      {'type': 'node',
       'id': 297985885,
       'lat': 51.0343448,
       'lon': 13.7604399,
       'tags': {'amenity': 'biergarten',
        'opening_hours': 'Apr-Oct: Mo-Fr 11:00-19:00; Sa-Su 10:00-19:00; PH 10:00-19:00',
        'phone': '+49 152 37 00 67 53',
        'website': 'https://www.grosser-garten-dresden.de/de/gaesteservice/gastronomie-shop/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 298915411,
       'lat': 48.3964149,
       'lon': 9.9542964,
       'tags': {'addr:housenumber': '45',
        'addr:postcode': '89077',
        'addr:street': 'Klosterhof',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Klosterhof Ulm',
        'opening_hours': 'Mo -Su 11:00 - 24:00',
        'website': 'http://www.klosterhofulm.de/'}},
      {'type': 'node',
       'id': 298992729,
       'lat': 49.4442505,
       'lon': 8.6192695,
       'tags': {'addr:city': 'Edingen-Neckarhausen',
        'addr:country': 'DE',
        'addr:postcode': '68535',
        'addr:suburb': 'Edingen',
        'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 299072879,
       'lat': 52.4344273,
       'lon': 9.4067196,
       'tags': {'amenity': 'biergarten',
        'name': "Alten's Ruh",
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 299108936,
       'lat': 49.9337425,
       'lon': 10.8283935,
       'tags': {'amenity': 'biergarten',
        'name': 'Kraft-Keller',
        'website': 'http://www.brauerei-eichhorn.de'}},
      {'type': 'node',
       'id': 299248249,
       'lat': 51.3879228,
       'lon': 6.9437787,
       'tags': {'amenity': 'biergarten',
        'name': 'Road Stop',
        'opening_hours': 'Su-Th 11:00-24:00, Fr,Sa 11:00-01:00',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 299465327,
       'lat': 49.7215448,
       'lon': 8.993351,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 300086101,
       'lat': 49.2910465,
       'lon': 7.574426,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 300128653,
       'lat': 50.9766939,
       'lon': 11.0267643,
       'tags': {'amenity': 'biergarten',
        'drink:beer': 'served',
        'name': 'Noah',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 300294178,
       'lat': 48.7559433,
       'lon': 9.7827311,
       'tags': {'amenity': 'biergarten', 'name': 'Burgschänke Rechberg'}},
      {'type': 'node',
       'id': 300327588,
       'lat': 52.5422827,
       'lon': 13.2816533,
       'tags': {'amenity': 'biergarten',
        'name': 'Kulturbiergarten Jungfernheide'}},
      {'type': 'node',
       'id': 300379701,
       'lat': 47.6504983,
       'lon': 9.4825666,
       'tags': {'amenity': 'biergarten',
        'name': 'Platanengarten',
        'note': '(nur im Sommer)',
        'outdoor_seating': 'only',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 300398643,
       'lat': 49.6295464,
       'lon': 11.25241,
       'tags': {'amenity': 'biergarten',
        'name': 'Klostergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 300424548,
       'lat': 47.9445415,
       'lon': 11.258104,
       'tags': {'amenity': 'biergarten', 'name': 'Alter Wirt'}},
      {'type': 'node',
       'id': 300596043,
       'lat': 48.1006704,
       'lon': 11.6252055,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'italian',
        'name': 'ROMA',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 301989132,
       'lat': 50.6079691,
       'lon': 10.4915015,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10c',
        'name': 'Zum Schwan'}},
      {'type': 'node',
       'id': 302114506,
       'lat': 47.8833037,
       'lon': 7.7312157,
       'tags': {'amenity': 'biergarten',
        'name': 'Weinbrunnen',
        'opening_hours': 'Mo-Fr 14:00-22:00; Sa,Su 11:00-22:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 302720319,
       'lat': 49.3708436,
       'lon': 8.653805,
       'tags': {'amenity': 'biergarten', 'name': 'Kleintierzüchterverein'}},
      {'type': 'node',
       'id': 302740823,
       'lat': 49.6814638,
       'lon': 10.8827025,
       'tags': {'amenity': 'biergarten', 'name': 'Felsenkeller Löwenbräu'}},
      {'type': 'node',
       'id': 302920720,
       'lat': 49.5213801,
       'lon': 11.8086677,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10d',
        'name': "beim Peter'n"}},
      {'type': 'node',
       'id': 302953838,
       'lat': 52.5715768,
       'lon': 13.1228576,
       'tags': {'amenity': 'biergarten',
        'name': 'Seeterrasse',
        'opening_hours': 'Mo-Su,PH 11:00-23:00',
        'operator': 'Ristorante Eis-Emporio',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 302957946,
       'lat': 49.7160826,
       'lon': 10.9449853,
       'tags': {'amenity': 'biergarten',
        'brewery': 'yes',
        'name': 'Waldkeller Utz',
        'opening_hours': 'May-Sep Su 11:00-22:00; May-Sep We-Fr 16:00-22:00; May-Sep PH 11:00-22:00; ',
        'phone': '+49 9195 / 7360',
        'tourism': 'attraction',
        'website': 'http://landgasthaus-utz.de/?page_id=29'}},
      {'type': 'node',
       'id': 303308352,
       'lat': 51.5324834,
       'lon': 7.6876616,
       'tags': {'amenity': 'biergarten',
        'name': 'Meisterhaus',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 303704092,
       'lat': 48.6308744,
       'lon': 9.4153248,
       'tags': {'amenity': 'biergarten',
        'email': 'reinerstradi@gmx.de',
        'name': 'Bürgerseen',
        'phone': '+49 7021 52310',
        'website': 'http://www.buergerseen.de'}},
      {'type': 'node',
       'id': 303913462,
       'lat': 51.3257533,
       'lon': 12.4538717,
       'tags': {'amenity': 'biergarten',
        'name': 'Zweinaundorf',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 304169949,
       'lat': 48.2653646,
       'lon': 8.2021756,
       'tags': {'amenity': 'biergarten', 'name': 'Rodelbahn'}},
      {'type': 'node',
       'id': 304257397,
       'lat': 47.9565329,
       'lon': 7.823153,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 304421364,
       'lat': 51.6383509,
       'lon': 12.3304445,
       'tags': {'amenity': 'biergarten', 'name': 'Goldene Aue'}},
      {'type': 'node',
       'id': 304440146,
       'lat': 49.665036,
       'lon': 10.0630939,
       'tags': {'amenity': 'biergarten', 'name': 'Gartenwirtschaft'}},
      {'type': 'node',
       'id': 304548108,
       'lat': 49.7894901,
       'lon': 11.0107626,
       'tags': {'amenity': 'biergarten',
        'name': 'Baggersee',
        'opening_hours': 'off'}},
      {'type': 'node',
       'id': 304595092,
       'lat': 50.4115225,
       'lon': 7.4655157,
       'tags': {'amenity': 'biergarten', 'name': 'Taj Mahal'}},
      {'type': 'node',
       'id': 304809450,
       'lat': 50.1248467,
       'lon': 10.8201826,
       'tags': {'amenity': 'biergarten',
        'name': 'Schloss Gereuth',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 305005691,
       'lat': 47.9140968,
       'lon': 11.2883191,
       'tags': {'addr:city': 'Tutzing',
        'addr:housenumber': '3',
        'addr:postcode': '82327',
        'addr:street': 'Midgardstraße',
        'amenity': 'biergarten',
        'name': 'Tutzinger Biergarten',
        'phone': '+49 8158 1216',
        'website': 'http://www.haering-wirtschaft.de/newpages/biergarten.htm',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 305187392,
       'lat': 50.0332509,
       'lon': 12.0105627,
       'tags': {'amenity': 'biergarten', 'name': 'Katharinenbergterrasse'}},
      {'type': 'node',
       'id': 305233756,
       'lat': 49.6714616,
       'lon': 10.1428049,
       'tags': {'amenity': 'biergarten', 'name': 'Weingut Kreglinger'}},
      {'type': 'node',
       'id': 305258385,
       'lat': 48.1025964,
       'lon': 11.5956025,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '71',
        'addr:postcode': '81549',
        'addr:street': 'Stadelheimer Straße',
        'amenity': 'biergarten',
        'name': "St. Benno's Einkehr",
        'opening_hours': 'Mo-Su 10:00-23:00',
        'phone': '+49 89 6900855',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 305472470,
       'lat': 48.5685694,
       'lon': 8.1619758,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Sternen'}},
      {'type': 'node',
       'id': 305786594,
       'lat': 47.3342605,
       'lon': 10.2685438,
       'tags': {'amenity': 'biergarten',
        'operator': 'Adler-Landhaus Birgsau',
        'source': 'survey',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 305787248,
       'lat': 47.4053682,
       'lon': 10.2770336,
       'tags': {'amenity': 'biergarten',
        'name': 'Königliches Jagdhaus',
        'source': 'survey',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 306004576,
       'lat': 49.4520631,
       'lon': 8.6774553,
       'tags': {'amenity': 'biergarten',
        'email': 'besen.info@dossema-weinhof.de',
        'name': 'Besenwirtschaft Dossema Weinhof',
        'opening_hours': 'We-Sa 16:00-23:00; Su 11:00-21:00',
        'phone': '+49 6221 7257617',
        'website': 'http://www.dossema-weinhof.de/'}},
      {'type': 'node',
       'id': 306080338,
       'lat': 49.6575162,
       'lon': 10.3003597,
       'tags': {'amenity': 'biergarten',
        'name': 'Nierenmühle',
        'opening_hours': 'Sa-Su 15:00+'}},
      {'type': 'node',
       'id': 306190786,
       'lat': 47.7635567,
       'lon': 8.8167386,
       'tags': {'amenity': 'biergarten', 'description': 'Kiosk'}},
      {'type': 'node',
       'id': 306213182,
       'lat': 47.9752787,
       'lon': 9.9287905,
       'tags': {'amenity': 'biergarten', 'name': 'Sonnenstüble'}},
      {'type': 'node',
       'id': 306304817,
       'lat': 47.7152703,
       'lon': 8.9639405,
       'tags': {'amenity': 'biergarten', 'name': 'Strandbad Iznang'}},
      {'type': 'node',
       'id': 307638858,
       'lat': 48.1644506,
       'lon': 9.8172252,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 307757466,
       'lat': 48.213588,
       'lon': 11.5289585,
       'tags': {'amenity': 'biergarten', 'name': 'Croatia Grill'}},
      {'type': 'node',
       'id': 307795022,
       'lat': 51.0010198,
       'lon': 13.8707229,
       'tags': {'amenity': 'biergarten', 'created_by': 'Potlatch 0.10e'}},
      {'type': 'node',
       'id': 308427374,
       'lat': 48.5361757,
       'lon': 12.1494879,
       'tags': {'addr:city': 'Landshut',
        'addr:country': 'DE',
        'addr:housenumber': '3',
        'addr:postcode': '84028',
        'addr:street': 'Isarpromenade',
        'amenity': 'biergarten',
        'check_date': '2016-04-02',
        'name': 'Alt Landshut',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 308723517,
       'lat': 50.068333,
       'lon': 8.2100368,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'german',
        'food': 'yes',
        'name': 'Straßenmühle',
        'phone': '+49 611 4508774'}},
      {'type': 'node',
       'id': 308739800,
       'lat': 51.3653534,
       'lon': 8.4357922,
       'tags': {'addr:city': 'Bestwig',
        'addr:country': 'DE',
        'addr:housenumber': '54',
        'addr:postcode': '59909',
        'addr:street': 'Briloner Straße',
        'amenity': 'biergarten',
        'name': 'Hester',
        'phone': '+49 2904 2324',
        'website': 'http://www.hester-nuttlar.de/'}},
      {'type': 'node',
       'id': 309188722,
       'lat': 49.1324222,
       'lon': 9.2667409,
       'tags': {'amenity': 'biergarten', 'name': 'Jägerhaus'}},
      {'type': 'node',
       'id': 309196446,
       'lat': 47.9364184,
       'lon': 9.7450733,
       'tags': {'amenity': 'biergarten', 'name': 'Mostbauer'}},
      {'type': 'node',
       'id': 309533161,
       'lat': 49.6308693,
       'lon': 11.3570004,
       'tags': {'amenity': 'biergarten', 'smoking': 'yes'}},
      {'type': 'node',
       'id': 309751897,
       'lat': 49.045378,
       'lon': 11.3526669,
       'tags': {'amenity': 'biergarten',
        'name': 'Hotel am Markt',
        'smoking': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 309841167,
       'lat': 52.1480523,
       'lon': 7.3393236,
       'tags': {'amenity': 'biergarten',
        'name': 'Biercafe Niveau',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 309889532,
       'lat': 48.2978637,
       'lon': 11.623836,
       'tags': {'amenity': 'biergarten', 'name': 'Alter Wirt'}},
      {'type': 'node',
       'id': 310349136,
       'lat': 48.3457933,
       'lon': 12.1323863,
       'tags': {'amenity': 'biergarten',
        'email': 'jell@freenet.de',
        'name': 'Biergarten Taufkirchen',
        'website': 'http://biergarten-taufkirchen.de'}},
      {'type': 'node',
       'id': 310362443,
       'lat': 52.2644918,
       'lon': 10.5615453,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 311078282,
       'lat': 47.6197866,
       'lon': 7.7703226,
       'tags': {'amenity': 'biergarten',
        'name': 'Dinkelberger Biergärdle Adelhausen'}},
      {'type': 'node',
       'id': 311194119,
       'lat': 49.976359,
       'lon': 8.0304925,
       'tags': {'amenity': 'biergarten', 'name': 'Westend-Oase'}},
      {'type': 'node',
       'id': 311338991,
       'lat': 52.3696025,
       'lon': 12.9333609,
       'tags': {'amenity': 'biergarten',
        'name': 'Weintiene',
        'shop': 'wine',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 311364372,
       'lat': 49.9851776,
       'lon': 10.9659561,
       'tags': {'amenity': 'biergarten',
        'contact:website': 'http://www.helmutshofschaenke.de',
        'name': "Helmut's Hofschänke"}},
      {'type': 'node',
       'id': 312109322,
       'lat': 49.7752704,
       'lon': 9.9285224,
       'tags': {'addr:city': 'Würzburg',
        'addr:housenumber': '19',
        'addr:postcode': '97082',
        'addr:street': 'Mergentheimer Straße',
        'amenity': 'biergarten',
        'brewery': 'yes;Würzburger_Hofbräu;Keiler_Hefe-Weißbier;Mönchshof_Zwickl',
        'email': 'info@zollhaus-wuerzburg.de',
        'name': 'Zollhaus',
        'opening_hours': 'Mo-So: 11:00-24:00',
        'outdoor_seating': 'yes',
        'phone': '+49 931 78 12 23',
        'website': 'http://www.zollhaus-wuerzburg.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 312660753,
       'lat': 49.7293644,
       'lon': 10.9122873,
       'tags': {'amenity': 'biergarten',
        'name': 'Laufer Keller',
        'tourism': 'attraction'}},
      {'type': 'node',
       'id': 312859181,
       'lat': 48.3769338,
       'lon': 10.8889464,
       'tags': {'amenity': 'biergarten', 'name': 'Freibank', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 312929579,
       'lat': 49.8011034,
       'lon': 9.9512732,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Loisl'}},
      {'type': 'node',
       'id': 313072201,
       'lat': 53.0225525,
       'lon': 9.8801098,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Rafting'}},
      {'type': 'node',
       'id': 313283461,
       'lat': 49.6165366,
       'lon': 10.747152,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 313738693,
       'lat': 50.6820257,
       'lon': 8.684547,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Salzbödetal'}},
      {'type': 'node',
       'id': 313793542,
       'lat': 48.5111315,
       'lon': 11.4988488,
       'tags': {'amenity': 'biergarten', 'name': 'Waldspielplatz'}},
      {'type': 'node',
       'id': 314605242,
       'lat': 53.8608047,
       'lon': 10.6904003,
       'tags': {'addr:city': 'Lübeck',
        'addr:postcode': '23552',
        'addr:street': 'Mühlenbrücke',
        'amenity': 'biergarten',
        'name': 'Stadthalle',
        'source:addr': 'interpolation'}},
      {'type': 'node',
       'id': 315089198,
       'lat': 51.2709499,
       'lon': 8.8754464,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthaus Am Dalwigker Tor',
        'operator': 'Manfred Meier',
        'phone': '+49 5631 62915',
        'tourism': 'guest_house',
        'website': 'http://www.amdalwigkertor-meier.de'}},
      {'type': 'node',
       'id': 315140514,
       'lat': 52.0284504,
       'lon': 8.5227015,
       'tags': {'amenity': 'biergarten',
        'name': 'Bürgerwache',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 315275437,
       'lat': 51.3446414,
       'lon': 7.1930759,
       'tags': {'addr:city': 'Hattingen',
        'addr:country': 'DE',
        'addr:housenumber': '8',
        'addr:postcode': '45527',
        'addr:street': 'Berger Weg',
        'amenity': 'biergarten',
        'email': 'info@bergerhof.de',
        'name': 'Bergerhof',
        'opening_hours': 'Mo-Su 09:00-18:00',
        'payment:cash': 'yes',
        'phone': '+49 2324 72478',
        'website': 'http://www.bergerhof.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 315541825,
       'lat': 49.9275439,
       'lon': 9.2218085,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'german',
        'name': 'Cafe Duckdich',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 315773660,
       'lat': 51.4409481,
       'lon': 7.046531,
       'tags': {'amenity': 'biergarten', 'name': 'Im Grünen'}},
      {'type': 'node',
       'id': 315773931,
       'lat': 51.4381317,
       'lon': 7.0484875,
       'tags': {'amenity': 'biergarten', 'name': 'Gute Erholung'}},
      {'type': 'node',
       'id': 315849734,
       'lat': 50.9602923,
       'lon': 7.1446856,
       'tags': {'amenity': 'biergarten',
        'name': 'Klausmann',
        'outdoor_seating': 'yes'}},
      {'type': 'node',
       'id': 315907255,
       'lat': 48.2729332,
       'lon': 11.450604,
       'tags': {'addr:city': 'Dachau',
        'addr:country': 'DE',
        'addr:housenumber': '31',
        'addr:postcode': '85221',
        'addr:street': 'Roßwachtstraße',
        'amenity': 'biergarten',
        'name': 'La Bodega'}},
      {'type': 'node',
       'id': 316192414,
       'lat': 50.1439107,
       'lon': 8.6492703,
       'tags': {'addr:city': 'Frankfurt am Main',
        'addr:country': 'DE',
        'addr:housenumber': '2a',
        'addr:postcode': '60431',
        'addr:street': 'Ginnheimer Hohl',
        'addr:suburb': 'Ginnheim',
        'amenity': 'biergarten',
        'contact:fax': '+49 69 510908',
        'contact:phone': '+49 69 520981',
        'contact:website': 'http://www.zumadler.net/',
        'name': 'Zum Adler',
        'opening_hours': '11:30-00:30',
        'source': 'http://www.zumadler.net/',
        'source:date': '2017-07-17',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 316522415,
       'lat': 49.2291704,
       'lon': 7.1118416,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 316730082,
       'lat': 49.8082253,
       'lon': 9.9470264,
       'tags': {'amenity': 'biergarten', 'name': 'TSV Grombühl'}},
      {'type': 'node',
       'id': 317301710,
       'lat': 51.9863668,
       'lon': 13.0681157,
       'tags': {'amenity': 'biergarten', 'name': 'Damm 119'}},
      {'type': 'node',
       'id': 318076765,
       'lat': 51.4872077,
       'lon': 11.961322,
       'tags': {'addr:city': 'Halle (Saale)',
        'addr:country': 'DE',
        'addr:housenumber': '14',
        'addr:postcode': '06108',
        'addr:street': 'Jägerplatz',
        'amenity': 'biergarten',
        'brewery': 'various',
        'name': 'Fritzengarten',
        'opening_hours': 'Mo-Sa 15:00+; Su,PH 14:00+',
        'outdoor_seating': 'yes',
        'phone': '+49 163 8485243',
        'smoking': 'outside',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 318625586,
       'lat': 48.0981207,
       'lon': 11.5804329,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:street': 'Naupliastraße',
        'amenity': 'biergarten',
        'name': 'Gaststätte Gartenstadt Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 318665876,
       'lat': 48.7114808,
       'lon': 9.4611544,
       'tags': {'amenity': 'biergarten',
        'ele': '268',
        'name': 'Biergarten Hotel Gasthaus zum Bock',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 319820911,
       'lat': 49.0079451,
       'lon': 12.0270058,
       'tags': {'addr:city': 'Sinzing',
        'addr:housenumber': '17',
        'addr:postcode': '93161',
        'addr:street': 'Mariaorter Straße',
        'amenity': 'biergarten',
        'contact:email': 'info@haubner-sinzing.de',
        'contact:facebook': 'https://www.facebook.com/haubnersinzing',
        'contact:phone': '+49 941 31207',
        'contact:website': 'http://www.haubner-sinzing.de/',
        'name': 'Gasthaus Haubner',
        'opening_hours': 'We-Fr 16:00-22:00; Sa-Su 11:00-22:00; Mo,Tu off',
        'source': 'http://www.haubner-sinzing.de/',
        'source:date': '2016-06-17'}},
      {'type': 'node',
       'id': 320347606,
       'lat': 51.9910825,
       'lon': 13.0812327,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Schmied',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 320347609,
       'lat': 51.9947973,
       'lon': 13.088774,
       'tags': {'amenity': 'biergarten', 'name': 'Fränkis Tanzbar'}},
      {'type': 'node',
       'id': 320347770,
       'lat': 51.9907186,
       'lon': 13.0805247,
       'tags': {'amenity': 'biergarten', 'name': 'Lodderleben'}},
      {'type': 'node',
       'id': 320353295,
       'lat': 52.0027681,
       'lon': 13.0859167,
       'tags': {'amenity': 'biergarten', 'name': 'Bergschlößchen'}},
      {'type': 'node',
       'id': 320467815,
       'lat': 51.475355,
       'lon': 6.8472339,
       'tags': {'amenity': 'biergarten', 'created_by': 'Potlatch 0.10f'}},
      {'type': 'node',
       'id': 320926577,
       'lat': 48.1538366,
       'lon': 11.6905108,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthaus Butz',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 321484510,
       'lat': 51.5614004,
       'lon': 13.0041372,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 321680664,
       'lat': 49.509915,
       'lon': 8.1792576,
       'tags': {'amenity': 'biergarten', 'name': 'Beckers Woistub'}},
      {'type': 'node',
       'id': 321749685,
       'lat': 52.3597322,
       'lon': 9.253893,
       'tags': {'amenity': 'biergarten', 'operator': 'Zum Dicken Heinrich'}},
      {'type': 'node',
       'id': 321774816,
       'lat': 49.5750125,
       'lon': 6.5752608,
       'tags': {'amenity': 'biergarten', 'name': '"Unter den Kastanien"'}},
      {'type': 'node',
       'id': 322079623,
       'lat': 49.3859139,
       'lon': 8.5221032,
       'tags': {'amenity': 'biergarten',
        'name': 'Grillhütte Brühl',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 322176802,
       'lat': 48.8465339,
       'lon': 8.5880311,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthaus Krone'}},
      {'type': 'node',
       'id': 322661449,
       'lat': 51.7905086,
       'lon': 11.7452888,
       'tags': {'amenity': 'biergarten', 'created_by': 'Potlatch 0.10f'}},
      {'type': 'node',
       'id': 323029777,
       'lat': 51.1670095,
       'lon': 7.0855351,
       'tags': {'amenity': 'biergarten',
        'name': 'Birkenweiher',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 323087989,
       'lat': 47.9106175,
       'lon': 7.7103312,
       'tags': {'amenity': 'biergarten',
        'email': 'cafe-z@t-online.de',
        'name': 'Café Z',
        'opening_hours': 'Mo-Su 09:00-24:00',
        'phone': '+49 7633 16790',
        'website': 'http://www.cafe-z.de/',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 323148183,
       'lat': 48.1223489,
       'lon': 9.8612164,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Witzles'}},
      {'type': 'node',
       'id': 323755812,
       'lat': 48.2112809,
       'lon': 10.9657527,
       'tags': {'addr:city': 'Schmiechen',
        'addr:country': 'DE',
        'addr:housenumber': '7',
        'addr:postcode': '86511',
        'addr:street': 'Eglinger Straße',
        'amenity': 'biergarten',
        'name': 'Haloisius',
        'opening_hours': 'closed',
        'website': 'http://www.haloisius-wirtsgarten.de/'}},
      {'type': 'node',
       'id': 323892546,
       'lat': 48.7993467,
       'lon': 8.6303125,
       'tags': {'addr:city': 'Schömberg',
        'addr:housenumber': '31',
        'addr:postcode': '75328',
        'addr:street': 'Höfener Straße',
        'amenity': 'biergarten',
        'name': 'Gasthof Grüner Baum',
        'tourism': 'guest_house'}},
      {'type': 'node',
       'id': 324289834,
       'lat': 47.6801049,
       'lon': 9.8186871,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 324354207,
       'lat': 50.6713717,
       'lon': 8.7890059,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 324404117,
       'lat': 50.9963429,
       'lon': 7.0359251,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 325139230,
       'lat': 49.9320591,
       'lon': 10.8306211,
       'tags': {'amenity': 'biergarten', 'name': 'Hannla-Keller'}},
      {'type': 'node',
       'id': 327063324,
       'lat': 48.6188584,
       'lon': 9.8385379,
       'tags': {'amenity': 'biergarten',
        'contact:email': 'biergarten10@aol.com',
        'contact:phone': '+49 7331 441135',
        'contact:website': 'http://www.geislinger-biergarten.de',
        'name': 'Stadtpark',
        'opening_hours': '11:00-23:00',
        'wheelchair': 'yes',
        'wheelchair:description': 'Rollstuhltoilette befindet sich in der Jahnhalle, mit Euroschlüssel!'}},
      {'type': 'node',
       'id': 327063333,
       'lat': 48.6249603,
       'lon': 9.8194701,
       'tags': {'amenity': 'biergarten',
        'name': 'Altenstädter Biergarten - Unter den Linden',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 329125325,
       'lat': 48.1318759,
       'lon': 11.5437129,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Augustiner Bräu München',
        'contact:email': 'info@wirtshaus-am-bavariapark.de',
        'contact:fax': '089/45211692',
        'contact:phone': '089/45211695',
        'contact:website': 'http://www.wirtshaus-am-bavariapark.com/',
        'cuisine': 'regional',
        'name': 'Wirtshaus am Bavariapark',
        'opening_hours': 'Mo-Su 11:00-23:00',
        'wheelchair': 'yes',
        'wheelchair:description': 'Toilette ist im Keller'}},
      {'type': 'node',
       'id': 329238199,
       'lat': 53.1194651,
       'lon': 9.7861251,
       'tags': {'addr:city': 'Schneverdingen',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '29640',
        'addr:street': 'Marktstraße',
        'amenity': 'biergarten',
        'name': 'Biergarten',
        'source': 'survey',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 330779126,
       'lat': 47.5358612,
       'lon': 10.0396404,
       'tags': {'amenity': 'biergarten', 'name': 'Seppls Gartenwirtschaft'}},
      {'type': 'node',
       'id': 331233859,
       'lat': 48.0692881,
       'lon': 11.1843615,
       'tags': {'amenity': 'biergarten',
        'name': 'Kiosk Roßschwemme',
        'wheelchair': 'limited',
        'wheelchair:description': 'Kiosk barrierefrei erreichbar, Toiletten haben 1 Stufe (ca. 7cm) und sind schmal und lang, Tür geht nach aussen auf. Mit einem schmalen Rolltuhl (<58cm) kommt man rein. Der Badeplatz ist ausserdem sehr schön und an einigen Stellen einigermaßen flach.'}},
      {'type': 'node',
       'id': 331238095,
       'lat': 48.1303749,
       'lon': 11.8335278,
       'tags': {'addr:city': 'Vaterstetten',
        'addr:housenumber': '20',
        'addr:postcode': '85646',
        'addr:street': 'Neufarner Straße',
        'addr:suburb': 'Purfing',
        'amenity': 'biergarten',
        'name': 'Purfinger Haberer',
        'opening_hours': 'Tu-Fr 17:00-22:00, Sa-Su 11:30-22:00',
        'phone': '+49 08106 29743',
        'website': 'https://www.purfinger-haberer.bayern'}},
      {'type': 'node',
       'id': 331276903,
       'lat': 48.9747764,
       'lon': 8.9594037,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 331512781,
       'lat': 48.1921681,
       'lon': 11.6744256,
       'tags': {'addr:city': 'Unterföhring',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '85774',
        'addr:street': 'Am Feringasee',
        'amenity': 'biergarten',
        'name': 'Gasthof Feringasee',
        'opening_hours': 'Mo-Su,PH 10:00-21:30',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 331650338,
       'lat': 50.0967635,
       'lon': 8.1694548,
       'tags': {'amenity': 'biergarten',
        'name': 'Chausseehaus',
        'website': 'http://www.restaurant-chausseehaus.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 332077844,
       'lat': 50.6370203,
       'lon': 7.0926755,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Görres'}},
      {'type': 'node',
       'id': 332119173,
       'lat': 49.435289,
       'lon': 11.116795,
       'tags': {'amenity': 'biergarten',
        'name': 'Gutmann am Dutzendteich',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 332240620,
       'lat': 52.1091395,
       'lon': 13.7625929,
       'tags': {'amenity': 'biergarten', 'name': 'Marktwirtschaft'}},
      {'type': 'node',
       'id': 332567020,
       'lat': 52.1676423,
       'lon': 9.0345547,
       'tags': {'addr:city': 'Rinteln',
        'addr:housenumber': '1',
        'addr:postcode': '31737',
        'addr:street': 'Am Kloster',
        'amenity': 'biergarten',
        'email': 'info@domaene-moellenbeck.de',
        'name': 'Hofgarten',
        'opening_hours:url': 'http://www.domaene-moellenbeck.de/hofgarten/oeffnungszeiten.htm',
        'outdoor_seating': 'yes',
        'phone': '+49 5751 965401',
        'smoking': 'outside',
        'website': 'http://www.domaene-moellenbeck.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 332618689,
       'lat': 49.7461038,
       'lon': 7.2691374,
       'tags': {'addr:city': 'Idar-Oberstein',
        'addr:postcode': '55743',
        'amenity': 'biergarten',
        'name': 'Gaststätte Peffelberg'}},
      {'type': 'node',
       'id': 333126077,
       'lat': 48.7278524,
       'lon': 12.4518408,
       'tags': {'addr:city': 'Mengkofen',
        'addr:country': 'DE',
        'addr:housenumber': '3',
        'addr:postcode': '84152',
        'addr:street': 'Ettenkofen',
        'amenity': 'biergarten',
        'name': 'Gasthof "zum Sepp"',
        'phone': '+49 8733 336'}},
      {'type': 'node',
       'id': 333775239,
       'lat': 47.6833824,
       'lon': 9.2026241,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 334367327,
       'lat': 51.443496,
       'lon': 7.0157269,
       'tags': {'addr:city': 'Essen',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '45128',
        'addr:street': 'Beethovenstraße',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Cafe Click',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 337546532,
       'lat': 51.9873112,
       'lon': 9.2457787,
       'tags': {'amenity': 'biergarten', 'name': 'Bahn 19'}},
      {'type': 'node',
       'id': 338348481,
       'lat': 50.1265109,
       'lon': 8.6835258,
       'tags': {'amenity': 'biergarten',
        'name': 'Stalburg',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 338390445,
       'lat': 49.2199811,
       'lon': 8.3870583,
       'tags': {'amenity': 'biergarten',
        'name': 'Tropic Beach Island Strandbar',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 339954392,
       'lat': 50.9046676,
       'lon': 14.0812963,
       'tags': {'addr:city': 'Königstein',
        'addr:country': 'DE',
        'addr:housenumber': '5',
        'addr:postcode': '01824',
        'addr:street': 'Pfaffensteinweg',
        'addr:suburb': 'Pfaffenstein',
        'amenity': 'biergarten',
        'name': 'Barbarinenhof'}},
      {'type': 'node',
       'id': 340112872,
       'lat': 48.1612764,
       'lon': 7.7936087,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 340459206,
       'lat': 49.0937585,
       'lon': 13.2477219,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 342793553,
       'lat': 51.0014733,
       'lon': 6.9914679,
       'tags': {'amenity': 'biergarten', 'created_by': 'Potlatch 0.10f'}},
      {'type': 'node',
       'id': 343096349,
       'lat': 48.2085858,
       'lon': 11.5717969,
       'tags': {'amenity': 'biergarten', 'name': 'Paulanergarten'}},
      {'type': 'node',
       'id': 343318414,
       'lat': 51.5585516,
       'lon': 13.0094829,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 343735120,
       'lat': 48.1352755,
       'lon': 11.5764257,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '9',
        'addr:postcode': '80331',
        'addr:street': 'Viktualienmarkt',
        'amenity': 'biergarten',
        'brewery': 'various',
        'capacity': '1100',
        'contact:phone': '+49 89 297545',
        'name': 'Viktualienmarkt',
        'opening_hours': 'Mo-Sa 09:00-22:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 344900423,
       'lat': 50.006529,
       'lon': 8.270206,
       'tags': {'addr:city': 'Mainz',
        'addr:country': 'DE',
        'addr:postcode': '55116',
        'addr:street': 'Peter-Altmeier-Allee',
        'amenity': 'biergarten',
        'email': 'info@eulchen-bier.de',
        'internet_access': 'wlan',
        'internet_access:fee': 'no',
        'microbrewery': 'yes',
        'name': 'Eulchen Schlossbiergarten',
        'opening_hours': 'Mo-Sa 16:00-23:00; Su 14:00-21:00',
        'phone': '+49 6131 4987097',
        'website': 'http://www.eulchen-bier.de/'}},
      {'type': 'node',
       'id': 344945294,
       'lat': 48.3617523,
       'lon': 11.581496,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthaus Weng'}},
      {'type': 'node',
       'id': 345234560,
       'lat': 48.8156959,
       'lon': 8.9034098,
       'tags': {'addr:housenumber': '64',
        'addr:street': 'Hauptstraße',
        'amenity': 'biergarten',
        'name': 'Waldschenke',
        'opening_hours': 'Mo-Fr 15:00-18:00+; Sa 14:00-18:00+; Su 12:00-18:00+'}},
      {'type': 'node',
       'id': 346161343,
       'lat': 49.331195,
       'lon': 12.1057376,
       'tags': {'amenity': 'biergarten', 'name': 'Stadtpark'}},
      {'type': 'node',
       'id': 347531663,
       'lat': 51.6986587,
       'lon': 7.8470195,
       'tags': {'amenity': 'biergarten',
        'name': 'Bei J. Jochum',
        'shop': 'kiosk',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 349102590,
       'lat': 50.0755401,
       'lon': 8.2331024,
       'tags': {'amenity': 'biergarten',
        'name': 'Störtebeker',
        'opening_hours': 'Mo-Sa 19:00+',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 350449666,
       'lat': 49.2200601,
       'lon': 7.1671577,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 351876983,
       'lat': 49.958452,
       'lon': 10.9568733,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Brauerei Wagner'}},
      {'type': 'node',
       'id': 352601158,
       'lat': 48.7108348,
       'lon': 9.2038072,
       'tags': {'amenity': 'biergarten',
        'beer_garden': 'yes',
        'name': 'Biergarten Wirtshaus Garbe',
        'opening_hours': 'Tu-Fr 12:00-14:30,17:30-23:00; Sa,Su 12:00-23:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 352740418,
       'lat': 49.9600237,
       'lon': 10.9561313,
       'tags': {'amenity': 'biergarten', 'name': 'Hummelskeller'}},
      {'type': 'node',
       'id': 354436758,
       'lat': 48.1739339,
       'lon': 11.5510934,
       'tags': {'amenity': 'biergarten',
        'name': 'Olympia Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 354619176,
       'lat': 48.5184996,
       'lon': 10.8107289,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Magg',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 354936843,
       'lat': 52.3620033,
       'lon': 13.0227683,
       'tags': {'amenity': 'biergarten',
        'name': 'Bootsvermietung Moisl & Strandbar „Skihütte“',
        'sport': 'canoe',
        'website': 'http://bootsvermietung-moisl.de/'}},
      {'type': 'node',
       'id': 355937832,
       'lat': 47.9134943,
       'lon': 11.4200455,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 356518768,
       'lat': 53.0915788,
       'lon': 8.8126028,
       'tags': {'amenity': 'biergarten',
        'contact:website': 'http://www.portpiet.de/',
        'name': 'Port Piet',
        'opening_hours': 'Apr-Sep: Su-Th 11:00-22:00; Fr 11:00-23:00; Sa 10:00-23:00; "Bei schlechtem Wetter geschlossen"',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes',
        'wheelchair:description': 'Öffentliches Rolli-WC! Leider trotz mehrfacher Bitte nicht mit Euro-Schloß, sondern mit anderem Schloß versehen, sodass man den Schlüssel nur erbitten kann, wenn der Biergarten offen ist. Rampe zum Biergarten etwas steiler, Zugang zum Tresen über 2 Stufen'}},
      {'type': 'node',
       'id': 356950630,
       'lat': 52.0751041,
       'lon': 13.1688803,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Elsthal',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 357433560,
       'lat': 47.6924945,
       'lon': 9.6567947,
       'tags': {'amenity': 'biergarten', 'name': 'Hofer'}},
      {'type': 'node',
       'id': 358158892,
       'lat': 51.9198786,
       'lon': 7.9669095,
       'tags': {'amenity': 'biergarten',
        'name': 'Stiftshof Dühlmann',
        'operator': 'Famile Dühlmann',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 358347842,
       'lat': 51.3492998,
       'lon': 12.3672441,
       'tags': {'amenity': 'biergarten',
        'name': 'Café Hacienda am Rosental',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 358452147,
       'lat': 51.3635093,
       'lon': 12.3736706,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10f',
        'name': 'Biergarten mit Ginkobaum',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 359525385,
       'lat': 50.3917104,
       'lon': 8.1920522,
       'tags': {'amenity': 'biergarten', 'created_by': 'Merkaartor 0.13'}},
      {'type': 'node',
       'id': 360001471,
       'lat': 48.7192802,
       'lon': 9.5845833,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 360482716,
       'lat': 49.7051383,
       'lon': 10.2598618,
       'tags': {'amenity': 'biergarten', 'name': 'Weinbau E. Neubert'}},
      {'type': 'node',
       'id': 360482882,
       'lat': 49.707929,
       'lon': 10.2595193,
       'tags': {'amenity': 'biergarten', 'name': 'Weinbau Dorsch'}},
      {'type': 'node',
       'id': 360636601,
       'lat': 50.2290387,
       'lon': 8.6109733,
       'tags': {'addr:city': 'Bad Homburg v.d. Höhe',
        'addr:country': 'DE',
        'addr:housenumber': '13',
        'addr:postcode': '61348',
        'addr:street': 'Schulberg',
        'amenity': 'biergarten',
        'email': 'info@cafe-eiding.de',
        'fax': '+49 6172 22857',
        'name': 'Zur Reblaus',
        'note': 'Gehört zum Cafe Eiding',
        'opening_hours': 'Mo 10:00-18:00; Tu-Su 08:30-18:00',
        'operator': 'Café Conditorei Eiding GmbH',
        'phone': '+49 6172 22855'}},
      {'type': 'node',
       'id': 360653817,
       'lat': 50.9452836,
       'lon': 12.7623983,
       'tags': {'amenity': 'biergarten', 'name': 'Manhatten Ost'}},
      {'type': 'node',
       'id': 360669788,
       'lat': 50.9320132,
       'lon': 12.7339002,
       'tags': {'amenity': 'biergarten',
        'contact:phone': '+49 37381 649031',
        'name': 'Amerikas Biergarten',
        'note': 'geschlossen',
        'operator': 'Hermann Richter'}},
      {'type': 'node',
       'id': 361199267,
       'lat': 47.9881948,
       'lon': 12.7477655,
       'tags': {'amenity': 'biergarten', 'leisure': 'playground'}},
      {'type': 'node',
       'id': 362235517,
       'lat': 52.2656133,
       'lon': 10.5519197,
       'tags': {'amenity': 'biergarten',
        'name': 'Löwen-Garten',
        'phone': '+49 151 / 58 83 98 95',
        'website': 'https://loewengarten.com/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 363609060,
       'lat': 49.7740788,
       'lon': 9.9273142,
       'tags': {'amenity': 'biergarten', 'name': 'Postkutscherl'}},
      {'type': 'node',
       'id': 364099686,
       'lat': 48.1361144,
       'lon': 11.4629409,
       'tags': {'amenity': 'biergarten', 'name': 'Franzz', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 364124961,
       'lat': 49.8757106,
       'lon': 10.163911,
       'tags': {'addr:city': 'Volkach - Fahr',
        'addr:housenumber': '2',
        'addr:postcode': '97332',
        'addr:street': 'Maingasse',
        'amenity': 'biergarten',
        'name': 'Zur Mainfähre',
        'phone': '+49 9381 3385',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 364174350,
       'lat': 50.8564036,
       'lon': 7.083632,
       'tags': {'amenity': 'biergarten',
        'name': 'Eltzhof',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 364615005,
       'lat': 50.1386036,
       'lon': 8.9183397,
       'tags': {'amenity': 'biergarten',
        'name': 'Paulanergarten Holle',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 364706558,
       'lat': 51.4922877,
       'lon': 6.8774791,
       'tags': {'amenity': 'biergarten',
        'name': "Ärwin's Biergarten",
        'outdoor_seating': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 364719902,
       'lat': 50.0387908,
       'lon': 11.2081968,
       'tags': {'amenity': 'biergarten',
        'name': 'Schrepfersmühle',
        'note': 'Dienstag Ruhetag, im Biergarten kann mitgebrachte Brotzeit gegessen werden',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 364735591,
       'lat': 48.327957,
       'lon': 10.153947,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 364749746,
       'lat': 49.1746744,
       'lon': 8.8301669,
       'tags': {'amenity': 'biergarten', 'name': 'Seekiosk'}},
      {'type': 'node',
       'id': 364889264,
       'lat': 49.3235535,
       'lon': 11.0791988,
       'tags': {'amenity': 'biergarten',
        'name': 'Döllinger',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 365287770,
       'lat': 48.6393769,
       'lon': 9.5528907,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 365951817,
       'lat': 49.9295018,
       'lon': 11.4632316,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Drei Linden',
        'note': 'Ruhetag: Dienstag',
        'phone': '+49 9279 8512'}},
      {'type': 'node',
       'id': 366005098,
       'lat': 49.693187,
       'lon': 8.4942206,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 366284430,
       'lat': 48.2843745,
       'lon': 10.4679377,
       'tags': {'addr:city': 'Thannhausen',
        'addr:country': 'DE',
        'addr:housenumber': '31',
        'addr:postcode': '86470',
        'addr:street': 'Frühmeßstraße',
        'amenity': 'biergarten',
        'name': 'Zum Pflugwirt',
        'phone': '+49 8281 4114'}},
      {'type': 'node',
       'id': 366514301,
       'lat': 50.7527813,
       'lon': 6.158488,
       'tags': {'amenity': 'biergarten', 'name': 'Brander Bahnhof'}},
      {'type': 'node',
       'id': 366542902,
       'lat': 49.8774123,
       'lon': 10.1683832,
       'tags': {'amenity': 'biergarten',
        'name': 'Weingut Borst',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 366866004,
       'lat': 49.2216914,
       'lon': 12.1749822,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 366939679,
       'lat': 48.3882701,
       'lon': 11.789155,
       'tags': {'amenity': 'biergarten',
        'created_by': 'Potlatch 0.10f',
        'name': 'Stoibermuehle',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 366965998,
       'lat': 48.7317029,
       'lon': 9.3672446,
       'tags': {'amenity': 'biergarten',
        'ele': '342',
        'name': 'Paulaner Biergarten'}},
      {'type': 'node',
       'id': 367896694,
       'lat': 50.4373243,
       'lon': 7.5993419,
       'tags': {'addr:city': 'Bendorf',
        'addr:country': 'DE',
        'addr:postcode': '56170',
        'amenity': 'biergarten',
        'name': 'Meisenhof'}},
      {'type': 'node',
       'id': 367949188,
       'lat': 51.0167541,
       'lon': 7.0065606,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 368196458,
       'lat': 47.8285492,
       'lon': 11.125437,
       'tags': {'addr:city': 'Weilheim in Oberbayern',
        'addr:country': 'DE',
        'addr:housenumber': '36',
        'addr:postcode': '82362',
        'addr:street': 'Holzhofstraße',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Weilheim',
        'opening_hours': 'Mo 17:00-24:00;Tu-Su 11:00-24:00',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'N 092',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'website': 'http://www.naturfreundehaus-weilheim.de/'}},
      {'type': 'node',
       'id': 368341436,
       'lat': 51.3841168,
       'lon': 9.439594,
       'tags': {'amenity': 'biergarten',
        'name': 'Paulaner Biergarten (ehemaliger)',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 369377186,
       'lat': 51.2357904,
       'lon': 6.8618858,
       'tags': {'addr:city': 'Düsseldorf',
        'addr:country': 'DE',
        'addr:housenumber': '17',
        'addr:postcode': '40625',
        'addr:street': 'Kölner Tor',
        'amenity': 'biergarten',
        'name': 'Zum Jägerhof',
        'sport': '9pin',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 369608111,
       'lat': 48.1231817,
       'lon': 11.5402954,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '32',
        'addr:postcode': '81373',
        'addr:street': 'Pfeuferstraße',
        'amenity': 'biergarten',
        'cuisine': 'bavarian',
        'name': 'Tannengarten',
        'phone': '+49 89 767 58 359',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 369766871,
       'lat': 49.942056,
       'lon': 11.6196976,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 369934311,
       'lat': 52.3912814,
       'lon': 13.0149252,
       'tags': {'amenity': 'biergarten', 'name': 'Krähenbusch'}},
      {'type': 'node',
       'id': 370002422,
       'lat': 47.8356101,
       'lon': 12.254138,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 370049547,
       'lat': 48.6044767,
       'lon': 10.8136811,
       'tags': {'amenity': 'biergarten', 'name': 'Kloster Gasthof Holzen'}},
      {'type': 'node',
       'id': 370110751,
       'lat': 51.580776,
       'lon': 6.8312181,
       'tags': {'amenity': 'biergarten',
        'ele': '46.5091553',
        'name': 'Whisky-Bude',
        'shop': 'kiosk'}},
      {'type': 'node',
       'id': 370275246,
       'lat': 50.9783747,
       'lon': 11.0271227,
       'tags': {'amenity': 'biergarten',
        'drink:beer': 'served',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 370286020,
       'lat': 50.936839,
       'lon': 11.012135,
       'tags': {'amenity': 'biergarten',
        'outdoor_seating': 'yes',
        'smoking': 'outside'}},
      {'type': 'node',
       'id': 370579847,
       'lat': 49.727694,
       'lon': 10.2443878,
       'tags': {'addr:city': 'Rödelsee',
        'addr:country': 'DE',
        'addr:housenumber': '14',
        'addr:postcode': '97348',
        'addr:street': 'Bachgasse',
        'amenity': 'biergarten',
        'name': 'Martins Brotzeit',
        'note': 'FIXME: Name und genaue Art der Bewirtung'}},
      {'type': 'node',
       'id': 370636759,
       'lat': 49.030173,
       'lon': 12.1013155,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Auer Bräu',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 370637260,
       'lat': 49.022984,
       'lon': 12.0913122,
       'tags': {'amenity': 'biergarten',
        'name': 'Goldene Ente',
        'phone': '(0941) 85 455',
        'website': 'http://www.die-goldene-ente.de',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 370904910,
       'lat': 49.3160959,
       'lon': 7.1390578,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Rosengarten'}},
      {'type': 'node',
       'id': 371137337,
       'lat': 49.8842097,
       'lon': 10.8868558,
       'tags': {'addr:city': 'Bamberg',
        'addr:country': 'DE',
        'addr:housenumber': '49',
        'addr:postcode': '96049',
        'addr:street': 'Oberer Stephansberg',
        'amenity': 'biergarten',
        'contact:email': 'info@wilde-rose-keller.de',
        'contact:phone': '+49 951 57 691',
        'contact:website': 'http://www.wilde-rose-keller.de/',
        'name': 'Wilde Rose Keller',
        'opening_hours': 'May-Sep: Mo-Sa 16:00-22:30; Su 15:00-22:30;PH 15:00-22:30',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 371659044,
       'lat': 48.7079914,
       'lon': 10.879473,
       'tags': {'amenity': 'biergarten',
        'capacity': '50',
        'name': 'Gasthof Schilke'}},
      {'type': 'node',
       'id': 371682688,
       'lat': 49.7572458,
       'lon': 10.9789366,
       'tags': {'addr:city': 'Hallerndorf',
        'addr:country': 'DE',
        'addr:housenumber': '17',
        'addr:postcode': '91352',
        'addr:street': 'Kreuzbergstraße',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'ele': '240.693970',
        'name': 'Dorfkeller Lieberth'}},
      {'type': 'node',
       'id': 371688339,
       'lat': 49.822996,
       'lon': 11.0071242,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'ele': '262.563721',
        'name': 'Hirschaider Keller',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 372746018,
       'lat': 48.8688927,
       'lon': 8.6830087,
       'tags': {'addr:city': 'Pforzheim',
        'addr:housenumber': '6',
        'addr:street': 'Belremstraße',
        'amenity': 'biergarten',
        'name': 'Rabeneck',
        'tourism': 'guest_house',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 372961106,
       'lat': 50.6317712,
       'lon': 7.2144562,
       'tags': {'amenity': 'biergarten', 'name': 'Anleger 640'}},
      {'type': 'node',
       'id': 373159895,
       'lat': 50.1321059,
       'lon': 6.930162,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 373160328,
       'lat': 50.1978535,
       'lon': 6.8357773,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Stellwerk'}},
      {'type': 'node',
       'id': 373264324,
       'lat': 49.8249417,
       'lon': 10.0084161,
       'tags': {'amenity': 'biergarten', 'name': 'Sängerheim'}},
      {'type': 'node',
       'id': 373299903,
       'lat': 50.1481065,
       'lon': 9.9361202,
       'tags': {'amenity': 'biergarten', 'name': 'Heckenwirtschaft Schumm'}},
      {'type': 'node',
       'id': 373343331,
       'lat': 48.1841686,
       'lon': 11.2799886,
       'tags': {'amenity': 'biergarten', 'name': 'Bürgerhaus'}},
      {'type': 'node',
       'id': 373547308,
       'lat': 51.5157635,
       'lon': 13.8981023,
       'tags': {'amenity': 'biergarten', 'name': 'Romi'}},
      {'type': 'node',
       'id': 373851431,
       'lat': 51.4771468,
       'lon': 7.0878993,
       'tags': {'addr:city': 'Essen',
        'addr:country': 'DE',
        'addr:housenumber': '81',
        'addr:postcode': '45309',
        'addr:street': 'Am Mechtenberg',
        'amenity': 'biergarten',
        'name': 'Biergarten am Mechtenberg'}},
      {'type': 'node',
       'id': 374002565,
       'lat': 49.1508069,
       'lon': 7.6087305,
       'tags': {'amenity': 'biergarten', 'name': 'Drei Buchen'}},
      {'type': 'node',
       'id': 374244754,
       'lat': 47.8780428,
       'lon': 10.6273631,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 375937965,
       'lat': 48.7228259,
       'lon': 11.3955892,
       'tags': {'amenity': 'biergarten', 'name': 'Gut Winkelacker'}},
      {'type': 'node',
       'id': 376025638,
       'lat': 47.9205813,
       'lon': 11.376842,
       'tags': {'addr:city': 'Münsing',
        'addr:housenumber': '1',
        'addr:street': 'Buchsee',
        'amenity': 'biergarten',
        'name': 'Buchsee'}},
      {'type': 'node',
       'id': 376045256,
       'lat': 49.0107553,
       'lon': 12.1342938,
       'tags': {'amenity': 'biergarten',
        'name': 'Bosporus',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 376985335,
       'lat': 47.816925,
       'lon': 12.6827036,
       'tags': {'amenity': 'biergarten',
        'name': 'Heutauer Gasthaus',
        'note': 'Gasthaus und Biergarten dauerhaft geschlossen. Nutzungsänderung in Planung. Gebäude wird Namen Gasthaus Heutau wahrscheinlich behalten. Biergarten wird wahrscheinlich in einen Parkplatz umgewidmet.'}},
      {'type': 'node',
       'id': 377041843,
       'lat': 47.8012504,
       'lon': 12.704514,
       'tags': {'amenity': 'biergarten', 'name': 'Hammerwirt'}},
      {'type': 'node',
       'id': 378334277,
       'lat': 52.0665036,
       'lon': 7.4442475,
       'tags': {'amenity': 'biergarten', 'name': 'Zum neuen Herd'}},
      {'type': 'node',
       'id': 379559686,
       'lat': 48.8052563,
       'lon': 9.1742216,
       'tags': {'addr:city': 'Stuttgart',
        'addr:country': 'DE',
        'addr:housenumber': '39',
        'addr:postcode': '70191',
        'addr:street': 'Stresemannstraße',
        'amenity': 'biergarten',
        'name': 'Perkins Park Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 379663192,
       'lat': 48.544032,
       'lon': 11.5208158,
       'tags': {'addr:city': 'Förnbach',
        'addr:street': 'Förnbachstraße',
        'amenity': 'biergarten',
        'name': 'Gasthof Galster',
        'opening_hours': 'Tu 9:00-13:30, 18:00-24:00; We 9:00-13:30; Fr 9:00-13:30, 18:00-24:00; Sa 9:00-13:30; Su 9:00-14:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 379689019,
       'lat': 51.1493065,
       'lon': 12.9286534,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 379718556,
       'lat': 52.1705334,
       'lon': 9.1936455,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Kastanienhof'}},
      {'type': 'node',
       'id': 379735291,
       'lat': 51.0984532,
       'lon': 14.9765878,
       'tags': {'amenity': 'biergarten',
        'name': 'CARARI',
        'website': 'https://www.carari.de'}},
      {'type': 'node',
       'id': 380273058,
       'lat': 49.9465021,
       'lon': 8.4755257,
       'tags': {'amenity': 'biergarten',
        'horse': 'yes',
        'name': 'Joy Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 380324280,
       'lat': 49.3707412,
       'lon': 8.1751989,
       'tags': {'amenity': 'biergarten', 'name': 'Schoppenwiese'}},
      {'type': 'node',
       'id': 380790248,
       'lat': 48.0902139,
       'lon': 9.9199354,
       'tags': {'amenity': 'biergarten', 'name': 'Ponyhof Bareis'}},
      {'type': 'node',
       'id': 382015389,
       'lat': 47.9537341,
       'lon': 11.2682239,
       'tags': {'amenity': 'biergarten', 'name': 'alte Linde'}},
      {'type': 'node',
       'id': 382382617,
       'lat': 50.1456981,
       'lon': 8.6435484,
       'tags': {'addr:city': 'Frankfurt am Main',
        'addr:country': 'DE',
        'addr:housenumber': '8',
        'addr:postcode': '60431',
        'addr:street': 'Am Ginnheimer Wäldchen',
        'addr:suburb': 'Ginnheim',
        'amenity': 'biergarten',
        'contact:email': 'info@ginnheimer-wirtshaus.de',
        'contact:phone': '+49 69 95524000',
        'contact:website': 'http://www.ginnheimer-wirtshaus.de/',
        'name': 'Ginnheimer Wirtshaus',
        'opening_hours': 'May-Oct: Tu-Su 12:00-23:00; Mo off',
        'source': 'http://www.ginnheimer-wirtshaus.de/',
        'source:date': '2017-07-17'}},
      {'type': 'node',
       'id': 382494906,
       'lat': 49.354301,
       'lon': 8.1346898,
       'tags': {'addr:city': 'Neustadt an der Weinstraße',
        'addr:housenumber': '18',
        'addr:street': 'Rathausstraße',
        'amenity': 'biergarten',
        'contact:facebook': 'https://www.facebook.com/BrauchBar-312266970960',
        'contact:phone': '+49 6321 354634',
        'name': 'Brauchbar',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 383081588,
       'lat': 48.8091982,
       'lon': 9.3182243,
       'tags': {'amenity': 'biergarten', 'name': "Biergarten Pit's Pub"}},
      {'type': 'node',
       'id': 383457645,
       'lat': 51.8648063,
       'lon': 14.0896961,
       'tags': {'addr:city': 'Burg (Spreewald)',
        'addr:country': 'DE',
        'addr:housenumber': '29c',
        'addr:postcode': '03096',
        'addr:street': 'Waldschlößchenstraße',
        'amenity': 'biergarten',
        'name': 'Hafenbistro',
        'opening_hours': 'Mo-Su,PH 12:00-20:00',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 384250355,
       'lat': 48.4986662,
       'lon': 9.1935362,
       'tags': {'addr:city': 'Reutlingen',
        'addr:housenumber': '36',
        'addr:postcode': '72760',
        'addr:street': 'Heppstraße',
        'amenity': 'biergarten',
        'fax': '+49 7121 372936',
        'name': 'Karz',
        'opening_hours': 'Mo-Su 11:00-01:00',
        'phone': '+49 7121 370630',
        'toilets:wheelchair': 'no',
        'website': 'http://www.karz.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 384913120,
       'lat': 53.1241512,
       'lon': 8.9850594,
       'tags': {'amenity': 'biergarten', 'name': 'Meyerdierks'}},
      {'type': 'node',
       'id': 385075372,
       'lat': 49.959026,
       'lon': 11.5693887,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 385088590,
       'lat': 48.8763388,
       'lon': 9.0738001,
       'tags': {'addr:city': 'Schwieberdingen',
        'addr:country': 'DE',
        'addr:housenumber': '3',
        'addr:postcode': '71701',
        'addr:street': 'Schloßhof',
        'amenity': 'biergarten',
        'cuisine': 'german',
        'food': 'yes',
        'name': 'Bierakademie',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 385126376,
       'lat': 48.80789,
       'lon': 9.224023,
       'tags': {'amenity': 'biergarten',
        'name': 'Augustiner Biergarten',
        'operator': 'Kursaal Bad Cannstatt'}},
      {'type': 'node',
       'id': 385400878,
       'lat': 48.9621595,
       'lon': 11.6891956,
       'tags': {'addr:city': 'Riedenburg',
        'addr:country': 'DE',
        'addr:housenumber': '5',
        'addr:postcode': '93339',
        'addr:street': 'Hammerweg',
        'amenity': 'biergarten',
        'brewery': 'Riedenburger',
        'email': 'info@riedenburger.de',
        'name': 'Biergarten Unterkrieger',
        'opening_hours': 'Fr-Su,PH 11:00-21:00',
        'organic': 'only',
        'website': 'http://www.riedenburger.de/startseite/heimat/biergarten.html',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 385551008,
       'lat': 51.05327,
       'lon': 13.8117548,
       'tags': {'addr:city': 'Dresden',
        'addr:country': 'DE',
        'addr:housenumber': '18',
        'addr:street': 'Friedrich-Wieck-Straße',
        'amenity': 'biergarten',
        'contact:website': 'www.elbegarten.de',
        'cuisine': 'german',
        'name': 'Demnitz Elbegarten',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 385890941,
       'lat': 48.7695783,
       'lon': 8.8494188,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthaus Traube',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 385892521,
       'lat': 48.7706031,
       'lon': 8.8532996,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 385892995,
       'lat': 48.7698135,
       'lon': 8.8511189,
       'tags': {'amenity': 'biergarten',
        'name': 'Landgasthof 1610',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 385907420,
       'lat': 48.7893914,
       'lon': 8.836122,
       'tags': {'amenity': 'biergarten',
        'name': 'Würmbrücke',
        'opening_hours': 'We-Su 11:00-22:00',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes',
        'wheelchair:description': 'Bei Bedarf kann eine Rampe angebracht werden;Der Außenbereich ist aber ohne Treppen.'}},
      {'type': 'node',
       'id': 386160839,
       'lat': 53.6407113,
       'lon': 10.6658988,
       'tags': {'amenity': 'biergarten', 'name': 'Zur Alten Ziegelei'}},
      {'type': 'node',
       'id': 386246578,
       'lat': 51.2023843,
       'lon': 12.3864474,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Zur Eiche'}},
      {'type': 'node',
       'id': 386246616,
       'lat': 51.1953812,
       'lon': 12.4067711,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten'}},
      {'type': 'node',
       'id': 387474006,
       'lat': 49.9895389,
       'lon': 8.8029196,
       'tags': {'amenity': 'biergarten', 'name': 'Grüner Baum'}},
      {'type': 'node',
       'id': 387503112,
       'lat': 48.37534,
       'lon': 8.1857023,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 388030274,
       'lat': 49.8300088,
       'lon': 9.6290462,
       'tags': {'amenity': 'biergarten', 'name': 'Krähennest'}},
      {'type': 'node',
       'id': 388108927,
       'lat': 52.4991189,
       'lon': 9.9418412,
       'tags': {'amenity': 'biergarten', 'name': 'Waldbühne'}},
      {'type': 'node',
       'id': 388237596,
       'lat': 47.8416135,
       'lon': 10.6764176,
       'tags': {'amenity': 'biergarten',
        'name': 'Mooshütte',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 388370411,
       'lat': 51.1362857,
       'lon': 9.99286,
       'tags': {'amenity': 'biergarten',
        'name': 'Wichtelbrunnen',
        'website': 'http://www.wichtelbrunnen.de'}},
      {'type': 'node',
       'id': 388413379,
       'lat': 48.1703718,
       'lon': 11.2479741,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 388514302,
       'lat': 52.4123211,
       'lon': 13.6095915,
       'tags': {'addr:city': 'Berlin',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:postcode': '12559',
        'addr:street': 'Zum Schmetterlingshorst',
        'addr:suburb': 'Köpenick',
        'amenity': 'biergarten',
        'cuisine': 'german',
        'email': 'schmetterlingshorst@berlin.de',
        'image': 'File:Schmetterlingshorst Berlin 04.jpg',
        'name': 'Schmetterlingshorst',
        'opening_hours': 'Oct-Mar: Tu-Fr 11:00-16:00; Sa-Su 11:00-17:00; Apr-Sep: Mo-Fr 10:00-17:00; Sa-Su 10:00-19:00',
        'operator': 'Bezirkssportbund Treptow-Köpenick e.V.',
        'phone': '+49-30-61674861',
        'website': 'http://www.schmetterlingshorst.de',
        'wheelchair': 'yes',
        'wikidata': 'Q2246147',
        'wikipedia': 'de:Schmetterlingshorst'}},
      {'type': 'node',
       'id': 388646232,
       'lat': 51.8063645,
       'lon': 6.7532038,
       'tags': {'amenity': 'biergarten', 'name': 'Hubertushof'}},
      {'type': 'node',
       'id': 388870111,
       'lat': 48.5875768,
       'lon': 9.7318283,
       'tags': {'amenity': 'biergarten',
        'historic': 'ruins',
        'name': 'Burgruine Berneck'}},
      {'type': 'node',
       'id': 388993529,
       'lat': 50.59566,
       'lon': 7.2915348,
       'tags': {'amenity': 'biergarten', 'name': 'Erler Berghütte'}},
      {'type': 'node',
       'id': 389015027,
       'lat': 48.333913,
       'lon': 11.6561736,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 389070257,
       'lat': 49.5985186,
       'lon': 11.3405867,
       'tags': {'amenity': 'biergarten', 'smoking': 'yes'}},
      {'type': 'node',
       'id': 389141637,
       'lat': 48.0615134,
       'lon': 8.4587737,
       'tags': {'amenity': 'biergarten', 'name': 'Turmstube'}},
      {'type': 'node',
       'id': 389945262,
       'lat': 48.277532,
       'lon': 10.8839574,
       'tags': {'amenity': 'biergarten', 'name': 'Gaststätte Trachtenheim'}},
      {'type': 'node',
       'id': 390288093,
       'lat': 48.1639498,
       'lon': 11.475791,
       'tags': {'addr:city': 'München',
        'addr:housenumber': '47',
        'addr:postcode': '81247',
        'addr:street': 'Verdistraße',
        'amenity': 'biergarten',
        'brewery': 'Augustiner Bräu München',
        'name': 'Zum grünen Baum',
        'outdoor_seating': 'yes',
        'website': 'http://www.gruenerbaum-muenchen.de/',
        'wheelchair': 'yes',
        'wheelchair:description': 'Der Biergarten ist durch teilweise tiefen Kies schwer befahrbar.'}},
      {'type': 'node',
       'id': 391183828,
       'lat': 49.3692311,
       'lon': 8.5417648,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 391530306,
       'lat': 53.1547763,
       'lon': 12.8742134,
       'tags': {'addr:city': 'Rheinsberg',
        'addr:country': 'DE',
        'addr:housenumber': '5',
        'addr:postcode': '16831',
        'addr:street': 'Zechliner Straße',
        'addr:suburb': 'Zechlinerhütte',
        'amenity': 'biergarten',
        'fax': '+49 33921 76919',
        'name': 'Haus am See',
        'phone': '+49 33921 7690',
        'source': 'http://www.hotel-see-rheinsberg.de/',
        'tourism': 'hotel',
        'website': 'http://www.hotel-see-rheinsberg.de/'}},
      {'type': 'node',
       'id': 391984640,
       'lat': 50.5533166,
       'lon': 12.1875622,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 392017012,
       'lat': 49.7376472,
       'lon': 10.1591628,
       'tags': {'amenity': 'biergarten', 'name': 'Kanapee'}},
      {'type': 'node',
       'id': 392039588,
       'lat': 54.4562606,
       'lon': 11.2738323,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 392244950,
       'lat': 49.6727412,
       'lon': 10.0480678,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 392246635,
       'lat': 49.0506716,
       'lon': 9.3756003,
       'tags': {'amenity': 'biergarten',
        'name': 'Obere Ölmühle',
        'note': 'geöffnet Sonn. und Feiertage Link: http://www.yelp.de/biz/obere-%C3%B6lm%C3%BChle-oberstenfeld',
        'source': 'GPS'}},
      {'type': 'node',
       'id': 392687541,
       'lat': 51.8101792,
       'lon': 10.92541,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Mönchemühlenteich',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 393101216,
       'lat': 48.1787508,
       'lon': 11.2540054,
       'tags': {'amenity': 'biergarten', 'name': 'Unterhaus', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 393299545,
       'lat': 51.7203789,
       'lon': 8.7510464,
       'tags': {'addr:city': 'Paderborn',
        'addr:country': 'DE',
        'addr:housenumber': '9',
        'addr:postcode': '33098',
        'addr:street': 'Kisau',
        'amenity': 'biergarten',
        'brewery': 'Warsteiner',
        'name': 'Deutsches Haus',
        'outdoor_seating': 'sidewalk',
        'weather_protection': 'parasol',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 393354110,
       'lat': 48.0493925,
       'lon': 10.6124025,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 393462645,
       'lat': 51.2306406,
       'lon': 12.7262287,
       'tags': {'amenity': 'biergarten',
        'name': 'Restaurant "Zur Großmühle"',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 394870004,
       'lat': 51.1113298,
       'lon': 13.6670163,
       'tags': {'amenity': 'biergarten',
        'name': 'Weingut Seifert',
        'note': "not really a 'biergarten' :)"}},
      {'type': 'node',
       'id': 399715175,
       'lat': 49.1109752,
       'lon': 9.7348738,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Unterwöhrd',
        'source': 'knowledge',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 400916176,
       'lat': 52.4747532,
       'lon': 13.5241898,
       'tags': {'amenity': 'biergarten',
        'name': 'Albers Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 401125548,
       'lat': 50.358977,
       'lon': 10.9099632,
       'tags': {'amenity': 'biergarten',
        'name': 'Alexandrinenhütte',
        'website': 'http://www.farnkraut-coburg.de/html/alexandrinenhutte.html'}},
      {'type': 'node',
       'id': 401258103,
       'lat': 48.1729642,
       'lon': 11.4931118,
       'tags': {'amenity': 'biergarten',
        'capacity': '1700',
        'name': 'die Fasanerie',
        'opening_hours': 'Mo-Fr 16:00-22:00; Sa,Su 12:00-22:00',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 401493462,
       'lat': 48.0595587,
       'lon': 10.6396548,
       'tags': {'amenity': 'biergarten', 'name': 'Café-Restaurant Schlossgarten'}},
      {'type': 'node',
       'id': 401858029,
       'lat': 51.1363185,
       'lon': 11.7211675,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 402740067,
       'lat': 48.1280939,
       'lon': 11.3261134,
       'tags': {'amenity': 'biergarten', 'horse': 'yes', 'name': 'Schusterhäusl'}},
      {'type': 'node',
       'id': 402842143,
       'lat': 50.3135651,
       'lon': 8.9959415,
       'tags': {'amenity': 'biergarten',
        'name': 'Landgasthof Glauberg',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 402949932,
       'lat': 50.9278772,
       'lon': 13.3601601,
       'tags': {'addr:city': 'Freiberg',
        'addr:country': 'DE',
        'addr:postcode': '09599',
        'addr:street': 'Fuchsmühlenweg',
        'amenity': 'biergarten',
        'name': 'Beachclub 7',
        'website': 'http://www.beachclub7.com/'}},
      {'type': 'node',
       'id': 402950296,
       'lat': 49.8610199,
       'lon': 11.7373867,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 403194495,
       'lat': 50.0740722,
       'lon': 10.2152524,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 403288122,
       'lat': 49.9471935,
       'lon': 9.7709394,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 403289784,
       'lat': 47.7519349,
       'lon': 11.7387535,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthaus am Gasteig'}},
      {'type': 'node',
       'id': 403866949,
       'lat': 51.3105677,
       'lon': 12.3762362,
       'tags': {'amenity': 'biergarten',
        'name': 'Prager Frühling',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 404389865,
       'lat': 47.6718642,
       'lon': 12.7843607,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Haiderhof'}},
      {'type': 'node',
       'id': 405170461,
       'lat': 48.001468,
       'lon': 11.0131844,
       'tags': {'amenity': 'biergarten',
        'capacity': '120',
        'name': 'Windachseealm',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 406076371,
       'lat': 47.7537269,
       'lon': 11.7183814,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthof Weidenau',
        'source': 'survey'}},
      {'type': 'node',
       'id': 406358613,
       'lat': 47.8584247,
       'lon': 10.0391094,
       'tags': {'amenity': 'biergarten', 'name': 'Kuhstallstüble'}},
      {'type': 'node',
       'id': 408315200,
       'lat': 51.8535612,
       'lon': 12.1779528,
       'tags': {'amenity': 'biergarten', 'name': 'Die Scheune'}},
      {'type': 'node',
       'id': 408473643,
       'lat': 47.6175172,
       'lon': 9.9287005,
       'tags': {'addr:city': 'Heimenkirch',
        'addr:housenumber': '138',
        'addr:postcode': '88178',
        'addr:street': 'Riedhirsch',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'description': 'Lokal mit Biergarten am Radweg Riedhirsch',
        'name': 'Zum Holzmichel',
        'phone': '08381/890144',
        'website': 'http://www.holzmichlseinkehr.de'}},
      {'type': 'node',
       'id': 408811512,
       'lat': 48.676842,
       'lon': 9.2173424,
       'tags': {'amenity': 'biergarten', 'name': 'Gaststätte Bahnhof'}},
      {'type': 'node',
       'id': 409004231,
       'lat': 48.1279193,
       'lon': 12.7857994,
       'tags': {'amenity': 'biergarten',
        'name': 'Klostergarten',
        'opening_hours': 'Sa,Su 11:00-20:00; SH Tu,Su 11:00-20:00',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 409683806,
       'lat': 47.9779876,
       'lon': 11.4664793,
       'tags': {'amenity': 'biergarten', 'name': 'Klosterbräu'}},
      {'type': 'node',
       'id': 409710868,
       'lat': 51.412227,
       'lon': 7.1458938,
       'tags': {'amenity': 'biergarten',
        'ele': '63.8127441',
        'name': 'Leinpfad Oase'}},
      {'type': 'node',
       'id': 410186680,
       'lat': 49.9200788,
       'lon': 8.1055039,
       'tags': {'amenity': 'biergarten',
        'name': 'Gutsschänke Bacchushof',
        'opening_hours': 'Tu-Fr 16:00+, Sa-Su 11:30+'}},
      {'type': 'node',
       'id': 410217303,
       'lat': 52.5905957,
       'lon': 13.2700085,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 410299103,
       'lat': 50.219231,
       'lon': 11.9365023,
       'tags': {'amenity': 'biergarten',
        'name': 'Squaw Valley',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 410311507,
       'lat': 48.824263,
       'lon': 8.9115193,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 410461712,
       'lat': 51.7185773,
       'lon': 8.3087002,
       'tags': {'amenity': 'biergarten',
        'operator': 'Landgasthaus Söbke',
        'website': 'http://www.landgasthaus-soebke.de'}},
      {'type': 'node',
       'id': 410473678,
       'lat': 48.7459696,
       'lon': 11.6351461,
       'tags': {'amenity': 'biergarten', 'name': 'Birkenheide'}},
      {'type': 'node',
       'id': 410652221,
       'lat': 50.627495,
       'lon': 6.4705565,
       'tags': {'amenity': 'biergarten', 'name': 'Terasse am See'}},
      {'type': 'node',
       'id': 410860454,
       'lat': 49.0345254,
       'lon': 11.4737375,
       'tags': {'addr:housenumber': '23',
        'addr:street': 'Hauptstraße',
        'amenity': 'biergarten',
        'contact:email': 'info@fuchsbraeu.de',
        'contact:phone': '+49 8461 6520',
        'contact:website': 'http://www.fuchsbraeu.de/',
        'name': 'Fuchsbräu',
        'source': 'http://www.fuchsbraeu.de/',
        'source:date': '2016-06-17'}},
      {'type': 'node',
       'id': 411309926,
       'lat': 49.3651506,
       'lon': 11.4161036,
       'tags': {'amenity': 'biergarten', 'name': 'Klostermühle'}},
      {'type': 'node',
       'id': 411819333,
       'lat': 52.2502413,
       'lon': 11.6343775,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 412229497,
       'lat': 49.7856926,
       'lon': 7.8342049,
       'tags': {'amenity': 'biergarten',
        'email': 'info@altenbaumburg.de',
        'fax': '+49 6708 3673',
        'kitchen_hours': 'We-Tu 11:00-20:00',
        'name': 'Altenbaumburg',
        'opening_hours': 'We-Tu 11:00-23:00',
        'phone': '+49 6708 3551',
        'smoking': 'outside',
        'website': 'http://www.altenbaumburg.de/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 412406290,
       'lat': 49.2979447,
       'lon': 11.3702757,
       'tags': {'amenity': 'biergarten', 'name': 'Gradl Hof'}},
      {'type': 'node',
       'id': 412494340,
       'lat': 49.1897523,
       'lon': 8.380727,
       'tags': {'addr:city': 'Germersheim',
        'addr:country': 'DE',
        'addr:housename': 'Alte Ziegelei',
        'addr:postcode': '76726',
        'amenity': 'biergarten',
        'name': 'Rasthaus Ziegelei',
        'website': 'http://www.ausgehen-in-germersheim.de/Werbepartner/Ziegelei/Ziegelei.htm'}},
      {'type': 'node',
       'id': 412920183,
       'lat': 48.7715273,
       'lon': 10.6471209,
       'tags': {'amenity': 'biergarten',
        'name': 'Waldschenke Eisbrunn',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 412956942,
       'lat': 48.2767491,
       'lon': 11.0970225,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Fischerwirt'}},
      {'type': 'node',
       'id': 413460864,
       'lat': 49.7468547,
       'lon': 9.2227292,
       'tags': {'amenity': 'biergarten',
        'name': 'Im Sommer Biergarten Gutsschänke Roßhof'}},
      {'type': 'node',
       'id': 413462097,
       'lat': 48.8809294,
       'lon': 12.5658508,
       'tags': {'amenity': 'biergarten', 'name': 'Wirtsgarten Geiss'}},
      {'type': 'node',
       'id': 413568558,
       'lat': 48.6007492,
       'lon': 10.1292702,
       'tags': {'amenity': 'biergarten',
        'name': 'Hofschenke (Zum schwarzen Beck)'}},
      {'type': 'node',
       'id': 413680277,
       'lat': 51.480146,
       'lon': 6.7914738,
       'tags': {'amenity': 'biergarten', 'name': 'Meidericher Hahn'}},
      {'type': 'node',
       'id': 414026518,
       'lat': 50.9163562,
       'lon': 10.3930726,
       'tags': {'amenity': 'biergarten', 'name': 'Thalfried'}},
      {'type': 'node',
       'id': 414058956,
       'lat': 52.1126582,
       'lon': 13.6191463,
       'tags': {'amenity': 'biergarten', 'name': "Gabi's Biergarten"}},
      {'type': 'node',
       'id': 414180935,
       'lat': 50.1587615,
       'lon': 7.6928225,
       'tags': {'addr:city': 'Sankt Goar',
        'addr:country': 'DE',
        'addr:postcode': '56329',
        'addr:street': 'Helenenhof',
        'addr:suburb': 'Werlau',
        'amenity': 'biergarten',
        'contact:email': 'info@helenenhof-werlau.de',
        'contact:mobile': '+49 170 9974066',
        'contact:phone': '+49 6741 7693',
        'contact:website': 'http://helenenhof-werlau.de/',
        'name': 'Biergarten Helenenhof',
        'operator': 'Fredi Mudersbach',
        'source': 'http://helenenhof-werlau.de/',
        'source:date': '2017-08-18',
        'wheelchair': 'yes',
        'wheelchair:description': 'keine stufen vorhanden'}},
      {'type': 'node',
       'id': 414981326,
       'lat': 49.7331597,
       'lon': 10.156565,
       'tags': {'amenity': 'biergarten',
        'name': 'Kastanienhof',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 415071234,
       'lat': 51.8683955,
       'lon': 14.1296678,
       'tags': {'amenity': 'biergarten', 'outdoor_seating': 'yes'}},
      {'type': 'node',
       'id': 415268912,
       'lat': 48.1709577,
       'lon': 11.7175501,
       'tags': {'amenity': 'biergarten', 'name': 'Schreiberhof'}},
      {'type': 'node',
       'id': 415691892,
       'lat': 51.6899449,
       'lon': 12.4877967,
       'tags': {'addr:city': 'Gräfenhainichen',
        'addr:housenumber': '2',
        'addr:postcode': '06773',
        'addr:street': 'Am Waldrand',
        'amenity': 'biergarten',
        'name': 'Waldschenke Jösigk'}},
      {'type': 'node',
       'id': 415935030,
       'lat': 47.5972628,
       'lon': 9.5393973,
       'tags': {'amenity': 'biergarten', 'name': 'Krone', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 416933121,
       'lat': 49.0211618,
       'lon': 12.173117,
       'tags': {'amenity': 'biergarten', 'name': 'Gaststätte KAIN'}},
      {'type': 'node',
       'id': 416995453,
       'lat': 50.961872,
       'lon': 13.9453098,
       'tags': {'addr:city': 'Pirna',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '01796',
        'addr:street': 'Schlosshof',
        'amenity': 'biergarten',
        'contact:phone': '+49 3501 490690',
        'email': 'info@schlossschaenke.com',
        'name': 'Biergarten Schlosschänke',
        'opening_hours': 'Mar,Apr: 12:00-19:00; May-Sep: 10:00-22:00; Oct: 12:00-19:00',
        'phone': '+49 3501 490690',
        'website': 'http://www.schlossschaenke.com/',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 417001026,
       'lat': 50.9503396,
       'lon': 13.9904218,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthof Obervogelgesang'}},
      {'type': 'node',
       'id': 417231963,
       'lat': 48.7520158,
       'lon': 9.6453605,
       'tags': {'amenity': 'biergarten',
        'day_off': 'Sunday',
        'day_on': 'Saturday',
        'description': 'Nur am Samstagen, Sonn- und Feiertagen geöffnet.',
        'name': 'Marbachstüble'}},
      {'type': 'node',
       'id': 417325165,
       'lat': 48.1686952,
       'lon': 11.4579208,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '39',
        'addr:postcode': '81247',
        'addr:street': 'Dorfstraße',
        'alt_name': 'Alter Wirt',
        'amenity': 'biergarten',
        'brewery': 'Augustiner Bräu München',
        'cuisine': 'bavarian',
        'name': 'Zum Alten Wirt',
        'toilets:wheelchair': 'no',
        'website': 'http://www.alterwirt-obermenzing.de/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 417337814,
       'lat': 53.5918004,
       'lon': 10.0286073,
       'tags': {'addr:city': 'Hamburg',
        'addr:housenumber': '5 B',
        'addr:postcode': '22303',
        'addr:street': 'Südring',
        'amenity': 'biergarten',
        'name': "Sierich's Biergarten",
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 418126051,
       'lat': 47.6847489,
       'lon': 11.1783352,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 418722156,
       'lat': 49.1568225,
       'lon': 12.8323615,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Kiosk Stausee'}},
      {'type': 'node',
       'id': 418765936,
       'lat': 48.7746752,
       'lon': 11.7942948,
       'tags': {'amenity': 'biergarten', 'name': 'Lenkers Biergarten'}},
      {'type': 'node',
       'id': 418778874,
       'lat': 48.5061266,
       'lon': 9.2381117,
       'tags': {'amenity': 'biergarten',
        'name': 'Rosengarten',
        'website': 'http://www.rosengarten-reutlingen.de/'}},
      {'type': 'node',
       'id': 418839136,
       'lat': 50.0881705,
       'lon': 8.230881,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 419183828,
       'lat': 51.4323635,
       'lon': 7.0048144,
       'tags': {'amenity': 'biergarten',
        'name': 'miamamia',
        'surface': 'gravel',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 419411093,
       'lat': 51.3460555,
       'lon': 6.6178924,
       'tags': {'amenity': 'biergarten',
        'name': 'Chocolate Fish',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 419419793,
       'lat': 49.8598447,
       'lon': 10.2270955,
       'tags': {'amenity': 'biergarten', 'name': 'Athmosphere'}},
      {'type': 'node',
       'id': 419429244,
       'lat': 49.7551666,
       'lon': 10.2396128,
       'tags': {'addr:city': 'Großlangheim',
        'addr:housenumber': '48',
        'addr:postcode': '97320',
        'addr:street': 'Hauptstraße',
        'amenity': 'biergarten',
        'name': 'Zum Hadi',
        'note': 'FIXME: Hausnummer und Telefon der neuen Gaststätte'}},
      {'type': 'node',
       'id': 419842089,
       'lat': 51.3189205,
       'lon': 9.4924189,
       'tags': {'amenity': 'biergarten', 'name': 'Lolitas Garten'}},
      {'type': 'node',
       'id': 420022066,
       'lat': 49.8752509,
       'lon': 10.1565708,
       'tags': {'addr:city': 'Eisenheim',
        'addr:housename': 'Biergarten Mainschleife',
        'addr:housenumber': '1',
        'addr:place': 'Kaltenhausen',
        'addr:postcode': '97247',
        'amenity': 'biergarten',
        'name': 'Biergarten Mainschleife',
        'website': 'http://www.biergarten-mainschleife.de/index.html'}},
      {'type': 'node',
       'id': 420213807,
       'lat': 49.7666239,
       'lon': 9.2495417,
       'tags': {'amenity': 'biergarten', 'name': 'Jausenstation'}},
      {'type': 'node',
       'id': 420372270,
       'lat': 49.5523905,
       'lon': 10.3134694,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Erdinger; Landwehrbräu',
        'name': 'Weinbau Wildberghof',
        'website': 'http://www.wildberghof.de'}},
      {'type': 'node',
       'id': 420892653,
       'lat': 49.7531665,
       'lon': 10.4757657,
       'tags': {'amenity': 'biergarten', 'name': "Sonja's Grillgarten"}},
      {'type': 'node',
       'id': 422810945,
       'lat': 49.8369361,
       'lon': 10.9280521,
       'tags': {'amenity': 'biergarten', 'name': 'Pettstadter Keller'}},
      {'type': 'node',
       'id': 423805971,
       'lat': 49.7989199,
       'lon': 8.832808,
       'tags': {'amenity': 'biergarten', 'name': 'Tennishalle'}},
      {'type': 'node',
       'id': 424065858,
       'lat': 50.0198201,
       'lon': 8.4035,
       'tags': {'amenity': 'biergarten',
        'name': 'Flörsheimer Warte',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 424238786,
       'lat': 49.9864785,
       'lon': 7.8665089,
       'tags': {'addr:city': 'Rüdesheim am Rhein',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '65385',
        'addr:street': 'Bahnhofstraße',
        'addr:suburb': 'Assmannshausen',
        'amenity': 'biergarten',
        'email': 'info@rheinhotels-kesseler.de',
        'fax': '+49 6722 911091',
        'name': 'Germania',
        'phone': '+49 6722 2749',
        'source': 'http://www.rheinhotels-kesseler.de/',
        'source:date': '2015-02-25',
        'website': 'http://www.rheinhotels-kesseler.de/'}},
      {'type': 'node',
       'id': 426932542,
       'lat': 50.8739702,
       'lon': 6.8153181,
       'tags': {'amenity': 'biergarten', 'name': 'Zur Deutschen Ecke'}},
      {'type': 'node',
       'id': 426950255,
       'lat': 50.0746042,
       'lon': 10.3506093,
       'tags': {'addr:city': 'Schonungen',
        'addr:country': 'DE',
        'addr:postcode': '97453',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Steinachblick',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'N 007',
        'source': 'Datenspende der NaturFreunde Deutschland'}},
      {'type': 'node',
       'id': 427525569,
       'lat': 49.5978353,
       'lon': 11.480521,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 427536589,
       'lat': 49.949991,
       'lon': 10.8614752,
       'tags': {'amenity': 'biergarten', 'name': 'Wagner-Keller'}},
      {'type': 'node',
       'id': 427698046,
       'lat': 48.468609,
       'lon': 10.7929776,
       'tags': {'amenity': 'biergarten', 'name': 'Gersthofer Hütte'}},
      {'type': 'node',
       'id': 427712658,
       'lat': 47.9952686,
       'lon': 11.1686405,
       'tags': {'amenity': 'biergarten', 'name': 'Seehof', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 427966397,
       'lat': 49.1803548,
       'lon': 9.4836448,
       'tags': {'amenity': 'biergarten', 'name': 'Lösch'}},
      {'type': 'node',
       'id': 428576748,
       'lat': 52.2965483,
       'lon': 13.6256778,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 428655300,
       'lat': 49.6237965,
       'lon': 9.6650218,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 428748516,
       'lat': 51.3585068,
       'lon': 12.3044698,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 429236721,
       'lat': 49.316176,
       'lon': 8.426914,
       'tags': {'amenity': 'biergarten', 'name': 'Alte Pasta Pasta'}},
      {'type': 'node',
       'id': 429914227,
       'lat': 50.9184493,
       'lon': 14.0569386,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 429995583,
       'lat': 49.5107529,
       'lon': 7.0221766,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Johann-Adams-Mühle',
        'place': 'hamlet',
        'tourism': 'attraction',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 430375822,
       'lat': 51.9931849,
       'lon': 7.4820104,
       'tags': {'amenity': 'biergarten', 'name': 'Egons Kotten'}},
      {'type': 'node',
       'id': 430610468,
       'lat': 51.9770844,
       'lon': 9.5172399,
       'tags': {'addr:city': 'Bodenwerder',
        'addr:postcode': '37619',
        'addr:street': 'Homburgstraße',
        'amenity': 'biergarten',
        'name': 'Biergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 431151533,
       'lat': 51.2550234,
       'lon': 12.5387706,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 431246865,
       'lat': 49.3333581,
       'lon': 6.8470573,
       'tags': {'amenity': 'biergarten',
        'name': 'Fischerhütte',
        'operator': 'Angelsportverein Schwarzenholz 1963',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 431258028,
       'lat': 50.0564254,
       'lon': 8.2303062,
       'tags': {'amenity': 'biergarten',
        'description': 'Nur im Sommer',
        'name': 'Lohmühle',
        'opening_hours': 'Tu-Fr 16:00-22:00; Sa 15:00-22:00; Su,Ph 12:00-22:00'}},
      {'type': 'node',
       'id': 431266461,
       'lat': 50.1055073,
       'lon': 8.6910281,
       'tags': {'addr:housenumber': '49',
        'addr:postcode': '60594',
        'addr:street': 'Große Rittergasse',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'email': 'info@lorsbacher-thal.de',
        'name': 'Lorsbacher Thal Apfelweingarten',
        'opening_hours': 'Mo-Su 12:00-00:00',
        'phone': '+49 61 09 50 77 60',
        'website': 'https://www.lorsbacher-thal.de/'}},
      {'type': 'node',
       'id': 431283854,
       'lat': 50.1147896,
       'lon': 9.8891685,
       'tags': {'addr:housenumber': '9',
        'addr:postcode': '97762',
        'addr:street': 'Weihertorstraße',
        'amenity': 'biergarten',
        'name': 'Finbarrs Irish Pub',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 431820570,
       'lat': 50.6330522,
       'lon': 12.2151229,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Waldfrieden'}},
      {'type': 'node',
       'id': 431884335,
       'lat': 51.0247395,
       'lon': 13.444955,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 431926149,
       'lat': 50.8023631,
       'lon': 10.4486166,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten am Mommelstein'}},
      {'type': 'node',
       'id': 432585605,
       'lat': 53.5287908,
       'lon': 7.2515326,
       'tags': {'amenity': 'biergarten',
        'name': 'Hof Klaassen',
        'opening_hours': 'Tu 19:00-22:00; Th 11:00-16:00; Sep-Jun off'}},
      {'type': 'node',
       'id': 432666299,
       'lat': 51.0947667,
       'lon': 13.8415398,
       'tags': {'amenity': 'biergarten', 'operator': 'Einkehr'}},
      {'type': 'node',
       'id': 432982738,
       'lat': 47.859643,
       'lon': 11.2308648,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthof Steidl'}},
      {'type': 'node',
       'id': 433065328,
       'lat': 51.5681275,
       'lon': 6.9616869,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 433723853,
       'lat': 50.2212822,
       'lon': 11.0676872,
       'tags': {'amenity': 'biergarten',
        'name': 'Goldener Stern',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 433752389,
       'lat': 53.186884,
       'lon': 12.9221427,
       'tags': {'addr:city': 'Rheinsberg',
        'addr:country': 'DE',
        'addr:postcode': '16831',
        'addr:street': 'Am Kleinen Pälitzsee',
        'amenity': 'biergarten',
        'email': 'ray@bootundmehr.com',
        'name': 'Boot & Mehr',
        'phone': '+49 33921 70445; +49 33921 70216',
        'phone:mobile': '+49 173 3845417',
        'source': 'http://www.bootundmehr.com/',
        'website': 'http://www.bootundmehr.com/'}},
      {'type': 'node',
       'id': 433999690,
       'lat': 49.1294646,
       'lon': 12.8643233,
       'tags': {'amenity': 'biergarten', 'name': 'Seeblick'}},
      {'type': 'node',
       'id': 434362081,
       'lat': 48.1092401,
       'lon': 11.6703237,
       'tags': {'amenity': 'biergarten',
        'name': 'Franziskaner Garten Biergarten',
        'opening_hours': 'Mo-Su 11:00-22:30',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 434467556,
       'lat': 48.1972215,
       'lon': 10.1756584,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Gasthof "Zur Linde"'}},
      {'type': 'node',
       'id': 434467569,
       'lat': 48.1968704,
       'lon': 10.1686176,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Gasthaus Adler'}},
      {'type': 'node',
       'id': 434503297,
       'lat': 50.2951209,
       'lon': 7.6014343,
       'tags': {'addr:city': 'Koblenz',
        'addr:housenumber': '23 - 25',
        'addr:postcode': '56075',
        'addr:street': 'Brunnenstraße',
        'amenity': 'biergarten',
        'name': 'Zur Kripp',
        'opening_hours': 'Su-Mo 11:00-22:00, Fr,Sa 11:00-23:00',
        'outdoor_seating': 'yes',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 434564435,
       'lat': 52.3735471,
       'lon': 13.6201106,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 434745346,
       'lat': 52.0252508,
       'lon': 13.1020968,
       'tags': {'amenity': 'biergarten', 'name': 'Kloster-Eck'}},
      {'type': 'node',
       'id': 434765910,
       'lat': 47.6925409,
       'lon': 9.854384,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 434765912,
       'lat': 47.6928798,
       'lon': 9.853574,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 437522759,
       'lat': 53.5415873,
       'lon': 8.0587818,
       'tags': {'amenity': 'biergarten',
        'name': 'Antonslust',
        'phone': '+49 4421-879600',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 437614448,
       'lat': 52.5213454,
       'lon': 13.4059828,
       'tags': {'addr:city': 'Berlin',
        'addr:country': 'DE',
        'addr:housenumber': '9',
        'addr:postcode': '10178',
        'addr:street': 'Karl-Liebknecht-Straße',
        'addr:suburb': 'Mitte',
        'amenity': 'biergarten',
        'name': "Schlögl's",
        'outdoor_seating': 'yes',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 438209267,
       'lat': 52.4608859,
       'lon': 13.5459148,
       'tags': {'amenity': 'biergarten', 'name': 'Viva an der Kindlbühne'}},
      {'type': 'node',
       'id': 438522846,
       'lat': 50.1822945,
       'lon': 8.596077,
       'tags': {'addr:city': 'Oberursel (Taunus)',
        'addr:housenumber': '50',
        'addr:postcode': '61440',
        'addr:street': 'Kurmainzer Straße',
        'amenity': 'biergarten',
        'email': 'info@zum-ruehl.de',
        'fax': '+49 6171 982594',
        'name': 'Zum Rühl',
        'outdoor_seating': 'yes',
        'phone': '+49 6171 73477',
        'website': 'http://www.zum-ruehl.de/'}},
      {'type': 'node',
       'id': 438522853,
       'lat': 50.181067,
       'lon': 8.595747,
       'tags': {'addr:city': 'Oberursel (Taunus)',
        'addr:country': 'DE',
        'addr:housenumber': '12',
        'addr:postcode': '61440',
        'addr:street': 'Urselbachstraße',
        'amenity': 'biergarten',
        'name': 'Gasthaus zur Linde',
        'outdoor_seating': 'yes',
        'phone': '+49 6171 286355',
        'source': 'Survey',
        'website': 'http://www.zur-linde-oberursel.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 439183119,
       'lat': 47.7632743,
       'lon': 11.38524,
       'tags': {'amenity': 'biergarten', 'name': 'Poseidon'}},
      {'type': 'node',
       'id': 439533838,
       'lat': 49.761772,
       'lon': 8.1783691,
       'tags': {'amenity': 'biergarten', 'name': 'Cavallino'}},
      {'type': 'node',
       'id': 440003900,
       'lat': 48.986916,
       'lon': 12.0128752,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 440356265,
       'lat': 48.2201788,
       'lon': 8.5995532,
       'tags': {'amenity': 'biergarten', 'name': 'Rosenhütte'}},
      {'type': 'node',
       'id': 440430519,
       'lat': 49.9434159,
       'lon': 11.573063,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 440430521,
       'lat': 49.9437721,
       'lon': 11.5793449,
       'tags': {'amenity': 'biergarten',
        'name': 'Lamperium',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 440430580,
       'lat': 49.943517,
       'lon': 11.5782278,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 440659112,
       'lat': 49.4122025,
       'lon': 8.5301696,
       'tags': {'amenity': 'biergarten', 'note': 'Wasserskianlage'}},
      {'type': 'node',
       'id': 440693068,
       'lat': 50.0194409,
       'lon': 7.8251768,
       'tags': {'amenity': 'biergarten',
        'fee': 'yes',
        'name': 'Burgschänke Sooneck'}},
      {'type': 'node',
       'id': 440773782,
       'lat': 50.1219029,
       'lon': 6.9020557,
       'tags': {'amenity': 'biergarten', 'name': 'Lunner Hütte'}},
      {'type': 'node',
       'id': 440812766,
       'lat': 51.2582292,
       'lon': 12.5063252,
       'tags': {'amenity': 'biergarten', 'name': 'Büffeltränke'}},
      {'type': 'node',
       'id': 440991695,
       'lat': 51.0545026,
       'lon': 6.9951762,
       'tags': {'amenity': 'biergarten', 'name': 'Garten Schänke'}},
      {'type': 'node',
       'id': 441163962,
       'lat': 49.7524873,
       'lon': 8.4045118,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Giggel'}},
      {'type': 'node',
       'id': 441526993,
       'lat': 49.4941758,
       'lon': 10.4264093,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 441610148,
       'lat': 50.653712,
       'lon': 10.7740012,
       'tags': {'addr:city': 'Gehlberg',
        'addr:country': 'DE',
        'addr:postcode': '98559',
        'addr:street': 'Schmücke',
        'amenity': 'biergarten',
        'contact:email': 'info@schmuecke.biz',
        'contact:fax': '+49 36845 58830',
        'contact:phone': '+49 36845 5880',
        'contact:website': 'http://www.schmuecke.biz/',
        'cuisine': 'sausage',
        'name': 'Joel´s Biergarten',
        'operator': 'Waldhotel Schmücke',
        'source': 'http://www.schmuecke.biz/'}},
      {'type': 'node',
       'id': 441706524,
       'lat': 48.2011198,
       'lon': 11.6414649,
       'tags': {'amenity': 'biergarten', 'name': 'Restaurant Seegarten'}},
      {'type': 'node',
       'id': 442120475,
       'lat': 47.7287095,
       'lon': 10.3105036,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Stift',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes',
        'wheelchair:description': 'WC im Keller'}},
      {'type': 'node',
       'id': 442128854,
       'lat': 51.6342799,
       'lon': 6.6763383,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 442580486,
       'lat': 50.6211285,
       'lon': 7.0217526,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 442866308,
       'lat': 51.2660172,
       'lon': 14.4470425,
       'tags': {'amenity': 'biergarten', 'name': 'Los Bandidos'}},
      {'type': 'node',
       'id': 443112569,
       'lat': 47.9738286,
       'lon': 11.1837741,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Klostergasthof Andechs',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 443355643,
       'lat': 52.3706533,
       'lon': 9.7377455,
       'tags': {'amenity': 'biergarten', 'name': 'Schöne Aussichten 360°'}},
      {'type': 'node',
       'id': 443384030,
       'lat': 51.2712161,
       'lon': 7.113738,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 444343321,
       'lat': 48.411687,
       'lon': 10.0190562,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'italian',
        'name': 'BluBianco'}},
      {'type': 'node',
       'id': 444343322,
       'lat': 48.4123096,
       'lon': 10.0193078,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 444541976,
       'lat': 48.1751758,
       'lon': 11.5701627,
       'tags': {'addr:city': 'München',
        'addr:housenumber': '280b',
        'addr:street': 'Schleißheimer Straße',
        'amenity': 'biergarten',
        'name': 'Brunnergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 444880404,
       'lat': 49.091379,
       'lon': 8.271449,
       'tags': {'addr:city': 'Jockgrim',
        'addr:country': 'DE',
        'addr:housenumber': '5',
        'addr:postcode': '76751',
        'addr:street': 'Buchstraße',
        'amenity': 'biergarten',
        'microbrewery': 'yes',
        'name': "s'Fröschl",
        'opening_hours': 'Mo 18:00+; Tu-Fr 16:00+; Sa 18:00+; Su 17:00+',
        'website': 'http://www.froschl.de/'}},
      {'type': 'node',
       'id': 446096766,
       'lat': 47.8112371,
       'lon': 11.1320989,
       'tags': {'amenity': 'biergarten',
        'name': 'Alte Klosterwirtschaft',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 446221224,
       'lat': 50.0525623,
       'lon': 11.7953286,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 447952391,
       'lat': 48.4218324,
       'lon': 10.0386069,
       'tags': {'amenity': 'biergarten', 'name': 'Im Eile'}},
      {'type': 'node',
       'id': 448169138,
       'lat': 48.9099608,
       'lon': 11.8516342,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Schneider Kelheim',
        'name': 'Klösterl'}},
      {'type': 'node',
       'id': 448421092,
       'lat': 50.8688123,
       'lon': 7.2485937,
       'tags': {'amenity': 'biergarten', 'name': 'Treffpunkt'}},
      {'type': 'node',
       'id': 448424707,
       'lat': 49.7269128,
       'lon': 11.076091,
       'tags': {'addr:street': 'Liebessteig',
        'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Blümleins Keller',
        'tourism': 'attraction',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 448453911,
       'lat': 48.6244882,
       'lon': 9.3305694,
       'tags': {'amenity': 'biergarten', 'name': 'Neckar-Biergarten'}},
      {'type': 'node',
       'id': 448602276,
       'lat': 49.9940923,
       'lon': 11.6000834,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 448930103,
       'lat': 52.4083018,
       'lon': 13.0147492,
       'tags': {'amenity': 'biergarten',
        'name': 'Gartenlokal am Lindstedter Tor',
        'phone': '+49 (0)331 520688',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 449213932,
       'lat': 51.4991589,
       'lon': 11.9498153,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Freiberger',
        'indoor_seating': 'yes',
        'name': 'Felsenpavillon',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 449632097,
       'lat': 53.2113445,
       'lon': 8.0287693,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten Rabben'}},
      {'type': 'node',
       'id': 449754298,
       'lat': 51.7612868,
       'lon': 8.703786,
       'tags': {'amenity': 'biergarten', 'name': 'Stauterrassen'}},
      {'type': 'node',
       'id': 450194461,
       'lat': 47.59623,
       'lon': 11.0652304,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 450572757,
       'lat': 47.7913455,
       'lon': 11.3876177,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 451000620,
       'lat': 48.0277674,
       'lon': 11.0979544,
       'tags': {'addr:city': 'Utting am Ammersee',
        'addr:country': 'DE',
        'addr:housenumber': '5',
        'addr:postcode': '86919',
        'addr:street': 'Im Freizeitgelände',
        'amenity': 'biergarten',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 451003750,
       'lat': 49.9394367,
       'lon': 11.5531185,
       'tags': {'amenity': 'biergarten',
        'name': 'Glenks Biergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 451005104,
       'lat': 50.0471249,
       'lon': 10.8845166,
       'tags': {'amenity': 'biergarten', 'name': 'Zum goldenen Stern'}},
      {'type': 'node',
       'id': 451011915,
       'lat': 48.0289683,
       'lon': 11.0966711,
       'tags': {'amenity': 'biergarten',
        'contact:facebook': 'https://m.facebook.com/Fischmeisterei-1186717644797207/',
        'contact:phone': '+48 8806 9599399',
        'name': 'Fischmeisterei',
        'old_name': 'Die Veranda',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 451617088,
       'lat': 48.8952362,
       'lon': 9.1930583,
       'tags': {'amenity': 'biergarten',
        'name': 'Scala-Biergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 451709268,
       'lat': 50.2876755,
       'lon': 11.0302292,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Domäne Rödental',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 451722168,
       'lat': 54.3106801,
       'lon': 10.7960779,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 451733116,
       'lat': 48.645262,
       'lon': 13.6302312,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten, Cafe',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 451776356,
       'lat': 51.84654,
       'lon': 12.22296,
       'tags': {'amenity': 'biergarten', 'name': 'Ziebigker Eck'}},
      {'type': 'node',
       'id': 452402387,
       'lat': 49.2065539,
       'lon': 7.1019736,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 452572006,
       'lat': 47.6765899,
       'lon': 11.3038608,
       'tags': {'amenity': 'biergarten', 'name': 'Alpengasthof Zur Loisach'}},
      {'type': 'node',
       'id': 452585986,
       'lat': 50.9294083,
       'lon': 12.0186268,
       'tags': {'addr:city': 'Bad Köstritz',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '07586',
        'addr:street': 'Elsteraue',
        'amenity': 'biergarten',
        'brewery': 'Köstritzer',
        'name': 'Biergarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 452634092,
       'lat': 50.0870754,
       'lon': 11.0638995,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 452736428,
       'lat': 50.3485241,
       'lon': 7.5985916,
       'tags': {'amenity': 'biergarten',
        'name': "Pretzer's Biergarten",
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 453060636,
       'lat': 49.9887995,
       'lon': 7.8571794,
       'tags': {'addr:city': 'Trechtingshausen',
        'addr:country': 'DE',
        'addr:postcode': '55413',
        'addr:street': 'Schweizerhaus',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Schweizerhaus',
        'opening_hours': '"-17:00"',
        'phone': '+49 6721 6122'}},
      {'type': 'node',
       'id': 454249685,
       'lat': 47.6219866,
       'lon': 7.6257308,
       'tags': {'amenity': 'biergarten', 'name': 'Rebstübli', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 454353217,
       'lat': 48.2756143,
       'lon': 10.2289777,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 454411084,
       'lat': 52.2036623,
       'lon': 8.802155,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 454448454,
       'lat': 50.01307,
       'lon': 10.5752098,
       'tags': {'amenity': 'biergarten',
        'name': 'Bauer Roberts Brotzeitkeller und Biergarten'}},
      {'type': 'node',
       'id': 454527786,
       'lat': 49.5663518,
       'lon': 7.0631111,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 454981390,
       'lat': 48.7874714,
       'lon': 13.4601728,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 455168598,
       'lat': 47.7516195,
       'lon': 11.3740509,
       'tags': {'amenity': 'biergarten',
        'name': 'Antica Rimini',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 455226157,
       'lat': 49.5179817,
       'lon': 11.6644518,
       'tags': {'amenity': 'biergarten', 'name': 'Osterhöhle'}},
      {'type': 'node',
       'id': 455638207,
       'lat': 51.2620083,
       'lon': 10.004078,
       'tags': {'addr:city': 'Bad Sooden-Allendorf',
        'addr:housenumber': '52',
        'addr:postcode': '37242',
        'addr:street': 'Rothesteinstraße',
        'amenity': 'biergarten',
        'name': 'Fischerstübchen',
        'phone': '+49 05652-3751',
        'toilets:wheelchair': 'no',
        'website': 'http://fischerstuebchen.info/Fischerstuebchen.htm',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 456024788,
       'lat': 48.6180897,
       'lon': 13.4832899,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 456380569,
       'lat': 51.4315555,
       'lon': 6.9911116,
       'tags': {'amenity': 'biergarten',
        'name': 'Orangerie',
        'opening_hours': 'Mo-Su,PH 10:00-20:00+',
        'phone': '+49',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 456690134,
       'lat': 52.1943602,
       'lon': 8.782516,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 456786026,
       'lat': 49.9830446,
       'lon': 11.9053264,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 456786028,
       'lat': 49.9820131,
       'lon': 11.9092534,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 457317805,
       'lat': 49.9718865,
       'lon': 11.9344276,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 457607872,
       'lat': 50.1556514,
       'lon': 7.5566692,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten am ZAP',
        'opening_hours': 'Mo-Fr 16:30+, Sa,Su 15:00+',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 457951563,
       'lat': 50.9981827,
       'lon': 11.0089004,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 458371168,
       'lat': 49.180377,
       'lon': 11.9902206,
       'tags': {'amenity': 'biergarten', 'name': 'Skt. Georgimühle'}},
      {'type': 'node',
       'id': 458714883,
       'lat': 50.8965746,
       'lon': 6.6802109,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthaus Schweitzer'}},
      {'type': 'node',
       'id': 458772892,
       'lat': 48.8123274,
       'lon': 11.8444596,
       'tags': {'addr:city': 'Abensberg',
        'addr:country': 'DE',
        'addr:housenumber': '23',
        'addr:postcode': '93326',
        'addr:street': 'Münchener Straße',
        'amenity': 'biergarten',
        'name': 'Weißbierstadl',
        'phone': '+49 9443 2165',
        'website': 'http://www.weissbierstadel.de'}},
      {'type': 'node',
       'id': 458775112,
       'lat': 49.9254018,
       'lon': 10.6652105,
       'tags': {'amenity': 'biergarten', 'name': 'Roppelts Keller'}},
      {'type': 'node',
       'id': 459155880,
       'lat': 50.0617871,
       'lon': 10.9656816,
       'tags': {'amenity': 'biergarten',
        'name': 'Engelhardts-Keller',
        'opening_hours': 'Mo-Sa 16:00+; Su,PH 10:00+',
        'phone': '+49 9573 1543'}},
      {'type': 'node',
       'id': 459175696,
       'lat': 53.2805091,
       'lon': 12.9737387,
       'tags': {'addr:city': 'Wesenberg',
        'addr:country': 'DE',
        'addr:housenumber': '7',
        'addr:postcode': '17255',
        'addr:street': 'Vor dem Mühlentor',
        'amenity': 'biergarten',
        'contact:website': 'http://www.altes-hospital.de/',
        'name': 'Biergarten am Hafen',
        'opening_hours': 'Apr-Oct 11:00-22:00',
        'source': 'http://www.altes-hospital.de/'}},
      {'type': 'node',
       'id': 459667668,
       'lat': 47.6571101,
       'lon': 9.1809,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Sea Life Centre',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes',
        'wheelchair:description': 'Barrierefrei zu erreichen. Genügend Platz zum manövrieren.'}},
      {'type': 'node',
       'id': 459946987,
       'lat': 50.076012,
       'lon': 11.5736795,
       'tags': {'amenity': 'biergarten', 'name': 'Schlömener Tränke'}},
      {'type': 'node',
       'id': 460365390,
       'lat': 49.0756833,
       'lon': 12.7155855,
       'tags': {'amenity': 'biergarten', 'name': 'Brauerei Gasthof Haid'}},
      {'type': 'node',
       'id': 460387307,
       'lat': 47.6128597,
       'lon': 9.593963,
       'tags': {'amenity': 'biergarten', 'name': 'Weinrädle Rottmar'}},
      {'type': 'node',
       'id': 463217490,
       'lat': 49.7035065,
       'lon': 10.2629572,
       'tags': {'amenity': 'biergarten',
        'name': 'Weingut Weigand',
        'shop': 'alcohol'}},
      {'type': 'node',
       'id': 463218152,
       'lat': 47.5819247,
       'lon': 10.9273814,
       'tags': {'amenity': 'biergarten',
        'name': 'Brunnenkopfhaus',
        'phone': '0175/6540155'}},
      {'type': 'node',
       'id': 466517530,
       'lat': 50.0809019,
       'lon': 10.414699,
       'tags': {'amenity': 'biergarten', 'name': 'Wässernachtal'}},
      {'type': 'node',
       'id': 467557826,
       'lat': 50.5554122,
       'lon': 8.7223477,
       'tags': {'amenity': 'biergarten',
        'name': 'Schiffenberg',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 469117365,
       'lat': 51.4691997,
       'lon': 7.0903008,
       'tags': {'amenity': 'biergarten',
        'name': 'Minigolf Volksgarten',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 469169391,
       'lat': 49.6606147,
       'lon': 8.7700387,
       'tags': {'amenity': 'biergarten', 'name': 'Eselsmühle'}},
      {'type': 'node',
       'id': 469264062,
       'lat': 49.4629812,
       'lon': 12.2260397,
       'tags': {'amenity': 'biergarten', 'name': 'Beim Wirt'}},
      {'type': 'node',
       'id': 469317467,
       'lat': 50.1100929,
       'lon': 11.1150882,
       'tags': {'amenity': 'biergarten', 'name': 'Klosterhof'}},
      {'type': 'node',
       'id': 469322582,
       'lat': 48.810306,
       'lon': 11.7658808,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Turm'}},
      {'type': 'node',
       'id': 469344012,
       'lat': 53.6196805,
       'lon': 10.8755668,
       'tags': {'amenity': 'biergarten',
        'name': 'Bier- und Kaffeegarten',
        'operator': 'Gasthof am See'}},
      {'type': 'node',
       'id': 469641568,
       'lat': 48.8168962,
       'lon': 11.7487336,
       'tags': {'amenity': 'biergarten',
        'name': 'Radlereck',
        'opening_hours': 'Mo-Su 15:00+'}},
      {'type': 'node',
       'id': 469672129,
       'lat': 52.3643657,
       'lon': 9.7364679,
       'tags': {'alt_name': 'Lorettas',
        'amenity': 'biergarten',
        'name': "Loretta's"}},
      {'type': 'node',
       'id': 469709502,
       'lat': 48.1887066,
       'lon': 11.0530128,
       'tags': {'amenity': 'biergarten', 'name': 'Drexl'}},
      {'type': 'node',
       'id': 470020406,
       'lat': 49.2715663,
       'lon': 7.1533853,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 471286963,
       'lat': 48.7759849,
       'lon': 9.1819957,
       'tags': {'amenity': 'biergarten',
        'name': 'Amadeus',
        'toilets:wheelchair': 'no'}},
      {'type': 'node',
       'id': 471485228,
       'lat': 48.8291852,
       'lon': 9.0670442,
       'tags': {'amenity': 'biergarten',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 471634463,
       'lat': 49.2038534,
       'lon': 12.1045087,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Zum Gockelwirt'}},
      {'type': 'node',
       'id': 471989738,
       'lat': 48.4514116,
       'lon': 8.8564811,
       'tags': {'addr:city': 'Rottenburg am Neckar',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:postcode': '72108',
        'addr:street': 'Neckartalstraße',
        'amenity': 'biergarten',
        'contact:website': 'http://www.backhaus-bieringen.de/',
        'name': 'Backhaus Bieringen',
        'opening_hours': 'Mo,We 06:30-13:00; Tu-Fr 06:30-12:30,14:30-18:00; Sa 05:30-12:30; Su 07:30-11:00,14:00-17:00',
        'shop': 'bakery'}},
      {'type': 'node',
       'id': 472082101,
       'lat': 49.2019883,
       'lon': 12.0420105,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Kare',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 472277460,
       'lat': 49.6494499,
       'lon': 7.1714373,
       'tags': {'amenity': 'biergarten', 'name': 'Alt Birkenfeld'}},
      {'type': 'node',
       'id': 472351020,
       'lat': 48.224385,
       'lon': 10.3791861,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 472376758,
       'lat': 49.7566256,
       'lon': 10.9496553,
       'tags': {'addr:city': 'Hallerndorf',
        'addr:country': 'DE',
        'addr:postcode': '91352',
        'addr:street': 'Stiebarlimbach',
        'amenity': 'biergarten',
        'fax': '+49 (9195) 4383',
        'name': "Roppelt's Keller",
        'operator': 'Brauerei Roppelt',
        'phone': '+49 (9195) 7263',
        'toilets:wheelchair': 'yes',
        'tourism': 'attraction',
        'website': 'http://brauerei-roppelt.de/bierkeller/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 472650277,
       'lat': 48.9528518,
       'lon': 9.0218808,
       'tags': {'amenity': 'biergarten', 'name': 'Kleintierzuchtverein Sersheim'}},
      {'type': 'node',
       'id': 473140672,
       'lat': 50.0501067,
       'lon': 11.6742566,
       'tags': {'amenity': 'biergarten', 'name': 'Teufels Biergarten'}},
      {'type': 'node',
       'id': 473518855,
       'lat': 51.3583814,
       'lon': 6.6500464,
       'tags': {'addr:housename': 'Innenhof Dujardin',
        'addr:housenumber': '9',
        'addr:postcode': '47829',
        'addr:street': 'Dujardinstraße',
        'amenity': 'biergarten',
        'cuisine': 'bavarian',
        'name': 'Biergarten Küferei',
        'website': 'http://www.weinbrennerei-dujardin.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 473733384,
       'lat': 52.5055232,
       'lon': 7.1971027,
       'tags': {'amenity': 'biergarten', 'name': 'Playa de Lohne'}},
      {'type': 'node',
       'id': 473854044,
       'lat': 48.9318285,
       'lon': 9.0342977,
       'tags': {'amenity': 'biergarten',
        'name': 'Radlertankstelle',
        'opening_hours': 'Mo-Fr off'}},
      {'type': 'node',
       'id': 474360699,
       'lat': 50.9746484,
       'lon': 11.6500869,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 475243882,
       'lat': 53.2436314,
       'lon': 8.6778811,
       'tags': {'amenity': 'biergarten',
        'horse': 'yes',
        'name': 'Tanneck - Minigolfanlage'}},
      {'type': 'node',
       'id': 475398849,
       'lat': 48.5987861,
       'lon': 10.8668541,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Floß'}},
      {'type': 'node',
       'id': 475547958,
       'lat': 50.8925215,
       'lon': 6.9330099,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 476819388,
       'lat': 48.0505922,
       'lon': 8.9702591,
       'tags': {'amenity': 'biergarten',
        'name': 'Hotel-Cafe Pelikan',
        'tourism': 'hotel'}},
      {'type': 'node',
       'id': 477322147,
       'lat': 50.711513,
       'lon': 13.4665856,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 477341293,
       'lat': 50.0722865,
       'lon': 11.5458398,
       'tags': {'addr:city': 'Trebgast',
        'addr:country': 'DE',
        'addr:housenumber': '31',
        'addr:postcode': '95367',
        'addr:street': 'Bergstraße',
        'amenity': 'biergarten',
        'email': 'info@brauerei-haberstumpf.de',
        'fax': '+49 (9227) 2273',
        'microbrewery': 'yes',
        'name': 'Brauerei Haberstumpf',
        'opening_hours': 'Mo-Fr 07:00-18:00; Sa 08:00-13:00',
        'phone': '+49 9227 351',
        'start_date': '1531',
        'website': 'http://www.brauerei-haberstumpf.de'}},
      {'type': 'node',
       'id': 479231543,
       'lat': 51.4902896,
       'lon': 7.4428066,
       'tags': {'amenity': 'biergarten', 'name': 'Helenenberg'}},
      {'type': 'node',
       'id': 479944363,
       'lat': 50.1970605,
       'lon': 11.5666293,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 480062756,
       'lat': 53.3275298,
       'lon': 8.4814172,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 480348465,
       'lat': 50.1971395,
       'lon': 6.8304927,
       'tags': {'amenity': 'biergarten',
        'building': 'yes',
        'name': 'Burghof',
        'opening_hours': 'We-Su,Mo 11:00+',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 480638033,
       'lat': 48.2437627,
       'lon': 10.370764,
       'tags': {'addr:city': 'Krumbach',
        'addr:country': 'DE',
        'addr:postcode': '86381',
        'amenity': 'biergarten',
        'name': 'Gasthof Munding',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 483444195,
       'lat': 51.2369793,
       'lon': 6.7704669,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten Rheinterasse',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 484196841,
       'lat': 47.5969042,
       'lon': 11.0710995,
       'tags': {'amenity': 'biergarten', 'name': 'Mühlbart´l'}},
      {'type': 'node',
       'id': 485119646,
       'lat': 49.7784929,
       'lon': 8.9896917,
       'tags': {'amenity': 'biergarten',
        'description': 'Vermutlich nur Getränke und Eis',
        'fixme': 'noch existent? Sah im späten April 2018 nicht sehr lebendig aus. Bitte im Hochsommer besichtigen und auch die Monate bei opening_hours angeben!',
        'name': 'Paradies-Biergarten',
        'opening_hours': 'Tu-Su 15:00-05:00'}},
      {'type': 'node',
       'id': 486074070,
       'lat': 50.3907552,
       'lon': 8.9788413,
       'tags': {'addr:city': 'Nidda',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:postcode': '63667',
        'addr:street': 'Im Orbes',
        'addr:suburb': 'Wallernhausen',
        'amenity': 'biergarten',
        'email': 'Postmaster@orbes.de',
        'fax': '+49 6043 4860',
        'name': 'Im Orbes',
        'operator': 'Manfred Lehnert',
        'phone': '+49 6043 7282',
        'source': 'http://www.orbes.de/',
        'source:date': '2016-03-07',
        'website': 'http://www.orbes.de/'}},
      {'type': 'node',
       'id': 488348512,
       'lat': 51.0095899,
       'lon': 13.8615464,
       'tags': {'addr:city': 'Dresden',
        'addr:country': 'DE',
        'addr:housenumber': '71b',
        'addr:postcode': '01259',
        'addr:street': 'Berthold-Haupt-Straße',
        'amenity': 'biergarten',
        'name': 'Elbidyll'}},
      {'type': 'node',
       'id': 488368737,
       'lat': 48.1708605,
       'lon': 11.5141045,
       'tags': {'amenity': 'biergarten', 'name': 'Kleingartenkolonie'}},
      {'type': 'node',
       'id': 489205204,
       'lat': 47.7226971,
       'lon': 10.3206859,
       'tags': {'amenity': 'biergarten',
        'brewery': 'Schäffler Bräu',
        'name': 'Burghalde Biergarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 492022191,
       'lat': 52.618156,
       'lon': 13.335382,
       'tags': {'amenity': 'biergarten',
        'name': 'Freibad Lübars',
        'website': 'http://www.strandbad-luebars.de/'}},
      {'type': 'node',
       'id': 492819586,
       'lat': 53.3872944,
       'lon': 12.3225542,
       'tags': {'amenity': 'biergarten', 'name': 'Fischerhütte'}},
      {'type': 'node',
       'id': 493735227,
       'lat': 48.6238898,
       'lon': 12.2135081,
       'tags': {'amenity': 'biergarten', 'name': 'Wolfgangsberg'}},
      {'type': 'node',
       'id': 494616179,
       'lat': 48.6888629,
       'lon': 9.4235326,
       'tags': {'addr:city': 'Wernau (Neckar)',
        'addr:country': 'DE',
        'addr:housenumber': '124',
        'addr:postcode': '73249',
        'addr:street': 'Kirchheimer Straße',
        'amenity': 'biergarten',
        'name': 'Bruzzel-Stüble'}},
      {'type': 'node',
       'id': 495038661,
       'lat': 48.2474064,
       'lon': 10.4497517,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 495404143,
       'lat': 50.282349,
       'lon': 12.0116184,
       'tags': {'amenity': 'biergarten', 'name': 'Erbschänke'}},
      {'type': 'node',
       'id': 496923895,
       'lat': 48.0941549,
       'lon': 11.6249683,
       'tags': {'amenity': 'biergarten',
        'name': 'Forschungsbrauerei',
        'opening_hours': 'Mo-Sa 11:00-23:00; Su,PH 11:00-22:00',
        'wheelchair': 'limited',
        'wikidata': 'Q1438023'}},
      {'type': 'node',
       'id': 498562238,
       'lat': 50.0998598,
       'lon': 8.6901957,
       'tags': {'amenity': 'biergarten',
        'cuisine': 'regional',
        'name': 'Schreiber Heyne'}},
      {'type': 'node',
       'id': 498841522,
       'lat': 50.1014237,
       'lon': 9.2633658,
       'tags': {'addr:city': 'Kleinkahl',
        'addr:housenumber': '8',
        'addr:postcode': '63828',
        'addr:street': 'Großlaudenbacher Straße',
        'amenity': 'biergarten',
        'name': 'Käslies'}},
      {'type': 'node',
       'id': 499994318,
       'lat': 48.9598817,
       'lon': 11.6843383,
       'tags': {'addr:city': 'Riedenburg',
        'addr:housenumber': '18',
        'addr:postcode': '93339',
        'addr:street': 'An der Altmühl',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'email': 'fuchs-riedenburg@t-online.de',
        'fax': '+49 9442 1312',
        'name': 'Fuchsgarten',
        'operator': 'Josef Fuchs',
        'phone': '+49 9442 1312',
        'source': 'http://www.fuchsgarten.de/',
        'source:date': '2016-06-17',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.fuchsgarten.de/',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 500727782,
       'lat': 48.2455966,
       'lon': 12.0916345,
       'tags': {'amenity': 'biergarten', 'name': 'Holzwirt'}},
      {'type': 'node',
       'id': 500866117,
       'lat': 54.399344,
       'lon': 13.609084,
       'tags': {'amenity': 'biergarten', 'name': 'Schmachter Hus'}},
      {'type': 'node',
       'id': 502306653,
       'lat': 51.4521326,
       'lon': 9.1125773,
       'tags': {'amenity': 'biergarten', 'name': 'Zur Twiste'}},
      {'type': 'node',
       'id': 502535141,
       'lat': 47.9175743,
       'lon': 7.6951367,
       'tags': {'amenity': 'biergarten',
        'name': 'Kiosk am Kurpark',
        'phone': '+49 7633 939234',
        'shop': 'kiosk'}},
      {'type': 'node',
       'id': 503404690,
       'lat': 49.7214579,
       'lon': 10.9230579,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthaus Utz'}},
      {'type': 'node',
       'id': 503503831,
       'lat': 51.2133279,
       'lon': 7.0839055,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 504915787,
       'lat': 49.7117213,
       'lon': 9.548225,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 505200184,
       'lat': 50.5151856,
       'lon': 7.0360224,
       'tags': {'amenity': 'biergarten', 'name': 'Am Herrenberg'}},
      {'type': 'node',
       'id': 505204795,
       'lat': 49.912988,
       'lon': 10.7519196,
       'tags': {'amenity': 'biergarten',
        'name': 'Brauerei Kundmüller',
        'wikidata': 'Q900290',
        'wikipedia': 'de:Brauerei Kundmüller'}},
      {'type': 'node',
       'id': 505274697,
       'lat': 51.7033284,
       'lon': 6.4166268,
       'tags': {'addr:city': 'Xanten',
        'addr:housenumber': '5',
        'addr:postcode': '46509',
        'addr:street': 'Alt-Vynscher-Weg',
        'addr:suburb': 'Vynen',
        'amenity': 'biergarten',
        'internet_access': 'wlan',
        'internet_access:fee': 'no',
        'name': 'Pier 5',
        'phone': '+49 (0) 2801 715656',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes',
        'wheelchair:description': 'Separates Sanitärgebäude'}},
      {'type': 'node',
       'id': 506887326,
       'lat': 51.3428191,
       'lon': 9.4302086,
       'tags': {'amenity': 'biergarten', 'name': 'Daspel-Stube'}},
      {'type': 'node',
       'id': 511130071,
       'lat': 48.779438,
       'lon': 9.2243824,
       'tags': {'FIXME': 'name', 'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 513059995,
       'lat': 47.5385325,
       'lon': 10.7762723,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 513853716,
       'lat': 51.8382723,
       'lon': 12.7836814,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 513853718,
       'lat': 51.8516939,
       'lon': 12.7234257,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 514767390,
       'lat': 50.1968481,
       'lon': 8.0530125,
       'tags': {'amenity': 'biergarten', 'name': 'Landgasthof Wiesenmühle'}},
      {'type': 'node',
       'id': 514885549,
       'lat': 49.5386014,
       'lon': 12.1475986,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthof Sperl',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 517227778,
       'lat': 47.5593873,
       'lon': 10.7780637,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 518803221,
       'lat': 50.5130098,
       'lon': 7.0366962,
       'tags': {'amenity': 'biergarten', 'name': 'Zum alten Pfarrhaus'}},
      {'type': 'node',
       'id': 519948254,
       'lat': 49.7291432,
       'lon': 10.5711681,
       'tags': {'amenity': 'biergarten', 'name': 'Bierkeller "Zum Hopfengarten"'}},
      {'type': 'node',
       'id': 520401258,
       'lat': 52.5235131,
       'lon': 11.3953699,
       'tags': {'amenity': 'biergarten',
        'name': 'Lindenhofgarten',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 521992915,
       'lat': 49.6545463,
       'lon': 8.9294949,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Deutschen Kaiser'}},
      {'type': 'node',
       'id': 522638338,
       'lat': 50.9150524,
       'lon': 6.9137303,
       'tags': {'amenity': 'biergarten', 'name': 'Em Birkenbäumche'}},
      {'type': 'node',
       'id': 523274354,
       'lat': 47.9931269,
       'lon': 11.8981128,
       'tags': {'amenity': 'biergarten', 'opening_hours': 'Sa, Su, PH 11:00+'}},
      {'type': 'node',
       'id': 524274733,
       'lat': 47.4696251,
       'lon': 11.2927466,
       'tags': {'amenity': 'biergarten', 'name': 'Aschauer Alm'}},
      {'type': 'node',
       'id': 524559784,
       'lat': 53.2763606,
       'lon': 11.3662735,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 526046321,
       'lat': 47.9827617,
       'lon': 7.8758317,
       'tags': {'amenity': 'biergarten',
        'name': 'Waldsee',
        'phone': '+49 (0)761 73688',
        'toilets:wheelchair': 'yes',
        'website': 'http://www.waldsee-freiburg.de',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 526133711,
       'lat': 50.0917669,
       'lon': 10.7960304,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 528610219,
       'lat': 49.2616035,
       'lon': 9.5774923,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 529953156,
       'lat': 50.0332947,
       'lon': 9.041785,
       'tags': {'amenity': 'biergarten',
        'name': 'Angelsportheim Dettingen',
        'toilets:wheelchair': 'no',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 533978073,
       'lat': 50.7678585,
       'lon': 12.3525336,
       'tags': {'amenity': 'biergarten',
        'name': 'Biergarten zum Gartenrestaurant'}},
      {'type': 'node',
       'id': 534372422,
       'lat': 49.1279402,
       'lon': 10.8626062,
       'tags': {'amenity': 'biergarten', 'name': 'Waldschänke'}},
      {'type': 'node',
       'id': 538156433,
       'lat': 48.2909715,
       'lon': 10.6573765,
       'tags': {'amenity': 'biergarten',
        'name': 'Gasthof zur Traube',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 538345212,
       'lat': 48.7627573,
       'lon': 11.5252855,
       'tags': {'addr:housenumber': '10',
        'addr:street': 'Am Sportplatz',
        'amenity': 'biergarten',
        'name': "Mehringer Stub'n",
        'phone': '+49 8407 263',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 538902043,
       'lat': 51.0561599,
       'lon': 7.8317876,
       'tags': {'amenity': 'biergarten',
        'name': 'Zum Stadl',
        'website': 'http://www.zum-stadl-eichhagen.de/'}},
      {'type': 'node',
       'id': 539501840,
       'lat': 52.3132146,
       'lon': 10.4892513,
       'tags': {'amenity': 'biergarten', 'name': 'Hafenflair'}},
      {'type': 'node',
       'id': 540149282,
       'lat': 50.0511261,
       'lon': 8.1231825,
       'tags': {'amenity': 'biergarten',
        'name': 'Wein- und Schlemmerstand Martinsthal',
        'toilets:wheelchair': 'yes',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 540279851,
       'lat': 51.762679,
       'lon': 11.795239,
       'tags': {'amenity': 'biergarten', 'name': 'Sportlerheim'}},
      {'type': 'node',
       'id': 540370192,
       'lat': 50.1513591,
       'lon': 8.7332814,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 540903768,
       'lat': 48.6272679,
       'lon': 12.3559308,
       'tags': {'amenity': 'biergarten', 'name': 'Biergarten WL'}},
      {'type': 'node',
       'id': 540924169,
       'lat': 50.0395422,
       'lon': 8.1928338,
       'tags': {'amenity': 'biergarten',
        'name': 'Yachtcafé',
        'toilets:wheelchair': 'no',
        'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 540960388,
       'lat': 48.0947749,
       'lon': 11.5158975,
       'tags': {'addr:city': 'München',
        'addr:country': 'DE',
        'addr:housenumber': '149',
        'addr:postcode': '81379',
        'addr:street': 'Kistlerhofstraße',
        'amenity': 'biergarten',
        'cuisine': 'german',
        'name': 'Holiday Inn Biergarten'}},
      {'type': 'node',
       'id': 541020184,
       'lat': 48.6107087,
       'lon': 10.9501591,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Beckerwirt'}},
      {'type': 'node',
       'id': 544054183,
       'lat': 48.0247906,
       'lon': 9.7875761,
       'tags': {'amenity': 'biergarten', 'name': 'Grüner Baum'}},
      {'type': 'node',
       'id': 544248680,
       'lat': 48.7905942,
       'lon': 8.235069,
       'tags': {'amenity': 'biergarten', 'name': 'Reitertränke Biergarten'}},
      {'type': 'node',
       'id': 549332284,
       'lat': 50.2027794,
       'lon': 8.5791835,
       'tags': {'addr:city': 'Oberursel (Taunus)',
        'addr:country': 'DE',
        'addr:housenumber': '13',
        'addr:postcode': '61440',
        'addr:street': 'Ackergasse',
        'amenity': 'biergarten',
        'cuisine': 'regional',
        'email': 'info@meinbier.de',
        'fax': '+49 6171 56900',
        'name': 'Alt Oberurseler Brauhaus',
        'opening_hours': 'Mo-Th 11:00-24:00, Fr,Sa 11:00-01:00, Su 10:00-23:00',
        'operator': 'Thomas Studanski',
        'phone': '+49 6171 54370',
        'source': 'Bing',
        'website': 'http://www.meinbier.de/',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 550079441,
       'lat': 48.021528,
       'lon': 11.9078631,
       'tags': {'amenity': 'biergarten', 'name': "Beim Wirt z'Bruck"}},
      {'type': 'node',
       'id': 552802043,
       'lat': 47.4166636,
       'lon': 10.2915123,
       'tags': {'amenity': 'biergarten', 'source': 'survey'}},
      {'type': 'node',
       'id': 553026538,
       'lat': 50.063464,
       'lon': 9.01517,
       'tags': {'amenity': 'biergarten',
        'name': 'Gaststätte Schützenhaus',
        'opening_hours': 'Tu-Sa 17:00-01:00, Su 09:30-14:00,17:00-23:00',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 558858004,
       'lat': 52.4883525,
       'lon': 13.3736102,
       'tags': {'addr:city': 'Berlin',
        'addr:country': 'DE',
        'addr:housenumber': '42',
        'addr:postcode': '10965',
        'addr:street': 'Kreuzbergstraße',
        'addr:suburb': 'Schöneberg',
        'amenity': 'biergarten',
        'name': 'Kurhaus Ponte Rosa'}},
      {'type': 'node',
       'id': 558876034,
       'lat': 48.8575956,
       'lon': 8.2104597,
       'tags': {'addr:city': 'Rastatt',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '76437',
        'addr:street': 'Rauentaler Straße',
        'amenity': 'biergarten',
        'name': 'Zum Franz'}},
      {'type': 'node',
       'id': 559278578,
       'lat': 48.1580695,
       'lon': 10.8313942,
       'tags': {'amenity': 'biergarten',
        'name': 'Gaststätte Grüner Baum',
        'toilets:wheelchair': 'no',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 559643078,
       'lat': 51.0078023,
       'lon': 9.7263831,
       'tags': {'addr:city': 'Rotenburg an der Fulda',
        'addr:country': 'DE',
        'addr:postcode': '36199',
        'amenity': 'biergarten',
        'name': 'Rodenberg Die Alm',
        'opening_hours': 'Sa,Su 11:00+'}},
      {'type': 'node',
       'id': 559649696,
       'lat': 50.9105565,
       'lon': 12.4415513,
       'tags': {'amenity': 'biergarten', 'name': 'Zur Linde'}},
      {'type': 'node',
       'id': 560133519,
       'lat': 50.5437935,
       'lon': 7.5990709,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 560670087,
       'lat': 49.4404853,
       'lon': 10.3102269,
       'tags': {'addr:city': 'Burgbernheim',
        'addr:country': 'DE',
        'addr:postcode': '91593',
        'addr:street': 'Felsenkellerstraße',
        'amenity': 'biergarten',
        'name': 'Langskeller',
        'operator': 'Metzgerei Häßlein',
        'phone': '+49-9843-95920',
        'website': 'http://www.langskeller-biergarten.de'}},
      {'type': 'node',
       'id': 561110617,
       'lat': 52.1803085,
       'lon': 8.5151273,
       'tags': {'amenity': 'biergarten', 'name': 'Irrlicht'}},
      {'type': 'node',
       'id': 561229979,
       'lat': 52.0826311,
       'lon': 7.5873777,
       'tags': {'amenity': 'biergarten', 'wheelchair': 'yes'}},
      {'type': 'node',
       'id': 562641426,
       'lat': 48.3607577,
       'lon': 10.829988,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 563744099,
       'lat': 47.735343,
       'lon': 9.6053754,
       'tags': {'amenity': 'biergarten', 'name': 'Zur Linde'}},
      {'type': 'node',
       'id': 563834068,
       'lat': 47.4838046,
       'lon': 10.3404985,
       'tags': {'addr:city': 'Sonthofen',
        'addr:country': 'DE',
        'addr:postcode': '87527',
        'addr:street': 'Auf dem Strausberg',
        'amenity': 'biergarten',
        'capacity': '10',
        'name': 'Naturfreundehaus Michael-Schuster-Hütte',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'N 088',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'chalet',
        'website': 'https://www.naturfreunde-sonthofen.de'}},
      {'type': 'node',
       'id': 563834160,
       'lat': 48.2553674,
       'lon': 8.267028,
       'tags': {'addr:city': 'Wolfach',
        'addr:country': 'DE',
        'addr:housenumber': '1',
        'addr:postcode': '77709',
        'addr:street': 'Sommerecke',
        'addr:suburb': 'Kirnbach',
        'amenity': 'biergarten',
        'capacity': '50',
        'name': 'Naturfreundehaus Sommerecke',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'M 056',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'hostel'}},
      {'type': 'node',
       'id': 563834166,
       'lat': 49.1784058,
       'lon': 7.6271613,
       'tags': {'FIXME': 'Bitte nicht löschen; siehe http://wiki.openstreetmap.org/index.php?title=DE:Naturfreundehäuser',
        'addr:city': 'Pirmasens',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '66955',
        'addr:street': 'Horbachhalde',
        'amenity': 'biergarten',
        'capacity': '6',
        'name': 'Naturfreundehaus Horbach',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'K 024',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'hostel'}},
      {'type': 'node',
       'id': 563834219,
       'lat': 49.6970751,
       'lon': 7.3244004,
       'tags': {'FIXME': 'Bitte nicht löschen; siehe http://wiki.openstreetmap.org/index.php?title=DE:Naturfreundehäuser',
        'addr:city': 'Idar-Oberstein',
        'addr:country': 'DE',
        'addr:housenumber': '25',
        'addr:postcode': '55743',
        'addr:street': 'Alte Treibe',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Alte Treibe',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'K 005',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'hostel'}},
      {'type': 'node',
       'id': 563834221,
       'lat': 49.4028575,
       'lon': 8.423241,
       'tags': {'addr:city': 'Neuhofen',
        'addr:country': 'DE',
        'addr:postcode': '67141',
        'addr:street': 'Bachstadenweg',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Im Woog',
        'opening_hours': 'Sa-Su',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'K 036',
        'source': 'Datenspende der NaturFreunde Deutschland'}},
      {'type': 'node',
       'id': 563834261,
       'lat': 48.2192651,
       'lon': 9.0399102,
       'tags': {'addr:city': 'Albstadt',
        'addr:country': 'DE',
        'addr:housenumber': '2',
        'addr:postcode': '72458',
        'addr:street': 'Am Waldheim',
        'addr:suburb': 'Ebingen',
        'amenity': 'biergarten',
        'capacity': '10',
        'name': 'Naturfreundehaus Richard-Joner-Heim',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'M 050',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'chalet'}},
      {'type': 'node',
       'id': 563834319,
       'lat': 48.9695468,
       'lon': 8.7997667,
       'tags': {'addr:city': 'Ötisheim',
        'addr:country': 'DE',
        'addr:housenumber': '100',
        'addr:postcode': '75443',
        'addr:street': 'Maulbronner Straße',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Kohlplattenhaus',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'L 055',
        'source': 'Datenspende der NaturFreunde Deutschland'}},
      {'type': 'node',
       'id': 563834338,
       'lat': 48.6791537,
       'lon': 9.7681855,
       'tags': {'addr:city': 'Süßen',
        'addr:country': 'DE',
        'addr:housenumber': '4',
        'addr:postcode': '73079',
        'addr:street': 'An der Lauter',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus An der Lauter',
        'opening_hours': 'We,Sa 15:00-19:00; Su 09:00-12:00',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'M 009',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'website': 'https://www.naturfreunde.de/haus/naturfreundehaus-der-lauter'}},
      {'type': 'node',
       'id': 563834346,
       'lat': 49.0649986,
       'lon': 9.3305716,
       'tags': {'addr:city': 'Beilstein',
        'addr:country': 'DE',
        'addr:postcode': '71717',
        'addr:suburb': 'Gagernberg',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus St. Annasee-Haus',
        'opening_hours': 'Su',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'M 012',
        'source': 'Datenspende der NaturFreunde Deutschland'}},
      {'type': 'node',
       'id': 563834397,
       'lat': 48.526037,
       'lon': 10.8691566,
       'tags': {'addr:city': 'Meitingen',
        'addr:country': 'DE',
        'addr:housenumber': '34',
        'addr:postcode': '86405',
        'addr:street': 'Fischerweg',
        'addr:suburb': 'Herbertshofen',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Vinzenz-Behr-Hütte',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'N 078',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'hostel',
        'website': 'http://www.naturfreunde-augsburg.com/homepaged.htm'}},
      {'type': 'node',
       'id': 563834467,
       'lat': 50.1847585,
       'lon': 9.0631173,
       'tags': {'FIXME': 'Bitte nicht löschen; siehe http://wiki.openstreetmap.org/index.php?title=DE:Naturfreundehäuser',
        'amenity': 'biergarten',
        'capacity': '29',
        'name': 'Naturfreundehaus Wingertskippel',
        'opening_hours': 'Su 9:00-17:00',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'H 017',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'chalet',
        'wheelchair': 'limited'}},
      {'type': 'node',
       'id': 563834491,
       'lat': 50.2700855,
       'lon': 10.8832783,
       'tags': {'FIXME': 'Bitte nicht löschen; siehe http://wiki.openstreetmap.org/index.php?title=DE:Naturfreundehäuser',
        'addr:city': 'Weitramsdorf',
        'addr:country': 'DE',
        'addr:postcode': '96479',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus An den Hofmannsteichen',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'N 016',
        'source': 'Datenspende der NaturFreunde Deutschland',
        'tourism': 'chalet'}},
      {'type': 'node',
       'id': 563834737,
       'lat': 50.2348995,
       'lon': 11.5714805,
       'tags': {'addr:city': 'Presseck',
        'addr:country': 'DE',
        'addr:postcode': '95355',
        'addr:street': 'Schnebes',
        'amenity': 'biergarten',
        'name': 'Naturfreundehaus Jakob-Spindler-Hütte',
        'note': 'wenig Info im NFH-Verzeichnis',
        'operator': 'NaturFreunde Deutschland',
        'ref': 'N 113',
        'source': 'Datenspende der NaturFreunde Deutschland'}},
      {'type': 'node',
       'id': 564614133,
       'lat': 53.6320517,
       'lon': 11.3832577,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Südufer'}},
      {'type': 'node',
       'id': 566808403,
       'lat': 48.18191,
       'lon': 11.570473,
       'tags': {'amenity': 'biergarten',
        'created_by': 'iLOE 1.6',
        'name': 'Blücher',
        'wheelchair': 'no'}},
      {'type': 'node',
       'id': 567145312,
       'lat': 49.7613924,
       'lon': 9.5131162,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 568122951,
       'lat': 49.5621668,
       'lon': 10.5904494,
       'tags': {'amenity': 'biergarten',
        'name': 'Stöckacher Mühle',
        'opening_hours': 'Mo 17:00-22:00;We-Th 17:00-22:00;Fr-Sa 17:00-23:00;Su 11:00-22:00;Tu off'}},
      {'type': 'node',
       'id': 569091631,
       'lat': 50.4930775,
       'lon': 6.6319421,
       'tags': {'amenity': 'biergarten', 'name': 'Museumshof'}},
      {'type': 'node',
       'id': 570221424,
       'lat': 49.7513855,
       'lon': 8.9444145,
       'tags': {'addr:housenumber': '5',
        'addr:street': 'Kinziger Straße',
        'amenity': 'biergarten',
        'description': 'Exakte Öffnungstage: 1. Mai bis 3. Oktober.',
        'name': 'Biergarten Birkert',
        'opening_hours': 'May-Sep: Sa 17:00-22:00; Su,PH 11:00-20:00',
        'phone': '+4960634047',
        'website': 'https://www.gabriels-biergarten.de'}},
      {'type': 'node',
       'id': 571264258,
       'lat': 53.0766188,
       'lon': 8.8018298,
       'tags': {'amenity': 'biergarten', 'name': 'Luv'}},
      {'type': 'node',
       'id': 571537106,
       'lat': 48.0479597,
       'lon': 7.9643119,
       'tags': {'amenity': 'biergarten',
        'name': 'Haberstrohs Vesperstube & Straußi',
        'opening_hours': 'Mar-Nov Mo-Tu off, We-Fr 17:00+, Sa 16:00+, Su,PH 12:00+',
        'phone': '+49 7684 316',
        'website': 'http://www.haberstroh-glottertal.de'}},
      {'type': 'node',
       'id': 571598597,
       'lat': 50.670032,
       'lon': 7.2056952,
       'tags': {'amenity': 'biergarten',
        'name': 'Am Drachenbrunnen',
        'website': 'http://drachenbrunnen.drachenfels.net/'}},
      {'type': 'node',
       'id': 573395588,
       'lat': 52.511952,
       'lon': 13.239938,
       'tags': {'amenity': 'biergarten', 'name': 'Stadionterrassen'}},
      {'type': 'node',
       'id': 573398147,
       'lat': 52.5156515,
       'lon': 13.2439374,
       'tags': {'amenity': 'biergarten', 'name': 'Pepe Mager'}},
      {'type': 'node',
       'id': 573609734,
       'lat': 48.9549047,
       'lon': 13.4257844,
       'tags': {'amenity': 'biergarten', 'opening_hours': 'May-Nov: Mo-Su'}},
      {'type': 'node',
       'id': 575639221,
       'lat': 50.1154267,
       'lon': 8.6741859,
       'tags': {'amenity': 'biergarten', 'name': 'Volkswirt'}},
      {'type': 'node',
       'id': 575786732,
       'lat': 51.0493842,
       'lon': 13.2972718,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 583066281,
       'lat': 51.9694804,
       'lon': 13.0106742,
       'tags': {'amenity': 'biergarten', 'name': 'Zum Grafen Bülow'}},
      {'type': 'node',
       'id': 586508263,
       'lat': 48.9281601,
       'lon': 9.3691467,
       'tags': {'addr:city': 'Burgstetten',
        'addr:housenumber': '1',
        'addr:postcode': '71576',
        'addr:street': 'Bahnhof',
        'amenity': 'biergarten',
        'name': 'Bahnhöfle',
        'note': 'Ehemaliger Bahnhof',
        'opening_hours': 'Mo-Su 12:00-22:00'}},
      {'type': 'node',
       'id': 597320982,
       'lat': 48.7660948,
       'lon': 10.7966594,
       'tags': {'amenity': 'biergarten', 'name': 'Thaddäus', 'wheelchair': 'no'}},
      {'type': 'node',
       'id': 597884488,
       'lat': 48.6406482,
       'lon': 10.0032583,
       'tags': {'amenity': 'biergarten', 'name': 'Cafe au lait'}},
      {'type': 'node',
       'id': 598793400,
       'lat': 49.523957,
       'lon': 11.5853558,
       'tags': {'amenity': 'biergarten',
        'email': 'Ute-Lautenschlager@t-online.de',
        'name': 'Felsenkeller',
        'phone': '+49 157 54500778',
        'website': 'http://www.felsenkeller-etzelwang.de/'}},
      {'type': 'node',
       'id': 599203899,
       'lat': 51.5795376,
       'lon': 6.6615515,
       'tags': {'amenity': 'biergarten', 'name': 'Café Restaurant Rheinwacht'}},
      {'type': 'node',
       'id': 599512216,
       'lat': 49.2048005,
       'lon': 8.9925868,
       'tags': {'amenity': 'biergarten', 'name': 'Gasthaus Schwanen'}},
      {'type': 'node',
       'id': 601082997,
       'lat': 52.1250212,
       'lon': 11.5990862,
       'tags': {'amenity': 'biergarten'}},
      {'type': 'node',
       'id': 602104168,
       'lat': 49.435577,
       'lon': 8.4634634,
       'tags': {'amenity': 'biergarten', 'name': 'Seeblick'}},
      {'type': 'node',
       'id': 602731916,
       'lat': 49.7216467,
       'lon': 11.0610982,
       'tags': {'amenity': 'biergarten', 'name': 'Gaststätte Kronengarten'}},
      {'type': 'node',
       'id': 603860690,
       'lat': 47.938341,
       'lon': 10.2973121,
       'tags': {'amenity': 'biergarten', 'name': 'Kleines Brauhaus am Kloster'}},
      {'type': 'node',
       'id': 605474025,
       'lat': 49.2975062,
       'lon': 12.1054006,
       'tags': {'amenity': 'biergarten',
        'name': 'Seeklause',
        'opening_hours': '"Sommermonate"'}},
      {'type': 'node',
       'id': 605536664,
       'lat': 48.8167921,
       'lon': 9.2839092,
       'tags': {'amenity': 'biergarten', 'name': 'Joe Bauer'}},
      ...]}



.. code:: ipython3

    for element in data['elements']:
        p='center' in element
        print(element['type'],p)


.. parsed-literal::

    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    node False
    

.. code:: ipython3

    import numpy as np
    import matplotlib.pyplot as plt
    
    # Collect coords into list
    coords = []
    for element in data['elements']:
      if element['type'] == 'node':
        lon = element['lon']
        lat = element['lat']
        coords.append((lon, lat))
      elif 'center' in element:
        
        lon = element['center']['lon']
        lat = element['center']['lat']
        coords.append((lon, lat))
    
    # Convert coordinates into numpy array
    X = np.array(coords)
    
    plt.plot(X[:, 0], X[:, 1], 'o',color="orange",markeredgecolor="black")
    plt.title('Biergarten in Germany')
    plt.xlabel('Longitude')
    plt.ylabel('Latitude')
    plt.axis('equal')
    plt.show()



.. parsed-literal::

    <Figure size 640x480 with 1 Axes>


.. code:: ipython3

    import overpy
    
    api = overpy.Overpass()
    r = api.query("""
    area["ISO3166-1"="DE"][admin_level=2];
    (node["amenity"="biergarten"](area);
     way["amenity"="biergarten"](area);
     rel["amenity"="biergarten"](area);
    );
    out center;
    """)
    
    coords  = []
    coords += [(float(node.lon), float(node.lat)) 
               for node in r.nodes]
    coords += [(float(way.center_lon), float(way.center_lat)) 
               for way in r.ways]
    coords += [(float(rel.center_lon), float(rel.center_lat)) 
               for rel in r.relations]

.. code:: ipython3

    import geopy

.. code:: ipython3

    from geopy.geocoders import Nominatim

.. code:: ipython3

    nom=Nominatim()
    n=nom.geocode("Villa Julie, Dolega")


.. parsed-literal::

    C:\ProgramData\Anaconda3\lib\site-packages\ipykernel_launcher.py:1: DeprecationWarning: Using Nominatim with the default "geopy/1.18.0" `user_agent` is strongly discouraged, as it violates Nominatim's ToS https://operations.osmfoundation.org/policies/nominatim/ and may possibly cause 403 and 429 HTTP errors. Please specify a custom `user_agent` with `Nominatim(user_agent="my-application")` or by overriding the default `user_agent`: `geopy.geocoders.options.default_user_agent = "my-application"`. In geopy 2.0 this will become an exception.
      """Entry point for launching an IPython kernel.
    

.. code:: ipython3

    n.latitude




.. parsed-literal::

    8.4888835



.. code:: ipython3

    n.longitude




.. parsed-literal::

    -82.4283388488612



.. code:: ipython3

    import pandas,os

.. code:: ipython3

    df1=pandas.read_csv("Coordenadas.csv",sep=",")
    df1["Address"]=df1['Ciudad']+','+df1['Provincia']+','+df1['Pais']
    df1




.. raw:: html

    <div>
    <style scoped>
        .dataframe tbody tr th:only-of-type {
            vertical-align: middle;
        }
    
        .dataframe tbody tr th {
            vertical-align: top;
        }
    
        .dataframe thead th {
            text-align: right;
        }
    </style>
    <table border="1" class="dataframe">
      <thead>
        <tr style="text-align: right;">
          <th></th>
          <th>Ciudad</th>
          <th>Provincia</th>
          <th>Pais</th>
          <th>Address</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>0</th>
          <td>David</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>David,Chiriqui,Panamá</td>
        </tr>
        <tr>
          <th>1</th>
          <td>Dolega</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>Dolega,Chiriqui,Panamá</td>
        </tr>
        <tr>
          <th>2</th>
          <td>Boquete</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>Boquete,Chiriqui,Panamá</td>
        </tr>
        <tr>
          <th>3</th>
          <td>Concepción</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>Concepción,Chiriqui,Panamá</td>
        </tr>
        <tr>
          <th>4</th>
          <td>Remedios</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>Remedios,Chiriqui,Panamá</td>
        </tr>
        <tr>
          <th>5</th>
          <td>Tolé</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>Tolé,Chiriqui,Panamá</td>
        </tr>
        <tr>
          <th>6</th>
          <td>Unachi</td>
          <td>Chiriqui</td>
          <td>Panamá</td>
          <td>Unachi,Chiriqui,Panamá</td>
        </tr>
      </tbody>
    </table>
    </div>



.. code:: ipython3

    df1["Coordinates"]=df1["Address"].apply(nom.geocode)
    df1["Latitude"]=df1["Coordinates"].apply(lambda x: x.latitude if x!=None else None)
    df1["Longitude"]=df1["Coordinates"].apply(lambda x: x.longitude if x!=None else None)

.. code:: ipython3

    df1

.. code:: ipython3

    #!pip install ipyleaflet 

.. code:: ipython3

    from ipyleaflet import Map, basemaps, basemap_to_tiles
    
    m = Map(
        layers=(basemap_to_tiles(basemaps.NASAGIBS.ModisTerraTrueColorCR, "2018-12-06"), ),
        center=(8.48927,-82.42602),
        zoom=8
    )
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/map.rst

.. code:: ipython3

    from ipyleaflet import Map, basemaps, basemap_to_tiles
    
    m = Map(center=(52.204793, 360.121558), zoom=9)
    
    dark_matter_layer = basemap_to_tiles(basemaps.CartoDB.DarkMatter)
    m.add_layer(dark_matter_layer)
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/tile\_layer.rst

.. code:: ipython3

    from __future__ import print_function
    from ipyleaflet import *
    m = Map(center=(52, 10), zoom=8, basemap=basemaps.OpenStreetMap.DE)
    m



.. parsed-literal::

    Map(basemap={'url': 'http://{s}.tile.openstreetmap.de/tiles/osmde/{z}/{x}/{y}.png', 'max_zoom': 18, 'attributi…


.. code:: ipython3

    from ipyleaflet import Marker
    
    #center = (52.204793, 360.121558)
    center=(8.48927,-82.42602)
    m = Map(center=center, zoom=15)
    
    marker = Marker(location=center, draggable=False)
    m.add_layer(marker);
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/marker.rst

.. code:: ipython3

    from ipyleaflet import Marker, Icon, Map
    
    center = (52.204793, 360.121558)
    
    m = Map(center=center, zoom=10)
    icon = Icon(icon_url='https://leafletjs.com/examples/custom-icons/leaf-green.png', icon_size=[38, 95], icon_anchor=[22,94])
    mark = Marker(location=center, icon=icon, rotation_angle=90, rotation_origin='22px 94px')
    m.add_layer(mark);
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/icon.rst

.. code:: ipython3

    from ipywidgets import HTML
    
    from ipyleaflet import Map, Marker, Popup
    
    center = (52.204793, 360.121558)
    
    m = Map(center=center, zoom=9, close_popup_on_click=False)
    
    marker = Marker(location=(52.1, 359.9))
    m.add_layer(marker)
    
    message1 = HTML()
    message2 = HTML()
    message1.value = "Try clicking the marker!"
    message2.value = "Hello <b>World</b>"
    message2.placeholder = "Some HTML"
    message2.description = "Some HTML"
    
    # Popup with a given location on the map:
    popup = Popup(
        location=center,
        child=message1,
        close_button=False,
        auto_close=False,
        close_on_escape_key=False
    )
    m.add_layer(popup)
    
    # Popup associated to a layer
    marker.popup = message2
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/popup.rst

.. code:: ipython3

    from ipyleaflet import Map, WMSLayer
    
    wms = WMSLayer(
        url="https://demo.boundlessgeo.com/geoserver/ows?",
        layers="nasa:bluemarble"
    )
    
    m = Map(layers=(wms, ), center=(42.5531, -48.6914), zoom=3)
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/wms\_layer.rst

.. code:: ipython3

    from ipyleaflet import Map, VideoOverlay
    center=(8.48927,-82.42602)
    m = Map(center=center, zoom=4)
    
    video = VideoOverlay(
        url="https://www.mapbox.com/bites/00188/patricia_nasa.webm",
        bounds=((13, -130), (32, -100))
    )
    
    m.add_layer(video);
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/image\_video\_overlay.rst

.. code:: ipython3

    from ipyleaflet import Map, Polyline
    
    line = Polyline(
        locations = [[
        [[45.51, -122.68],
         [37.77, -122.43],
         [34.04, -118.2]],]],
        color = "green" ,
        fill_color= "green")
    m = Map(center = (42.5, -41), zoom =2)
    m.add_layer(line)
    m
    



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. code:: ipython3

    from ipyleaflet import Map, Polyline
    
    line = Polyline(
        locations = [
        [[45.51, -122.68],
        [37.77, -122.43],
        [34.04, -118.2]],
        [[40.78, -73.91],
        [41.83, -87.62],
        [32.76, -96.72]]
        ],
        color = "green" ,
        fill_color= "green")
    m = Map(center = (42.5, -41), zoom =2)
    m.add_layer(line)
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/polyline.rst

.. code:: ipython3

    from ipyleaflet import Map, Polygon
    
    polygon = Polygon(
        locations=[(8, -82), (9, -85), (13, -83)],
        color="green",
        fill_color="green"
    )
    
    m = Map(center=[8.48927,-82.42602], zoom=6)
    m.add_layer(polygon);
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


https://github.com/jupyter-widgets/ipyleaflet/blob/master/docs/source/api\_reference/polygon.rst

.. code:: ipython3

    from ipyleaflet import Map, basemaps, basemap_to_tiles, Rectangle
    
    watercolor = basemap_to_tiles(basemaps.Stamen.Watercolor)
    
    m = Map(layers=(watercolor, ), center=(53, 354), zoom=5)
    
    rectangle = Rectangle(bounds=((52, 354), (53, 360)))
    
    m.add_layer(rectangle)
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. code:: ipython3

    
    from ipyleaflet import *
    
    
    m = Map( center=[8.48927,-82.42602], zoom=17)
    
    circle = Circle()
    circle.location = (8.48927,-82.42602)
    circle.radius = 50
    circle.color = "green"
    circle.fill_opacity=0.1
    circle.fill_color = "yellow"
    circle.weight=1
    m.add_layer(circle)
    
    circle_marker = CircleMarker()
    circle_marker.location = (8.7007, -82.4579)
    circle_marker.radius = 50
    circle_marker.weight=1
    circle_marker.color = "red"
    circle_marker.fill_color = "red"
    
    m.add_layer(circle_marker)
    
    m
    



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. code:: ipython3

    ipyleaflet.Widget()

.. code:: ipython3

    import ipywidgets
     
    ipywidgets.HBox([m, Map(center=[43.6, 1.44], zoom=10)])



.. parsed-literal::

    HBox(children=(Map(basemap={'url': 'http://{s}.tile.openstreetmap.se/hydda/full/{z}/{x}/{y}.png', 'max_zoom': …


.. code:: ipython3

    import os
    import requests
    url = 'http://earlywarning.usgs.gov/hydrodata/sa_30s_zip_grid/sa_acc_30s_grid.zip'
    filename = os.path.basename(url)
    name = filename[:filename.find('_grid')]
    adffile = name + '/' + name + '/w001001.adf'
    
    if not os.path.exists(adffile):
        r = requests.get(url, stream=True)
        with open(filename, 'wb') as f:
            total_length = int(r.headers.get('content-length'))
            for chunk in tqdm(r.iter_content(chunk_size=1024), total=(total_length/1024) + 1):
                if chunk:
                    f.write(chunk)
                    f.flush()
        zip = zipfile.ZipFile(filename)
        zip.extractall('.')

.. code:: ipython3

    center = [8.34, -82.1]
    zoom = 10
    m = Map(center=center, zoom=zoom)
    m.basemap

.. code:: ipython3

    !pip install mapscript

.. code:: ipython3

    import mapscript

Circle Marker
=============

.. code:: ipython3

    watercolor = basemap_to_tiles(basemaps.Stamen.Watercolor)
    
    m = Map(layers=(watercolor, ), center=(53, 354), zoom=5)
    
    circle_marker = CircleMarker()
    circle_marker.location = (55, 360)
    circle_marker.radius = 50
    circle_marker.color = "red"
    circle_marker.fill_color = "red"
    
    m.add_layer(circle_marker)
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. figure:: attachment:image.png
   :alt: image.png

   image.png

Marker Cluster
==============

.. code:: ipython3

    from ipyleaflet import Map, Marker, MarkerCluster
    
    m = Map(center=(50, 0), zoom=5)
    
    marker1 = Marker(location=(48, -2))
    marker2 = Marker(location=(50, 0))
    marker3 = Marker(location=(52, 2))
    
    marker_cluster = MarkerCluster(
        markers=(marker1, marker2, marker3)
    )
    
    m.add_layer(marker_cluster);
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. figure:: attachment:image.png
   :alt: image.png

   image.png

.. code:: ipython3

    from ipyleaflet import Map, Heatmap
    from random import uniform
    m = Map(center=(0, 0), zoom=2)
    
    heatmap = Heatmap(
        locations=[[uniform(-90, 90), uniform(-180, 180), uniform(0, 800)] for i in range(2000)],
        radius=20
    )
    
    m.add_layer(heatmap);
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. figure:: attachment:image.png
   :alt: image.png

   image.png

.. code:: ipython3

    from ipyleaflet import Map, Velocity, TileLayer, basemaps
    import xarray as xr
    
    center = [0, 0]
    zoom = 1
    m = Map(center=center, zoom=zoom, interpolation='nearest', basemap=basemaps.CartoDB.DarkMatter)
    
    ds = xr.open_dataset('wind-global.nc')
    display_options = {
        'velocityType': 'Global Wind',
        'displayPosition': 'bottomleft',
        'displayEmptyString': 'No wind data'
    }
    wind = Velocity(data=ds,
                    zonal_speed='u_wind',
                    meridional_speed='v_wind',
                    latitude_dimension='lat',
                    longitude_dimension='lon',
                    velocity_scale=0.01,
                    max_velocity=20,
                    display_options=display_options)
    m.add_layer(wind)
    
    m


::


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    <ipython-input-72-f26b7400801e> in <module>()
          6 m = Map(center=center, zoom=zoom, interpolation='nearest', basemap=basemaps.CartoDB.DarkMatter)
          7 
    ----> 8 ds = xr.open_dataset('wind-global.nc')
          9 display_options = {
         10     'velocityType': 'Global Wind',
    

    C:\ProgramData\Anaconda3\lib\site-packages\xarray\backends\api.py in open_dataset(filename_or_obj, group, decode_cf, mask_and_scale, decode_times, autoclose, concat_characters, decode_coords, engine, chunks, lock, cache, drop_variables, backend_kwargs)
        322             store = backends.ScipyDataStore(filename_or_obj,
        323                                             autoclose=autoclose,
    --> 324                                             **backend_kwargs)
        325         elif engine == 'pydap':
        326             store = backends.PydapDataStore.open(filename_or_obj,
    

    C:\ProgramData\Anaconda3\lib\site-packages\xarray\backends\scipy_.py in __init__(self, filename_or_obj, mode, format, group, writer, mmap, autoclose, lock)
        144                                    filename=filename_or_obj,
        145                                    mode=mode, mmap=mmap, version=version)
    --> 146         self._ds = opener()
        147         self._autoclose = autoclose
        148         self._isopen = True
    

    C:\ProgramData\Anaconda3\lib\site-packages\xarray\backends\scipy_.py in _open_scipy_netcdf(filename, mode, mmap, version)
         91     try:
         92         return scipy.io.netcdf_file(filename, mode=mode, mmap=mmap,
    ---> 93                                     version=version)
         94     except TypeError as e:  # netcdf3 message is obscure in this case
         95         errmsg = e.args[0]
    

    C:\ProgramData\Anaconda3\lib\site-packages\scipy\io\netcdf.py in __init__(self, filename, mode, mmap, version, maskandscale)
        250             self.filename = filename
        251             omode = 'r+' if mode == 'a' else mode
    --> 252             self.fp = open(self.filename, '%sb' % omode)
        253             if mmap is None:
        254                 # Mmapped files on PyPy cannot be usually closed
    

    FileNotFoundError: [Errno 2] No such file or directory: 'C:\\Users\\eduli\\wind-global.nc'


https://earth.nullschool.net

.. code:: ipython3

    from ipyleaflet import (
        Map, basemaps, basemap_to_tiles,
        WMSLayer, LayersControl
    )
    
    m = Map(center=(50, 354), zoom=4)
    
    nasa_layer = basemap_to_tiles(basemaps.NASAGIBS.ModisTerraTrueColorCR, "2018-03-30")
    m.add_layer(nasa_layer)
    
    wms = WMSLayer(
        url="https://demo.boundlessgeo.com/geoserver/ows?",
        layers="nasa:bluemarble",
        name="nasa:bluemarble"
    )
    m.add_layer(wms)
    
    m.add_control(LayersControl())
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. code:: ipython3

    from ipyleaflet import (
        Map, basemaps, basemap_to_tiles,
        Circle, Marker, Rectangle, LayerGroup
    )
    
    toner = basemap_to_tiles(basemaps.Stamen.Toner)
    
    m = Map(layers=(toner, ), center=(50, 354), zoom=5)
    
    # Create some layers
    marker = Marker(location=(50, 354))
    circle = Circle(location=(50, 354), radius=500000, color="yellow", fill_color="yellow")
    rectangle = Rectangle(bounds=((54, 354), (55, 360)), color="orange", fill_color="orange")
    
    # Create layer group
    layer_group = LayerGroup(layers=(marker, circle))
    
    m.add_layer(layer_group)
    
    layer_group.add_layer(rectangle)
    
    #layer_group.remove_layer(circle)
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. figure:: attachment:image.png
   :alt: image.png

   image.png

.. code:: ipython3

    from ipyleaflet import Map, GeoJSON
    import json
    
    # Load a local file
    with open('geo.json') as f:
        data = json.load(f)
    
    m = Map(center=(34.6252978589571, -77.34580993652344), zoom=10)
    
    geo_json = GeoJSON(data=data)
    m.add_layer(geo_json);
    
    m


::


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    <ipython-input-84-4cccacd03d26> in <module>()
          3 
          4 # Load a local file
    ----> 5 with open('geo.json') as f:
          6     data = json.load(f)
          7 
    

    FileNotFoundError: [Errno 2] No such file or directory: 'geo.json'


.. figure:: attachment:image.png
   :alt: image.png

   image.png

.. code:: ipython3

    from ipyleaflet import Map, MeasureControl
    
    m = Map(center=(43.0327, 6.0232), zoom=9, basemap=basemaps.Hydda.Full)
    
    measure = MeasureControl(
        position='bottomleft',
        active_color = 'orange',
        primary_length_unit = 'kilometers'
    )
    m.add_control(measure)
    
    measure.completed_color = 'red'
    
    measure.add_length_unit('yards', 1.09361, 4)
    measure.secondary_length_unit = 'yards'
    
    measure.add_area_unit('sqyards', 1.19599, 4)
    measure.secondary_area_unit = 'sqyards'
    
    m



.. parsed-literal::

    Map(basemap={'url': 'http://{s}.tile.openstreetmap.se/hydda/full/{z}/{x}/{y}.png', 'max_zoom': 18, 'attributio…


.. figure:: attachment:image.png
   :alt: image.png

   image.png

.. code:: ipython3

    from ipyleaflet import Map, basemaps, basemap_to_tiles, SplitMapControl
    
    m = Map(center=(42.6824, 365.581), zoom=5)
    
    right_layer = basemap_to_tiles(basemaps.NASAGIBS.ModisTerraTrueColorCR, "2017-11-11")
    left_layer = basemap_to_tiles(basemaps.NASAGIBS.ModisAquaBands721CR, "2017-11-11")
    
    control = SplitMapControl(left_layer=left_layer, right_layer=right_layer)
    m.add_control(control)
    
    m
    



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …


.. code:: ipython3

    from ipyleaflet import Map, basemaps, basemap_to_tiles, DrawControl
    
    watercolor = basemap_to_tiles(basemaps.Stamen.Watercolor)
    
    m = Map( center=(50, 354), zoom=5)
    
    draw_control = DrawControl()
    draw_control.polyline =  {
        "shapeOptions": {
            "color": "#6bc2e5",
            "weight": 8,
            "opacity": 1.0
        }
    }
    draw_control.polygon = {
        "shapeOptions": {
            "fillColor": "#6be5c3",
            "color": "#6be5c3",
            "fillOpacity": 1.0
        },
        "drawError": {
            "color": "#dd253b",
            "message": "Oups!"
        },
        "allowIntersection": False
    }
    draw_control.circle = {
        "shapeOptions": {
            "fillColor": "#efed69",
            "color": "#efed69",
            "fillOpacity": 1.0
        }
    }
    draw_control.rectangle = {
        "shapeOptions": {
            "fillColor": "#fca45d",
            "color": "#fca45d",
            "fillOpacity": 1.0
        }
    }
    
    m.add_control(draw_control)
    
    m



.. parsed-literal::

    Map(basemap={'url': 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', 'max_zoom': 19, 'attribution': 'Map …

