# loosing-language
<section class="readme">

  <h1>Losing a Language</h1>

  <p>
    An interactive data story about how Belarusian disappeared from everyday
    life but remained central to identity.
  </p>

  <p>
    🔗 <strong>Read the story:</strong>
    <a href="https://by-ali.github.io/loosing-language/" target="_blank" rel="noopener noreferrer">
      https://by-ali.github.io/loosing-language/
    </a>
  </p>

  <h2>Repository structure</h2>

  <ul>
    <li><code>index.html</code> — the published story</li>
    <li><code>images/</code> — images and visual assets</li>
    <li><code>files/</code> — cleaned datasets used in the analysis</li>
    <li><code>google_trends.ipynb</code> — Google Trends analysis</li>
    <li><code>bel_lit_extreme.ipynb</code> — analysis of books designated as extremist materials</li>
    <li><code>repressions_analysis.ipynb</code> — analysis of repression against cultural figures</li>
  </ul>

  <h2>Data</h2>

  <p>
    The project combines historical sources with original data analysis. It uses
    <a href="https://census.belstat.gov.by/saiku/?guest=true&lang=ru&default_view_state=edit#query/open//public/F503N_ru.saiku" target="_blank" rel="noopener noreferrer">census data</a>,
    <a href="https://dataportal.belstat.gov.by/osids/indicator-info/10103000022" target="_blank" rel="noopener noreferrer">education statistics</a>,
    <a href="https://byculture.org/represii/" target="_blank" rel="noopener noreferrer">monitoring</a>
    by the Belarusian Council for Culture, and PEN Belarus's
    <a href="https://bannedbooks.penbelarus.org/extremist_list/" target="_blank" rel="noopener noreferrer">register</a>
    of books designated as "extremist materials."
  </p>

  <h2>Methodology</h2>

  <p>
    Google search data was collected with
    <a href="https://pypi.org/project/pytrends/" target="_blank" rel="noopener noreferrer">Pytrends</a>
    for Belarus between 2015 and 2025. I compared 36 pairs of equivalent
    Belarusian- and Russian-language search queries covering everyday topics
    such as work, housing, healthcare, education, shopping and news. Since
    Google Trends reports relative rather than absolute search interest, I
    aggregated weekly observations into yearly averages using
    <strong>pandas</strong>. I also compiled a second dataset of searches
    related to Belarusian language, literature, history and national identity
    to measure changes in cultural interest over time.
  </p>

  <p>
    The PEN Belarus bibliography was parsed into structured records using
    Python's <code>re</code> module. Because the dataset does not specify the
    language of each title, I built a custom rule-based classifier that
    identifies Belarusian and Russian using language-specific letters,
    orthographic patterns and common vocabulary instead of a general-purpose
    language detection model. Unfortunately, this classifier is tailored specifically to this dataset of books and would not perform well on arbitrary datasets.
  </p>

  <p>
    Data cleaning and analysis were performed with
    <strong>pandas</strong>. Visualizations were created in
    <strong>Flourish</strong>. 
 </p>

  <p>   
    The interactive glossary at the end of the story
    was built with HTML, CSS and vanilla JavaScript and uses the browser's
    <strong>Web Speech API</strong> to generate Belarusian pronunciation.
  </p>

</section>
