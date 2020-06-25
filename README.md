# Udemy_apps
#Learning

2020.06.23 App_1_dictionary
  something new in this section: input; library 'json'; library 'difflib': get_close_matches, SequenceMatcher; str.
  word = input("what to enter: ")
  data = json.load(open("data.json"); data.keys()
  SequenceMatch(None, 'word_a', 'word_b').ratio()
  get_close_matches('word_a', a_list_word, n = a_number, cutoff = number_the_ratio)
  word.lower(), word.upper(), word.title()

2020.06.24 App_2_webmaps Take ~3h.
  somthing new in this section: load and label maps under the library 'folium'. 
  Note: learned similar thing in the R workshop. Editing map might be a high-frequently used function in daily applications. Spent ~3h on this section.
  Problem: Do not know how to generate .json files for map labeling. Hard to read help for other functions, want a GUI for python libraries. 
  
  python3 -m notebook // Have difficulty with Anaconda-Navigator, can not load library, give up it. Use Mac terminal python3 for jupyter notebook.
  
  map = folium.Map(location = a_list, zoom_start = a_number, tiles = "Stamen Terrain")
  fg = folium.FeatureGroup(name = a_string)
  fg.add_child(folium.CircleMarker(location = a_list, radius = a_number, popup = folium.Popup(str(el)+'m',parse_html = True), fill_color = color_producer(el), color  = a_string_for_color, fill_opacity = a_number )) // color is out the color of outline.
  
  fg.add_child(folium.Marker(location = a_list, popup = a_string, icon = folium.Icon(color = a_string_for_color) ))
  fg.add_child(folium.Marker(location=a_list, popup=folium.Popup(iframe), icon = folium.Icon(color = a_string_for_color)))
  iframe is pre-defined as html:
  html = """
  Volcano name:<br>
  <a href="https://www.google.com/search?q=%%22%s%%22" target="_blank">%s</a><br>
  Height: %s m
  """
  iframe = folium.IFrame(html=html % (name, name, el), width=200, height=100) // (name, name, el) are inputs

  fg.add_child(folium.GeoJson(data = open('world.json','r', encoding ='utf-8-sig').read(), 
style_function=lambda x: {'fillColor':'green' if x['properties']['POP2005'] < 10000000
else 'orange' if 10000000 <= x['properties']['POP2005'] < 20000000 else 'red'})) // add color layer mask for selected regions
  
  map.add_child(folium.LayerControl()) 
  map.add_child(fg)
  map.save('Map1.html')
  
2020.06.25 App_3_webpage Take ~2h.
  something new in this section: Flask.
  Did not work. Cannot fix the problem. Not as easy as github personal page.
  CSS: a file defines format of the webpage, arrangement, font, color, etc.
  html: a file defines information of the webpage.
  python file: just load the webpage to somewhere?
  
  
  






