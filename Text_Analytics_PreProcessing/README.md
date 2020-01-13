<p><strong>Q1.</strong>&nbsp;Try to get used to using then <strong>nltk </strong>package. Create a text file with, at least, 200</p>
<p>words in it and items that challenge the tokeniser (e.g., I.B.M., and such like</p>
<p>things). But, you need to make these up yourself, so you think about what it is</p>
<p>doing.</p>
<ol>
<li>Load the file in and use nltk.word_tokenizer() on it. Report the list of tokens that are produced from it and note any oddities that arise. Comment on these oddities and how they might be handled.</li>
</ol>
<p><strong><strong>Ans</strong></strong>: After using nltk.word_tokenizer() we can see how the data is being split.</p>
<p>['Good', 'Morning', 'Mr.', 'Singh.I', 'believe', 'Data', 'Science', ',', 'Artificial', 'Intelligence', '(', 'AI', ')', 'and', 'Machine', 'Learning', 'are', 'going', 'to', 'be', 'the', 'cornerstone', 'in', 'shaping', 'the', 'future', 'of', 'the', 'technology', 'industry', '.', 'India', ',', 'U.S.A', ',', 'Russia', ',', 'China', 'all', 'major', 'countries', 'are', 'looking', 'forward', 'to', 'work', 'in', 'these', 'technology', '.', 'The', 'revolution', 'that', 'is', 'going', 'to', 'redefine', 'human-computer', 'interaction', 'in', 'the', 'future', 'is', 'on', 'its', 'way', ',', 'of', 'which', 'I', 'wish', 'to', 'be', 'a', 'part', 'of', '.', 'I', 'am', 'applying', 'for', 'a', 'Master', 'in', 'Data', 'Analytics', 'at', 'your', 'esteemed', 'University', '.', 'I', 'am', 'a', 'person', 'who', 'has', 'always', 'had', 'a', 'profound', 'passion', 'and', 'fascination', 'for', 'areas', 'requiring', 'an', 'analytical', 'approach', '.', 'Right', 'from', 'early', 'days', 'at', 'school', ',', 'Mathematics', 'has', 'intrigued', 'me', '.', 'I', "scored'95", 'out', 'of', '100', 'and', 'ranked', 'no.1', 'in', 'my', 'engineering', 'math', 'subject', '.', 'The', 'most', 'challenging', 'of', 'all', 'problems', 'were', 'my', 'favorites', 'and', 'obtaining', 'solutions', 'to', 'them', 'would', 'leave', 'me', 'with', 'a', 'sheer', 'feeling', 'of', 'ecstasy', '.', 'During', 'the', 'first', 'two', 'years', 'of', 'undergraduate', 'study', ',', 'I', 'studied', 'courses', 'like', 'Theory', 'of', 'Computer', 'Science', ',', 'Data', 'structure', 'and', 'File', 'Systems', ',', 'Microprocessor', 'Based', 'Design', ',', 'Computer', 'Organization', 'and', 'Systems', 'Programming', '.', 'These', 'courses', 'helped', 'me', 'gain', 'a', 'strong', 'background', 'in', 'the', 'fundamentals', 'of', 'Computer', 'Science', '.', 'These', 'were', 'aptly', 'complemented', 'by', 'the', 'laboratory', 'courses', '.', 'The', 'challenging', 'assignments', 'that', 'were', 'a', 'part', 'of', 'the', 'laboratory', 'courses', 'helped', 'me', 'to', 'develop', 'the', 'required', 'technical', 'and', 'programming', 'skills', '.', 'During', 'the', 'last', 'two', 'years', 'of', 'my', 'study', ',', 'I', 'took', 'advanced', 'courses', 'like', 'Artificial', 'Intelligence', ',', 'Compiler', 'Design', ',', 'Databases', ',', 'Operating', 'Systems', ',', 'and', 'Computer', 'Networks', '.']</p>
<p>&nbsp;</p>
<p>The oddities that can be seen are:</p>
<table>
<tbody>
<tr>
<td width="205">
<p><strong><strong>Oddities</strong></strong></p>
</td>
<td width="201">
<p><strong><strong>Comment</strong></strong></p>
</td>
<td width="299">
<p><strong><strong>How to handle</strong></strong></p>
</td>
</tr>
<tr>
<td width="205">
<p><strong><strong>'(', 'AI', ')'</strong></strong></p>
</td>
<td width="201">
<p>(AI)</p>
</td>
<td width="299">
<p>Punctuation&rsquo;s can be removed initially before applying tokenization</p>
</td>
</tr>
<tr>
<td width="205">
<p><strong><strong>&lsquo;scored'95&rsquo;</strong></strong></p>
</td>
<td width="201">
<p>Scored 95</p>
</td>
<td width="299">
<p>Punctuation&rsquo;s can be removed initially before applying tokenization</p>
</td>
</tr>
<tr>
<td width="205">
<p><strong><strong>'Singh.I'</strong></strong></p>
</td>
<td width="201">
<p>Singh. I</p>
</td>
<td width="299">
<p>We can split the para based on full stop(.) first and then apply tokenization</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>
<ol>
<li>Now, do normalization on it, and report this output as your answer.</li>
</ol>
<p><strong><strong>Ans</strong></strong>: For normalization, removed the stop words and changed the case to lower:</p>
<p>['good', 'morning', 'mr.', 'singh.i', 'believe', 'data', 'science', ',', 'artificial', 'intelligence', '(', 'ai', ')', 'machine', 'learning', 'going', 'cornerstone', 'shaping', 'future', 'technology', 'industry', '.', 'india', ',', 'u.s.a', ',', 'russia', ',', 'china', 'major', 'countries', 'looking', 'forward', 'work', 'technology', '.', 'the', 'revolution', 'going', 'redefine', 'human-computer', 'interaction', 'future', 'way', ',', 'i', 'wish', 'part', '.', 'i', 'applying', 'master', 'data', 'analytics', 'esteemed', 'university', '.', 'i', 'person', 'always', 'profound', 'passion', 'fascination', 'areas', 'requiring', 'analytical', 'approach', '.', 'right', 'early', 'days', 'school', ',', 'mathematics', 'intrigued', '.', 'i', "scored'95", '100', 'ranked', 'no.1', 'engineering', 'math', 'subject', '.', 'the', 'challenging', 'problems', 'favorites', 'obtaining', 'solutions', 'would', 'leave', 'sheer', 'feeling', 'ecstasy', '.', 'during', 'first', 'two', 'years', 'undergraduate', 'study', ',', 'i', 'studied', 'courses', 'like', 'theory', 'computer', 'science', ',', 'data', 'structure', 'file', 'systems', ',', 'microprocessor', 'based', 'design', ',', 'computer', 'organization', 'systems', 'programming', '.', 'these', 'courses', 'helped', 'gain', 'strong', 'background', 'fundamentals', 'computer', 'science', '.', 'these', 'aptly', 'complemented', 'laboratory', 'courses', '.', 'the', 'challenging', 'assignments', 'part', 'laboratory', 'courses', 'helped', 'develop', 'required', 'technical', 'programming', 'skills', '.', 'during', 'last', 'two', 'years', 'study', ',', 'i', 'took', 'advanced', 'courses', 'like', 'artificial', 'intelligence', ',', 'compiler', 'design', ',', 'databases', ',', 'operating', 'systems', ',', 'computer', 'networks', '.']</p>
<p>&nbsp;</p>
<ol>
<li>Now, take the output from normalization step and run it through a pos-tagger Report this output as your answer and highlight any inaccuracies that occur at this stage.</li>
</ol>
<p><strong><strong>Ans:</strong></strong></p>
<p>[('good', 'JJ'), ('morning', 'NN'), ('mr.', 'NN'), ('singh.i', 'NNP'), ('believe', 'VBP'), ('data', 'NN'), ('science', 'NN'), (',', ','), ('artificial', 'JJ'), ('intelligence', 'NN'), ('(', '('), ('ai', 'NN'), (')', ')'), ('machine', 'NN'), ('learning', 'VBG'), ('going', 'VBG'), ('cornerstone', 'NN'), ('shaping', 'VBG'), ('future', 'JJ'), ('technology', 'NN'), ('industry', 'NN'), ('.', '.'), ('india', 'NN'), (',', ','), <strong><strong>('u.s.a', 'JJ')</strong></strong>, (',', ','), ('russia', 'NN'), (',', ','), ('china', 'VBP'), ('major', 'JJ'), ('countries', 'NNS'), ('looking', 'VBG'), ('forward', 'RB'), ('work', 'NN'), ('technology', 'NN'), ('.', '.'), ('the', 'DT'), ('revolution', 'NN'), ('going', 'VBG'), ('redefine', 'JJ'), ('human-computer', 'JJ'), ('interaction', 'NN'), ('future', 'JJ'), ('way', 'NN'), (',', ','), ('i', 'JJ'), <strong><strong>('wish', 'JJ')</strong></strong>, ('part', 'NN'), ('.', '.'), ('i', 'NN'), ('applying', 'VBG'), ('master', 'NN'), ('data', 'NNS'), ('analytics', 'NNS'), ('esteemed', 'VBD'), ('university', 'NN'), ('.', '.'), ('i', 'JJ'), ('person', 'NN'), ('always', 'RB'), ('profound', 'JJ'), ('passion', 'NN'), ('fascination', 'NN'), ('areas', 'NNS'), ('requiring', 'VBG'), ('analytical', 'JJ'), <strong><strong>('approach', 'NN')</strong></strong>, ('.', '.'), ('right', 'JJ'), ('early', 'JJ'), ('days', 'NNS'), ('school', 'NN'), (',', ','), ('mathematics', 'NNS'), ('intrigued', 'VBD'), ('.', '.'), ('i', 'VB'), ("scored'95", 'VBP'), ('100', 'CD'), ('ranked', 'JJ'), ('no.1', 'JJ'), ('engineering', 'NN'), ('math', 'NN'), ('subject', 'NN'), ('.', '.'), ('the', 'DT'), ('challenging', 'VBG'), ('problems', 'NNS'), ('favorites', 'VBZ'), ('obtaining', 'VBG'), ('solutions', 'NNS'), ('would', 'MD'), ('leave', 'VB'), ('sheer', 'NN'), ('feeling', 'NN'), <strong><strong>('ecstasy', 'NN')</strong></strong>, ('.', '.'), ('during', 'IN'), ('first', 'JJ'), ('two', 'CD'), ('years', 'NNS'), ('undergraduate', 'JJ'), ('study', 'NN'), (',', ','), ('i', 'VB'), ('studied', 'VBN'), ('courses', 'NNS'), ('like', 'IN'), ('theory', 'NN'), ('computer', 'NN'), ('science', 'NN'), (',', ','), ('data', 'NN'), ('structure', 'NN'), ('file', 'NN'), ('systems', 'NNS'), (',', ','), ('microprocessor', 'NN'), ('based', 'VBN'), ('design', 'NN'), (',', ','), ('computer', 'NN'), ('organization', 'NN'), ('systems', 'NNS'), ('programming', 'VBG'), ('.', '.'), ('these', 'DT'), ('courses', 'NNS'), ('helped', 'VBD'), ('gain', 'VB'), ('strong', 'JJ'), ('background', 'NN'), ('fundamentals', 'NNS'), ('computer', 'NN'), ('science', 'NN'), ('.', '.'), ('these', 'DT'), ('aptly', 'RB'), ('complemented', 'VBN'), ('laboratory', 'NN'), ('courses', 'NNS'), ('.', '.'), ('the', 'DT'), ('challenging', 'VBG'), ('assignments', 'NNS'), ('part', 'NN'), ('laboratory', 'NN'), ('courses', 'NNS'), ('helped', 'VBD'), ('develop', 'VB'), ('required', 'JJ'), ('technical', 'JJ'), ('programming', 'NN'), ('skills', 'NNS'), ('.', '.'), ('during', 'IN'), ('last', 'JJ'), ('two', 'CD'), ('years', 'NNS'), ('study', 'VBP'), (',', ','), ('i', 'JJ'), ('took', 'VBD'), ('advanced', 'JJ'), ('courses', 'NNS'), ('like', 'IN'), ('artificial', 'JJ'), ('intelligence', 'NN'), (',', ','), ('compiler', 'NN'), ('design', 'NN'), (',', ','), ('databases', 'NNS'), (',', ','), ('operating', 'VBG'), ('systems', 'NNS'), (',', ','), ('computer', 'NN'), ('networks', 'NNS'), ('.', '.')]</p>
<p><strong><strong>&nbsp;</strong></strong></p>
<table>
<tbody>
<tr>
<td width="358">
<p><strong><strong>Inaccuracies</strong></strong></p>
</td>
<td width="353">
<p><strong><strong>Comment</strong></strong></p>
</td>
</tr>
<tr>
<td width="358">
<p>('approach', 'NN')</p>
</td>
<td width="353">
<p>Considered as noun but It&rsquo;s a verb</p>
</td>
</tr>
<tr>
<td width="358">
<p>('wish', 'NN')</p>
</td>
<td width="353">
<p>Considered as noun but It&rsquo;s a verb</p>
</td>
</tr>
<tr>
<td width="358">
<p>('u.s.a', 'JJ')</p>
</td>
<td width="353">
<p>Considered as Adjective but it&rsquo;s a noun</p>
</td>
</tr>
<tr>
<td width="358">
<p>('ecstasy', 'JJ')</p>
</td>
<td width="353">
<p>Considered as Adjective but it&rsquo;s a noun</p>
</td>
</tr>
</tbody>
</table>
<p><strong><strong>&nbsp;</strong></strong></p>
<p>&nbsp;</p>
<p><strong><strong>Q2.</strong></strong>&nbsp;Now, take a second, new text-file do the following:</p>
<ol>
<li>Tokenize a new text-file (200 words) and the stem it using Porter Stemming. Report your answer and some of weird things that Porter Stemming does.</li>
</ol>
<p><strong><strong>Ans: </strong></strong>The article (<em><em>My Biggest Competitive Advantage Is to Look You in the Eye</em></em>,2019) has been used for text extraction.</p>
<p>After applying porter stemming on the data, following is the output.</p>
<p>['I', 'have', 'alway', <strong><strong>'believ'</strong></strong>, 'there', 'is', 'magic', 'in', 'face-to-fac', 'human', 'interact', '.', 'As', 'a', 'child', <strong><strong>'struggl'</strong></strong>, 'with', 'undiagnos', 'dyslexia', ',', 'I', 'turn', 'to', 'peopl', 'to', 'learn', 'about', 'the', 'world', '.', 'As', 'a', 'young', 'filmmak', ',', 'I', 'came', 'to', 'find', 'that', 'some', 'of', 'the', 'most', 'emot', 'impact', 'moment', 'in', 'a', 'movi', 'happen', 'when', 'charact', 'meet', 'each', 'other', '&rsquo;', 's', 'gaze', '&mdash;', 'in', 'moment', 'of', 'confront', 'or', 'confess', 'or', 'love', 'at', 'first', 'sight', '.', 'throughout', 'my', 'life', ',', 'I', '&rsquo;', 've', 'learn', 'that', 'such', 'connect', 'are', 'more', 'than', 'just', 'a', 'storytel', 'devic', ';', 'they', 'are', 'the', 'antidot', 'to', 'much', 'of', 'what', 'ail', 'us', '.', 'I', 'have', 'come', 'to', 'believ', 'that', 'our', 'abil', 'to', 'struggl', ',', 'see', 'one', 'anoth', 'better', 'depend', ',', 'quit', 'liter', ',', 'on', 'us', 'see', 'each', 'other', 'at', 'all', '.', 'It', 'turn', 'out', 'that', 'human', 'are', 'hardwir', 'for', '1-to-1', <strong><strong>'commun'</strong></strong>, '.', 'We', 'know', ',', 'for', 'exampl', ',', 'that', 'there', 'are', 'specif', 'cell', 'in', 'our', 'brain', ',', 'known', 'as', '&ldquo;', 'mirror', 'neuron', ',', '&rdquo;', 'that', 'discharg', 'when', 'we', '&rsquo;', 're', 'learn', 'to', 'imit', 'social', 'cue', 'from', 'one', 'anoth', '.', 'studi', 'show', 'that', 'when', 'mother', 'and', 'babi', 'look', 'at', 'each', 'other', ',', 'their', 'brain', 'wave', 'actual', 'sync', 'up', 'and', 'produc', 'oxytocin', ',', 'a', 'chemic', 'often', 'describ', 'as', 'the', '&ldquo;', 'love', 'hormone.', '&rdquo;', 'evolutionari', 'biologist', 'even', 'surmis', 'that', 'the', 'white', 'of', 'our', 'eye', 'evolv', 'so', 'that', 'we', 'could', 'better', 'follow', 'each', 'other', '&rsquo;', 's', 'gaze', '.', 'It', 'is', 'through', 'face-to-fac', 'interact', 'that', 'we', 'develop', 'the', <strong><strong>'essenti'</strong></strong>, 'trait', 'of', 'social', 'be', ':', 'empathi', ',', 'trust', ',', 'and', 'mutual', 'respect', '.', 'and', 'it', '&rsquo;', 's', 'in', 'it', 'absenc', 'that', 'we', 'often', 'see', 'the', 'darker', 'side', 'of', 'human', 'natur', '.', 'there', '&rsquo;', 's', 'a', 'reason', 'whi', 'we', 'have', 'a', 'road', 'rage', 'problem', ',', 'but', 'not', 'a', 'sidewalk', 'rage', 'problem', ',', 'whi', 'internet', 'troll', 'can', 'be', 'so', 'viciou', 'onlin', 'and', 'so', 'meek', 'in', 'real', 'life', '.', 'It', '&rsquo;', 's', 'as', 'though', 'we', 'are', 'more', 'apt', 'to', 'human', 'those', 'we', 'can', 'see', ',', 'and', 'to', 'dehuman', 'those', 'we', 'can', 'not', '.']</p>
<p>&nbsp;</p>
<p>There are a lot of oddities that occurs after using Porter stemmer, out of which I have mentioned few in the table below.</p>
<table>
<tbody>
<tr>
<td width="355">
<p><strong><strong>Actual Word</strong></strong></p>
</td>
<td width="355">
<p><strong><strong>After Porter Stemming</strong></strong></p>
</td>
</tr>
<tr>
<td width="355">
<p>&lsquo;believe&rsquo;</p>
</td>
<td width="355">
<p>'believ'</p>
</td>
</tr>
<tr>
<td width="355">
<p>'struggle'</p>
</td>
<td width="355">
<p>'struggl'</p>
</td>
</tr>
<tr>
<td width="355">
<p>&lsquo;communication&rsquo;</p>
</td>
<td width="355">
<p>'commun&rsquo;</p>
</td>
</tr>
<tr>
<td width="355">
<p>&lsquo;essential&rsquo;</p>
</td>
<td width="355">
<p>'essenti'</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>
<ol>
<li>Tokenize the new text-file and then lemmatize it using WordNet Lemmatizer; note you may have to pos-tag the sentences first and then convert the tags to make this work. Report the result of these steps and point out some of the things that look wrong.</li>
</ol>
<p><strong><strong>Ans: </strong></strong>After applying porter stemmer on the new text file, I have converted the tags to simple form so that WordNet Lemmatizer can work. Below function is used to convert the tags.</p>
<p><strong><strong>def convert_big_tags(t):</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;if t=='vbd' or t=='vbg' or t=='vbz':</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return 'v'</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;elif t == 'jj' or t == 'jjr' or t=='jjs':</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return 'a'</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;elif t == 'rb' or t=='rbr' or t=='rbs':</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return 'r'</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;else:</strong></strong></p>
<p><strong><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return 'n'</strong></strong></p>
<p><strong><strong>Output:</strong></strong></p>
<p>[('I', 'n'), ('have', 'n'), ('always', 'r'), ('believed', 'n'), ('there', 'n'), ('be', 'v'), ('magic', 'a'), ('in', 'n'), <strong><strong>('face-to-face', 'a')</strong></strong>, ('human', 'a'), ('interaction', 'n'), ('.', 'n'), ('As', 'n'), ('a', 'n'), ('child', 'n'), ('struggle', 'v'), ('with', 'n'), ('undiagnosed', 'a'), ('dyslexia', 'n'), (',', 'n'), ('I', 'n'), ('turn', 'v'), ('to', 'n'), ('people', 'n'), ('to', 'n'), ('learn', 'n'), ('about', 'n'), ('the', 'n'), ('world', 'n'), ('.', 'n'), ('As', 'n'), ('a', 'n'), ('young', 'a'), ('filmmaker', 'n'), (',', 'n'), ('I', 'n'), ('come', 'v'), ('to', 'n'), ('find', 'n'), ('that', 'n'), ('some', 'n'), ('of', 'n'), ('the', 'n'), ('most', 'r'), ('emotionally', 'r'), <strong><strong>('impactful', 'a')</strong></strong>, ('moment', 'n'), ('in', 'n'), ('a', 'n'), ('movie', 'n'), ('happen', 'n'), ('when', 'n'), ('character', 'n'), ('meet', 'n'), ('each', 'n'), ('other', 'a'), ('&rsquo;', 'a'), ('s', 'n'), ('gaze', 'n'), ('&mdash;', 'n'), ('in', 'n'), ('moment', 'n'), ('of', 'n'), ('confrontation', 'n'), ('or', 'n'), ('confession', 'n'), ('or', 'n'), ('love', 'n'), ('at', 'n'), ('first', 'a'), ('sight', 'n'), ('.', 'n'), ('Throughout', 'n'), ('my', 'n'), ('life', 'n'), <strong><strong>(',', 'n')</strong></strong>, ('I', 'n'), ('&rsquo;', 'n'), ('ve', 'r'), ('learned', 'n'), ('that', 'n'), ('such', 'a'), ('connection', 'n'), ('are', 'n'), ('more', 'a'), ('than', 'n'), ('just', 'r'), ('a', 'n'), ('storytelling', 'a'), ('device', 'n'), (';', 'n'), ('they', 'n'), ('are', 'n'), ('the', 'n'), ('antidote', 'n'), ('to', 'n'), ('much', 'r'), ('of', 'n'), ('what', 'n'), ('ail', 'v'), ('u', 'n'), ('.', 'n'), ('I', 'n'), ('have', 'n'), ('come', 'n'), ('to', 'n'), ('believe', 'n'), ('that', 'n'), ('our', 'n'), ('ability', 'n'), ('to', 'n'), ('struggle', 'n'), (',', 'n'), ('see', 'n'), ('one', 'n'), ('another', 'n'), ('good', 'a'), ('depends', 'n'), (',', 'n'), ('quite', 'r'), ('literally', 'r'), (',', 'n'), ('on', 'n'), ('u', 'n'), ('see', 'v'), ('each', 'n'), ('other', 'a'), ('at', 'n'), ('all', 'n'), ('.', 'n'), ('It', 'n'), ('turn', 'v'), ('out', 'n'), ('that', 'n'), ('human', 'n'), ('are', 'n'), ('hardwired', 'n'), ('for', 'n'), ('1-to-1', 'a'), ('communication', 'n'), ('.', 'n'), ('We', 'n'), ('know', 'n'), (',', 'n'), ('for', 'n'), ('example', 'n'), (',', 'n'), ('that', 'n'), ('there', 'n'), ('are', 'n'), ('specific', 'a'), ('cell', 'n'), ('in', 'n'), ('our', 'n'), ('brain', 'n'), (',', 'n'), ('known', 'n'), ('a', 'n'), ('&ldquo;', 'a'), ('mirror', 'n'), ('neuron', 'n'), (',', 'n'), ('&rdquo;', 'n'), ('that', 'n'), ('discharge', 'n'), ('when', 'n'), ('we', 'n'), ('&rsquo;', 'n'), ('re', 'a'), ('learning', 'n'), ('to', 'n'), ('imitate', 'n'), ('social', 'a'), ('cue', 'n'), ('from', 'n'), ('one', 'n'), ('another', 'n'), ('.', 'n'), ('Studies', 'v'), ('show', 'n'), ('that', 'n'), ('when', 'n'), ('mother', 'n'), ('and', 'n'), ('baby', 'n'), ('look', 'n'), ('at', 'n'), ('each', 'n'), ('other', 'a'), (',', 'n'), ('their', 'n'), ('brain', 'n'), ('wave', 'n'), ('actually', 'r'), ('sync', 'n'), ('up', 'n'), ('and', 'n'), ('produce', 'n'), ('oxytocin', 'n'), (',', 'n'), ('a', 'n'), ('chemical', 'n'), ('often', 'r'), ('described', 'n'), ('a', 'n'), ('the', 'n'), ('&ldquo;', 'n'), ('love', 'n'), ('hormone.', 'n'), ('&rdquo;', 'n'), ('Evolutionary', 'n'), ('biologist', 'n'), ('even', 'r'), ('surmise', 'n'), ('that', 'n'), ('the', 'n'), ('white', 'n'), ('of', 'n'), ('our', 'n'), ('eye', 'n'), ('evolved', 'n'), ('so', 'r'), ('that', 'n'), ('we', 'n'), ('could', 'n'), ('well', 'r'), ('follow', 'n'), ('each', 'n'), ('other', 'a'), ('&rsquo;', 'a'), ('s', 'n'), ('gaze', 'n'), ('.', 'n'), ('It', 'n'), ('be', 'v'), ('through', 'n'), ('face-to-face', 'a'), ('interaction', 'n'), ('that', 'n'), ('we', 'n'), ('develop', 'n'), ('the', 'n'), ('essential', 'a'), ('trait', 'n'), ('of', 'n'), ('social', 'a'), ('being', 'n'), (':', 'n'), ('empathy', 'n'), (',', 'n'), ('trust', 'n'), (',', 'n'), ('and', 'n'), ('mutual', 'a'), ('respect', 'n'), ('.', 'n'), ('And', 'n'), ('it', 'n'), ('&rsquo;', 'n'), <strong><strong>('s', 'v')</strong></strong>, ('in', 'n'), ('it', 'n'), ('absence', 'n'), ('that', 'n'), ('we', 'n'), ('often', 'r'), ('see', 'n'), ('the', 'n'), ('darker', 'n'), ('side', 'n'), ('of', 'n'), ('human', 'a'), ('nature', 'n'), <strong><strong>('.', 'n')</strong></strong>, ('There', 'n'), ('&rsquo;', 'a'), ('s', 'n'), ('a', 'n'), ('reason', 'n'), ('why', 'n'), ('we', 'n'), ('have', 'n'), ('a', 'n'), ('road', 'n'), ('rage', 'n'), ('problem', 'n'), (',', 'n'), ('but', 'n'), ('not', 'r'), ('a', 'n'), ('sidewalk', 'n'), ('rage', 'n'), ('problem', 'n'), (',', 'n'), ('why', 'n'), ('internet', 'n'), ('troll', 'n'), ('can', 'n'), ('be', 'n'), ('so', 'r'), ('vicious', 'a'), ('online', 'n'), ('and', 'n'), ('so', 'r'), ('meek', 'a'), ('in', 'n'), ('real', 'a'), ('life', 'n'), ('.', 'n'), ('It', 'n'), ('&rsquo;', 'v'), ('s', 'a'), ('a', 'n'), ('though', 'n'), ('we', 'n'), ('are', 'n'), ('more', 'r'), ('apt', 'a'), ('to', 'n'), ('humanize', 'n'), ('those', 'n'), ('we', 'n'), ('can', 'n'), ('see', 'n'), (',', 'n'), ('and', 'n'), ('to', 'n'), ('dehumanize', 'n'), ('those', 'n'), ('we', 'n'), ('can', 'n'), ('not', 'r'), ('.', 'n')]</p>
<p>&nbsp;</p>
<p>After changing the tags and passing words through the WordNet Lemmatizer we can see few of the tags are wrongly mentioned. These oddities are highlighted in the above output. &nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<ol>
<li>Compare the outputs from Porter Stemming and the Lemmatisation of the same file. Which do you think is the best to use and why?</li>
</ol>
<p><strong><strong>Ans: </strong></strong>After comparing the output from both of them, It is clear that lemmatisation works better because:</p>
<p><strong><strong>Lemmatisation:</strong></strong></p>
<p>-Gets better roots</p>
<p>-Deals better with irregular plurals</p>
<p>-Removes affixes if the output word is present in dictionary</p>
<p><strong><strong>Porter Stemmer</strong></strong></p>
<p>-Removes plurals, -ed and -ing suffixes</p>
<p>-Turns &lsquo;y&rsquo; to &lsquo;i&rsquo; when there is another vowel in the stem</p>
<p>-Removal of final -e etc.</p>
<p>&nbsp;</p>
<p>Below is the comparison table:</p>
<table>
<tbody>
<tr>
<td width="236">
<p><strong><strong>Actual Word</strong></strong></p>
</td>
<td width="236">
<p><strong><strong>Porter Stemmer</strong></strong></p>
</td>
<td width="236">
<p><strong><strong>Lemmatisation</strong></strong></p>
</td>
</tr>
<tr>
<td width="236">
<p>always</p>
</td>
<td width="236">
<p>alway</p>
</td>
<td width="236">
<p>always</p>
</td>
</tr>
<tr>
<td width="236">
<p>believed</p>
</td>
<td width="236">
<p>believ</p>
</td>
<td width="236">
<p>believed</p>
</td>
</tr>
<tr>
<td width="236">
<p>interactions</p>
</td>
<td width="236">
<p>interact</p>
</td>
<td width="236">
<p>interaction</p>
</td>
</tr>
<tr>
<td width="236">
<p>emotionally</p>
</td>
<td width="236">
<p>emot</p>
</td>
<td width="236">
<p>emotionally</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p><strong><strong>&nbsp;</strong></strong></p>
<p><strong><strong>Q3.</strong></strong>&nbsp;Finally, choose a remote webpage and extract key text content from it. Install the packages you need and then parse it using BeautifulSoup. Try to get to a point where you can extract one of its XML/HTML parts (e.g., title, summary, body)</p>
<p><strong><strong>Ans: </strong></strong>The article (<em><em>How to Read Medium Member-Only Articles for Free</em></em>,2018) has been used for text extraction.</p>
<p>We can open url using the <em><em>urllib.request.urlopen()</em></em>&nbsp;function as follows:</p>
<p><strong><strong>url=r'https://www.syncwithtech.org/member-only-content-free-medium/'</strong></strong></p>
<p><strong><strong>rawhtml = urllib.request.urlopen(url).read()</strong></strong></p>
<p>&nbsp;</p>
<p>Once we had the rawhtml we can parse it using BeautifulSoap as shown in the code below.</p>
<p><strong><strong>from bs4 import BeautifulSoup</strong></strong></p>
<p><strong><strong>soup = BeautifulSoup(rawhtml)</strong></strong></p>
<p>&nbsp;</p>
<p>After that we can fetch the individual components such as title or body using the following commands:</p>
<p><strong><strong>soup.title</strong></strong></p>
<p><strong><strong>Output</strong></strong></p>
<p><strong><strong>&lt;title&gt;How to Read Medium Member-Only Articles for Free&lt;/title&gt;</strong></strong></p>
<p>&nbsp;</p>
<p><strong><strong>soup.body</strong></strong></p>
<p><strong><strong>Output</strong></strong>: A short snippet of the output is shown below.</p>
<p><strong><strong>. . . . .</strong></strong></p>
<p><strong><strong>&lt;section class="post-full-content"&gt;</strong></strong></p>
<p><strong><strong>&lt;div class="kg-card-markdown"&gt;&lt;p&gt;Medium is an awesome platform with a lot of great content. People love it. The newsletter they send is useful more often than not. Sometimes when you see a compelling title for a post and click on the link to read the article. You get this,&lt;/p&gt;</strong></strong></p>
<p><strong><strong>&lt;blockquote&gt;</strong></strong></p>
<p><strong><strong>. . . . .</strong></strong><strong><strong>&nbsp;</strong></strong></p>
<p><strong><strong>&nbsp;</strong></strong></p>
<p><strong><strong>References:</strong></strong></p>
<p>S,Ganapathy.(2018) <em><em>How to Read Medium Member-Only Articles for Free</em></em>. Available at: <a href="https://www.syncwithtech.org/member-only-content-free-medium/"><u>https://www.syncwithtech.org/member-only-content-free-medium/</u></a></p>
<p>&nbsp;</p>
<p>Grazer,Brian.(2019)<em><em>My Biggest Competitive Advantage Is to Look You in the Eye</em></em>. Available at: <a href="https://marker.medium.com/my-biggest-competitive-advantage-is-to-look-you-in-the-eye-7ec2dc6ef30d"><u>https://marker.medium.com/my-biggest-competitive-advantage-is-to-look-you-in-the-eye-7ec2dc6ef30d</u></a></p>
<p>&nbsp;</p>
<p>&nbsp;&nbsp;</p>
