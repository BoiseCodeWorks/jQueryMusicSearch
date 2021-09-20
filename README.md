## jQuery Music Search Instructions

---

### Overview

This application will use jQuery AJAX to interact with the iTunes API.
Requests will go through http://bcw-getter.herokuapp.com to get around the CORS security configuration on the iTunes server.

<br>

### User Interface

<p>The application will need a search form with a text input box and a search button.</p>
<p>There should be an input box to set a limit for the number of results.</p>
<p>There also needs to be an element to contain the search results.</p>
<p>The search results should display:</p>
<ul>
	<li>title</li>
	<li>artist</li>
	<li>price</li>
	<li>album art</li>
	<li>song preview (hint: "html audio tag")</li>
</ul>

<p>Example UI (without limit input):</p>
<img src="https://boisecodeworks.github.io/jQueryMusicSearch/docs/ui-example.jpeg">

<br>

### Required Javascript Objects

#### Music Search Object
<img src="https://boisecodeworks.github.io/jQueryMusicSearch/docs/MusicSearchObject.png">

<br>

### API Notes

<ul>
	<li><strong>API Url:</strong> http://bcw-getter.herokuapp.com/?url=https://itunes.apple.com/search?term=</li>
	<li><strong>Result Limits:</strong> The number of results are automatically limited to 50 items. This limit can be any number up to 200. You can change the limit by appending a limit parameter. For example, to limit the results to 25 items, you can append <code>&amp;limit=25</code> to the request url.</li>
	<li><strong>Url Encoding:</strong> Before making the AJAX request, the request url needs to be encoded with <code>encodeURIComponent</code> to compensate for spaces in the search term. The following example demonstrates using <code>encodeURIComponent</code><br><code>var encodedUrl = encodeURIComponent(url);</code></li>
	<li><strong>Response Type:</strong> JSON</li>
</ul>

<br>

### Data Transformation

<p>Each song in the AJAX response should be transformed to the following structure before passing them to the callback function:</p>
<p><code><pre>
{
	title: song.trackName,
	albumArt: song.artworkUrl60,
	artist: song.artistName,
	collection: song.collectionName,
	price: song.collectionPrice,
	preview: song.previewUrl
}
</pre></code></p>

<br>

### Scoring
* MusicSearch Object (10)
* Result Limiting (10)
* Music Track Preview (10)
* Bootstrap CSS (5)
* Project in GitHub (5)
* GitHub Pages Enabled (5)
* Missed deadline (-10)


#### Total Possible (45)



## Legal Overview

The content under the CodeWorks®, LLC Organization and all of the individual repos are soley intended for use by CodeWorks Instruction to deliver Educational content to CodeWorks Students.

---

## Copyright

© CodeWorks® LLC, 2021. Unauthorized use and/or duplication of this material without express and written permission from CodeWorks, LLC is strictly prohibited.


<img src="https://bcw.blob.core.windows.net/public/img/7815839041305055" width="125">

