<h1 align="center">
The Paris streets of the Maigret novels
</h1>

<p align="center">
  <img src="https://github.com/JackMcKechnie/maigret_streets/blob/main/maigret_final_100_with_text.png" />
</p>

<p align="center">
In order to keep up my written French after finishing university, I have been reading books in their original French language. After a few heavy and slow going reads about poverty and colonisation in the Maghreb and the rise and fall of council housing in Paris, I decided that it was time for something a bit lighter. Helped along by being gifted a copy of “Maigret et le Tueur” I decided to read some of Georges Simenon’s Maigret series. The novels follow Jules Maigret as he investigates a wide range of crimes, from simple thefts to complex murders, using his unique combination of intelligence, intuition, and understanding of human nature to solve cases and bring perpetrators to justice.

  

As I was reading, I couldn’t help but notice the number of different street names that Simenon mentioned in “Maigret et le Tueur” and I started to wonder if A) they are real streets and B) if they are, then where in Paris are the books set. I decided to have a look into it. The task naturally broke itself down into two different stages; collecting the streets and the number of times they are mentioned, and plotting that data onto a map.

  

At first I though that I would collect the data manually, as I was reading, but I quickly realised how long and annoying a task that would become. Stopping two or three times a page to write down a street name was impractical and ruined my experience of reading the book. Therefore, I needed to add in another step before my original two, find the book in a digital format. This was more difficult that I first expected, but i eventually came across “Maigret et le Tueur” on vk.com - essentially Russian Facebook. Worried I’d ruin my laptop with viruses I downloaded the .epub version of the book, converted it to a .txt file and breathed a sigh of relief that my laptop hadn’t burst into flames.

  

This brought me onto the next step, extracting the data from the book. I would need a list of all of the streets in Paris and then could check each line of the book to see if it contained a street. Getting the list of street names was surprisingly easy after some googling, it is all available with OpenStreetMaps data using the OSMnx package, which I was planning on using for mapping the streets anyway. Once I had this, it was just a case of reading in each line of the book, removing some punctuation that was causing some issues and checking if it had a street name. After saving each of those street names, I counted their frequency and saved them in a file for later use.

The code from this step can be seen [here](https://github.com/JackMcKechnie/maigret_streets/blob/main/extract_street_names.ipynb), and the output can be seen [here](https://github.com/JackMcKechnie/maigret_streets/blob/main/street_names_count.txt).

  

Next was mapping the data and in order to do this I used the OSMnx package. I first generated a graph of Paris to see if I could get it to work. Once I had this working I needed to highlight the streets if they appeared in the file, regardless of their frequency. I was able to figure out how to do this with help from [this](https://github.com/puntofisso/OSMnxNotebooks/blob/master/Street%20colouring.ipynb) great notebook by Puntofisso. I then used the same logic but with a Matplotlib colour map function to get the heat map effect and complete the image.

The code from this step can be seen [here](https://github.com/JackMcKechnie/maigret_streets/blob/main/paris.ipynb).

  

However, this provided somewhat unsatisfactory results. There just wasn’t enough data for the map to be interesting or show much information of use as most of the streets were mentioned only once or twice. Therefore, I went back onto vk.com and downloaded the rest of the Maigret books and repeated my steps to generate the above map.

To return to my original questions and conclude: A) yes they are real streets mentioned in the book and B) the books take place all over Paris. There is the obvious common streets around the Palais de Justice on Quai des Orfèvres and Place Dauphine. Interestingly, almost all of the most commonly mentioned streets are north of the Seine, with the notable exception of Boulevard Saint-Germain passing through Latin Quarter and the Sorbonne. I’m not sure that I’ve taken anything of note from the actual map, other than it’s something that looks quite nice and that I enjoyed making. I don’t think we can take away some interesting point about crime in Paris, or about Maigret - other than he never visited anywhere outside the Boulevard Périphérique according to this map! However, it was a nice way of spending a few hours over the 2022/2023 Christmas and New Year period and I got the chance to use the amazing OSMnx package for something I was interested in.
</p>
