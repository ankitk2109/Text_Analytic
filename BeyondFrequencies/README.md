## Objective
Preprocessing Tweets, Calculating TF-IDF score and visualising the most frequent words through wordcloud.
Calcualting the entropy of tweets which could potentialy classify which set of tweets are spam and which are not.

<html xmlns:o="urn:schemas-microsoft-com:office:office" xmlns:w="urn:schemas-microsoft-com:office:word" xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882" xmlns="http://www.w3.org/TR/REC-html40"><head><meta http-equiv=Content-Type  content="text/html; charset=utf-8" ><meta name=ProgId  content=Word.Document ><meta name=Generator  content="Microsoft Word 14" ><meta name=Originator  content="Microsoft Word 14" ><title></title><!--[if gte mso 9]><xml><o:DocumentProperties><o:Author>AY</o:Author><o:LastAuthor>AY</o:LastAuthor><o:Revision>1</o:Revision><o:Pages>11</o:Pages><o:Characters>9951</o:Characters></o:DocumentProperties><o:CustomDocumentProperties><o:KSOProductBuildVer dt:dt="string" >1033-11.2.0.9127</o:KSOProductBuildVer></o:CustomDocumentProperties></xml><![endif]--><!--[if gte mso 9]><xml><o:OfficeDocumentSettings></o:OfficeDocumentSettings></xml><![endif]--><!--[if gte mso 9]><xml><w:WordDocument><w:BrowserLevel>MicrosoftInternetExplorer4</w:BrowserLevel><w:DisplayHorizontalDrawingGridEvery>0</w:DisplayHorizontalDrawingGridEvery><w:DisplayVerticalDrawingGridEvery>2</w:DisplayVerticalDrawingGridEvery><w:DocumentKind>DocumentNotSpecified</w:DocumentKind><w:DrawingGridVerticalSpacing>7.8 磅</w:DrawingGridVerticalSpacing><w:View>Web</w:View><w:Compatibility><w:DontGrowAutofit/><w:BalanceSingleByteDoubleByteWidth/><w:DoNotExpandShiftReturn/></w:Compatibility><w:Zoom>0</w:Zoom></w:WordDocument></xml><![endif]--><!--[if gte mso 9]><xml><w:LatentStyles DefLockedState="false"  DefUnhideWhenUsed="true"  DefSemiHidden="true"  DefQFormat="false"  DefPriority="99"  LatentStyleCount="260" >
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Normal" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="heading 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 7" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 8" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="heading 9" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 7" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 8" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index 9" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 7" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 8" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toc 9" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Normal Indent" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="footnote text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="annotation text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="header" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="footer" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="index heading" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  QFormat="true"  Name="caption" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="table of figures" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="envelope address" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="envelope return" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="footnote reference" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="annotation reference" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="line number" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="page number" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="endnote reference" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="endnote text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="table of authorities" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="macro" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="toa heading" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Bullet" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Number" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Bullet 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Bullet 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Bullet 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Bullet 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Number 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Number 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Number 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Number 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Title" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Closing" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Signature" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  UnhideWhenUsed="false"  QFormat="true"  Name="Default Paragraph Font" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text Indent" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Continue" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Continue 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Continue 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Continue 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="List Continue 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Message Header" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Subtitle" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Salutation" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Date" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text First Indent" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text First Indent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Note Heading" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text Indent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Body Text Indent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Block Text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Hyperlink" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="FollowedHyperlink" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Strong" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Emphasis" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Document Map" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Plain Text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="E-mail Signature" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Normal (Web)" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Acronym" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Address" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Cite" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Code" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Definition" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Keyboard" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Preformatted" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Sample" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Typewriter" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="HTML Variable" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  UnhideWhenUsed="false"  QFormat="true"  Name="Normal Table" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="annotation subject" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="No List" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="1 / a / i" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="1 / 1.1 / 1.1.1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="Article / Section" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Simple 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Simple 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Simple 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Classic 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Classic 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Classic 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Classic 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Colorful 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Colorful 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Colorful 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Columns 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Columns 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Columns 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Columns 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Columns 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 7" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Grid 8" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 7" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table List 8" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table 3D effects 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table 3D effects 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table 3D effects 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Contemporary" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Elegant" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Professional" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Subtle 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Subtle 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Web 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Web 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Web 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Balloon Text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  QFormat="true"  Name="Table Grid" ></w:LsdException>
<w:LsdException Locked="false"  Priority="0"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Table Theme" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="Placeholder Text" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="No Spacing" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="List Paragraph" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="Quote" ></w:LsdException>
<w:LsdException Locked="false"  Priority="99"  SemiHidden="false"  Name="Intense Quote" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3 Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid Accent 1" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3 Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid Accent 2" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3 Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid Accent 3" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3 Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid Accent 4" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3 Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid Accent 5" ></w:LsdException>
<w:LsdException Locked="false"  Priority="60"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Shading Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="61"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light List Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="62"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Light Grid Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="63"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 1 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="64"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Shading 2 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="65"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 1 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="66"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium List 2 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="67"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 1 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="68"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 2 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="69"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Medium Grid 3 Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="70"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Dark List Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="71"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Shading Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="72"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful List Accent 6" ></w:LsdException>
<w:LsdException Locked="false"  Priority="73"  SemiHidden="false"  UnhideWhenUsed="false"  Name="Colorful Grid Accent 6" ></w:LsdException>
</w:LatentStyles></xml><![endif]--><style>
@font-face{
font-family:"Times New Roman";
}

@font-face{
font-family:"宋体";
}

@font-face{
font-family:"SimSun";
}

@font-face{
font-family:"Wingdings";
}

@font-face{
font-family:"Calibri";
}

@font-face{
font-family:"Consolas";
}

@font-face{
font-family:"Segoe UI";
}

@list l0:level1{
mso-level-number-format:alpha-lower;
mso-level-suffix:space;
mso-level-text:"%1.";
mso-level-tab-stop:none;
mso-level-number-position:left;
margin-left:0.0000pt;
text-indent:0.0000pt;
font-family:'Times New Roman';}

@list l1:level1{
mso-level-number-format:bullet;
mso-level-suffix:tab;
mso-level-text:"";
mso-level-tab-stop:21.0000pt;
mso-level-number-position:left;
margin-left:21.0000pt;text-indent:-21.0000pt;font-family:Wingdings;font-size:6.5000pt;}

@list l2:level1{
mso-level-number-format:bullet;
mso-level-suffix:tab;
mso-level-text:"";
mso-level-tab-stop:21.0000pt;
mso-level-number-position:left;
margin-left:21.0000pt;text-indent:-21.0000pt;font-family:Wingdings;font-size:6.5000pt;}

@list l3:level1{
mso-level-number-format:lower-roman;
mso-level-suffix:space;
mso-level-text:"%1.";
mso-level-tab-stop:none;
mso-level-number-position:left;
margin-left:0.0000pt;
text-indent:0.0000pt;
font-family:'Times New Roman';}

@list l4:level1{
mso-level-number-format:alpha-lower;
mso-level-suffix:space;
mso-level-text:"%1.";
mso-level-tab-stop:none;
mso-level-number-position:left;
margin-left:0.0000pt;
text-indent:0.0000pt;
font-family:'Times New Roman';}

p.MsoNormal{
mso-style-name:Normal;
mso-style-parent:"";
margin:0pt;
margin-bottom:.0001pt;
font-family:Calibri;
mso-fareast-font-family:SimSun;
mso-bidi-font-family:'Times New Roman';
}

h1{
mso-style-name:"Heading 1";
mso-style-next:Normal;
margin-top:5.0000pt;
margin-bottom:5.0000pt;
mso-margin-top-alt:auto;
mso-margin-bottom-alt:auto;
text-align:left;
font-family:SimSun;
font-weight:bold;
font-size:24.0000pt;
mso-font-kerning:22.0000pt;
}

h3{
mso-style-name:"Heading 3";
mso-style-noshow:yes;
mso-style-next:Normal;
margin-top:5.0000pt;
margin-bottom:5.0000pt;
mso-margin-top-alt:auto;
mso-margin-bottom-alt:auto;
text-align:left;
font-family:SimSun;
font-weight:bold;
font-size:13.5000pt;
}

h4{
mso-style-name:"Heading 4";
mso-style-noshow:yes;
mso-style-next:Normal;
margin-top:5.0000pt;
margin-bottom:5.0000pt;
mso-margin-top-alt:auto;
mso-margin-bottom-alt:auto;
text-align:left;
font-family:SimSun;
font-weight:bold;
font-size:12.0000pt;
}

span.10{
font-family:'Times New Roman';
}

span.15{
font-family:'Times New Roman';
color:rgb(128,0,128);
text-decoration:underline;
text-underline:single;
}

span.16{
font-family:'Times New Roman';
color:rgb(0,0,255);
text-decoration:underline;
text-underline:single;
}

span.17{
font-family:'Times New Roman';
font-weight:bold;
}

span.18{
font-family:'Times New Roman';
font-style:italic;
}

p.MsoFooter{
mso-style-name:Footer;
margin:0pt;
margin-bottom:.0001pt;
layout-grid-mode:char;
text-align:left;
font-family:Calibri;
mso-fareast-font-family:SimSun;
mso-bidi-font-family:'Times New Roman';
font-size:9.0000pt;
}

p.p{
mso-style-name:"Normal \(Web\)";
margin-top:5.0000pt;
margin-right:0.0000pt;
margin-bottom:5.0000pt;
margin-left:0.0000pt;
mso-margin-top-alt:auto;
mso-margin-bottom-alt:auto;
text-align:left;
font-family:'Times New Roman';
mso-fareast-font-family:SimSun;
font-size:12.0000pt;
}

p.pre{
mso-style-name:"HTML Preformatted";
margin:0pt;
margin-bottom:.0001pt;
text-align:left;
font-family:SimSun;
font-size:12.0000pt;
}

p.MsoHeader{
mso-style-name:Header;
margin:0pt;
margin-bottom:.0001pt;
layout-grid-mode:char;
font-family:Calibri;
mso-fareast-font-family:SimSun;
mso-bidi-font-family:'Times New Roman';
font-size:9.0000pt;
}

span.msoIns{
mso-style-type:export-only;
mso-style-name:"";
text-decoration:underline;
text-underline:single;
color:blue;
}

span.msoDel{
mso-style-type:export-only;
mso-style-name:"";
text-decoration:line-through;
color:red;
}

table.MsoNormalTable{
mso-style-name:"Table Normal";
mso-style-parent:"";
mso-style-noshow:yes;
mso-tstyle-rowband-size:0;
mso-tstyle-colband-size:0;
mso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt;
mso-para-margin:0pt;
mso-para-margin-bottom:.0001pt;
mso-pagination:widow-orphan;
font-family:'Times New Roman';
font-size:10.0000pt;
mso-ansi-language:#0400;
mso-fareast-language:#0400;
mso-bidi-language:#0400;
}

table.MsoTableGrid{
mso-style-name:"Table Grid";
mso-tstyle-rowband-size:0;
mso-tstyle-colband-size:0;
mso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt;
mso-border-top-alt:0.5000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;
mso-border-right-alt:0.5000pt solid windowtext;
mso-border-insideh:0.5000pt solid windowtext;
mso-border-insidev:0.5000pt solid windowtext;
mso-para-margin:0pt;
mso-para-margin-bottom:.0001pt;
mso-pagination:none;
text-align:justify;
text-justify:inter-ideograph;
font-family:'Times New Roman';
font-size:10.0000pt;
mso-ansi-language:#0400;
mso-fareast-language:#0400;
mso-bidi-language:#0400;
}
@page{mso-page-border-surround-header:no;
	mso-page-border-surround-footer:no;}@page Section0{
margin-top:72.0000pt;
margin-bottom:72.0000pt;
margin-left:90.0000pt;
margin-right:90.0000pt;
size:595.3000pt 841.9000pt;
layout-grid:18.0000pt;
}
div.Section0{page:Section0;}</style></head><body style="tab-interval:115pt;text-justify-trim:punctuation;" ><!--StartFragment--><div class="Section0"  style="layout-grid:18.0000pt;" ><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Following tasks are performed which includes calculating TF score, TF-IDF, PMI score and determining entropy of tweets to classify them as spam or non spam. </span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Task1. Find 10 short text-items (20-30 words); they could be emails, short docs, tweets or whatever. Make sure they all deal with some common topic of interest; so they have some of the same words.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;mso-list:l0 level1 lfo1;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:bold;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >a.<span>&nbsp;</span></span></span><![endif]><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Remove the standard stopwords from them using some standard list, use nltk.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Ans</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >: Following steps are followed to pre-process the data.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-align:justify;text-justify:inter-ideograph;
mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:bold;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >TweetTokenizer(Tokenize the tweets) -&#62; Stop word removal -&#62; Removal of special characters -&#62; Changing words to lower case -&#62; Blank space removal -&#62; Applying WordNetLemmatizer -&#62; Joined elements of multiple list to a single List</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-align:justify;text-justify:inter-ideograph;
mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >After applying the above steps on tweets below is the produced clean corpus.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-align:center;" ><img width="740"  height="152"  src="Practical4_Report.files/Practical4_Report799.png" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-align:center;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Fig: Preprocessed Tweets</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="margin-left:0.0000pt;mso-para-margin-left:0.0000gd;text-indent:0.0000pt;
mso-char-indent-count:0.0000;text-align:justify;text-justify:inter-ideograph;
mso-list:l0 level1 lfo1;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:bold;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >b.<span>&nbsp;</span></span></span><![endif]><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Compute the TF scores for all the remaining words in the texts and use R to show the word-cloud for these words. In your answer provide the matix of TF scores and the word-cloud image.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Ans:Term frequency: </span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Measures how frequently a term occurs in a document.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:bold;font-size:10.0000pt;mso-font-kerning:0.0000pt;" >TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document)</span></b><span style="mso-spacerun:'yes';font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;background:rgb(189,214,238);
mso-shading:rgb(189,214,238);" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >To create a word-cloud in python we need </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >C</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >ountVectorizer </span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >inside the package called as </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >sklearn.feature_extraction.text</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >. </span><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(189,214,238);mso-shading:rgb(189,214,238);" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Created an object of CountVectorizer as </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >cnt_vec</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >. </span><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(189,214,238);mso-shading:rgb(189,214,238);" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Performed </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >cnt_vec.fit_transform(corpus)</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >.</span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >&nbsp;</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >The fit_transform method calculates the frequency of each word in the entire sets of docs.</span><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(189,214,238);mso-shading:rgb(189,214,238);" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Now to represent calculated frequency in a table we use Dataframe. Below is the snapshot of the frequency table.</span><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(189,214,238);mso-shading:rgb(189,214,238);" ><o:p></o:p></span></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(189,214,238);mso-shading:rgb(189,214,238);" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><img width="463"  height="234"  src="Practical4_Report.files/Practical4_Report1599.png" ><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(189,214,238);mso-shading:rgb(189,214,238);" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-align:center;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Fig:Snapshot of Frequency table produced after applying TF-score</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Below is the word cloud that is produced based on the tweets corpus.</span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="358"  height="185"  src="Practical4_Report.files/Practical4_Report1736.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Fig: Word Cloud based on Tweets</span></b><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=justify  style="margin-left:0.0000pt;mso-para-margin-left:0.0000gd;text-indent:0.0000pt;
mso-char-indent-count:0.0000;text-align:justify;text-justify:inter-ideograph;
mso-list:l0 level1 lfo1;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:bold;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >c.<span>&nbsp;</span></span></span><![endif]><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Now, compute the TF-IDF scores for all the same words in the texts. Construct a set of words that represents the TF-IDF scores you have found, for all the words. Use R to show a word-cloud for these words. Also, provide the matrix of TF-IDF scores and the word-cloud image.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Ans: Inverse document frequency(IDF): </span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >The specificity of a term can be quantified as an inverse function of the number of documents in which it occurs. Actually it measures how important a term is.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >The Formula is defined as: </span><b><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:bold;font-size:10.0000pt;mso-font-kerning:0.0000pt;" >IDF(t) = log_e(Total number of documents / Number of documents with term t in it).</span></b><b><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-weight:bold;font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >TF-IDF </span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >is calculated using </span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >To calculate tf-idf in python we need a module </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >TfidfTransformer</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >&nbsp;inside package </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >sklearn.feature_extraction.text</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >fit_transform() method of TfidfTransformer is used to calculate the TF-score from pre-processed data.</span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >In the matrix below, left side shows the number of documents and the top column shows the words occuring in each document.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><img width="651"  height="187"  src="Practical4_Report.files/Practical4_Report2719.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Fig: TF-IDF Matrix</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:justify;
text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Before creating the word cloud, summation of tf-idf of each columns i.e words are calculated and a dictionary is created. Below is the snippet of the dictionary and tf-idf summation . </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:justify;
text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="297"  height="200"  src="Practical4_Report.files/Practical4_Report2927.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" >&nbsp;&nbsp;&nbsp;&nbsp;</span><img width="257"  height="199"  src="Practical4_Report.files/Practical4_Report2932.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Below is the word-cloud out of all words</span><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >&nbsp;</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="text-align:center;" ><img width="338"  height="179"  src="Practical4_Report.files/Practical4_Report2978.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-align:center;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Fig: Word cloud based on TF_IDF-Score</span></b><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Task2. Using Python or R, compute the PMI scores for all adjacent pairs of words in your 10-doc corpus (i.e the texts after stop-word removal).</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >List the top-10 pairs based on the PMI scores found for the pairs.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Do the results make sense? If not, then introduce a minimal cut-off frequency and re-compute the top-10 until they seem sensible.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
font-weight:bold;font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Ans:</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
font-weight:bold;font-size:10.0000pt;mso-font-kerning:0.0000pt;" >&nbsp;</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:normal;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Pointwise Mutual Information (PMI) </span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:normal;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >: The main intuition is that it measures how much more likely the words co-occur than if they were independent. formula is given by:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
font-weight:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
font-weight:bold;font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  align=center  style="text-align:center;" ><img width="301"  height="111"  src="Practical4_Report.files/Practical4_Report3535.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.5000pt;
mso-font-kerning:0.0000pt;" >Module required to calculate the PMI in python is </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" >nltk.collocations.BigramAssocMeasures()</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.5000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" >Corpus of 10 documents id tokenized and bigrams are found using BigramCollocationFinder.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" >The score is produced using </span><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" >bigram_measures.pmi.</span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:justify;
text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Below is the snippet of bigram with pmi score:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:justify;
text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="352"  height="297"  src="Practical4_Report.files/Practical4_Report3813.png" ><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.5000pt;
mso-font-kerning:0.0000pt;" >Top 10 pairs based on PMI score: </span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.5000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><img width="196"  height="189"  src="Practical4_Report.files/Practical4_Report3849.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" >Looking at the result it can be seen that it doesn<font face="SimSun" >&#8217;</font><font face="Calibri" >t make much sense. The issue with PMI is that it over-estimates the low frequency events because of how it treats counts.</font></span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l1 level1 lfo2;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-weight:normal;font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" >We can set a frequency filter to narrow down our result. To do so I have used apply_freq_filter(). Below is the output after applying frequency filter=2.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.5000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><img width="336"  height="496"  src="Practical4_Report.files/Practical4_Report4178.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Task</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >3.Entropy has been used to determine whether tweet set is interesting (contains variety) or repetitive</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >(spam). Create two sets of 10 made-up tweets:</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;mso-list:l4 level1 lfo3;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:bold;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >a.<span>&nbsp;</span></span></span><![endif]><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >spam-set: where the 10 tweets are very similar containing an advert for a product. </span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;mso-list:l4 level1 lfo3;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-weight:bold;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >b.<span>&nbsp;</span></span></span><![endif]><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >b. random-set: where the 10 tweets are very different, chosen at random from Twitter. Now, find a Python/R program or package that computes entropy and find the entropy values for (i)</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >spam-set, (ii) random-set, (iii) the two sets combined. Report the program you used and its source, the tweet data and the entropy values found.</span></b><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></b></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></b></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;" ><b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:bold;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Ans: </span></b><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Two sets are created, </span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:left;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >Twitter Spam set:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><img width="694"  height="161"  src="Practical4_Report.files/Practical4_Report4794.png" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-weight:normal;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:justify;
text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:left;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Random Set:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="695"  height="148"  src="Practical4_Report.files/Practical4_Report4809.png" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:justify;
text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l2 level1 lfo4;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Entropy is defined as the sum of the probability of each label times the log probability of that same label, written as H(A) = -sum(p * log(p), axis=0). It is randomness in words.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l2 level1 lfo4;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >FreqDist calculates the frequency distribution for each token and prob generates the probability of each token and entropy is returned(-sum(p*log(p with base 2))) for every probability [1]</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=justify  style="margin-left:21.0000pt;mso-para-margin-left:0.0000gd;text-indent:-21.0000pt;
mso-char-indent-count:0.0000;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l2 level1 lfo4;" ><![if !supportLists]><span style="font-family:Wingdings;mso-fareast-font-family:SimSun;mso-bidi-font-family:SimSun;
font-size:6.5000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >&#108;<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Below is the function to calculate the entropy.</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:Consolas;mso-bidi-font-family:Consolas;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><img width="350"  height="148"  src="Practical4_Report.files/Practical4_Report5229.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:center;" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l3 level1 lfo5;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >i.<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Entropy is calculated for the spam set is shown below:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="308"  height="78"  src="Practical4_Report.files/Practical4_Report5287.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l3 level1 lfo5;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >ii.<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Entropy is calculated for the random set is shown below:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="313"  height="72"  src="Practical4_Report.files/Practical4_Report5347.png" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><span style="mso-spacerun:'yes';font-family:SimSun;font-size:12.0000pt;
mso-font-kerning:0.0000pt;" ><o:p>&nbsp;</o:p></span></p><p class=pre  align=justify  style="mso-para-margin-left:0.0000gd;text-autospace:ideograph-numeric;mso-pagination:widow-orphan;
text-align:justify;text-justify:inter-ideograph;mso-list:l3 level1 lfo5;" ><![if !supportLists]><span style="font-family:Calibri;mso-fareast-font-family:SimSun;mso-hansi-font-family:SimSun;
mso-bidi-font-family:SimSun;font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><span style='mso-list:Ignore;' >iii.<span>&nbsp;</span></span></span><![endif]><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" >Combined entropy is shown below:</span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:SimSun;
mso-hansi-font-family:SimSun;mso-bidi-font-family:SimSun;font-size:10.0000pt;
mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p><p class=pre  align=center  style="text-autospace:ideograph-numeric;mso-pagination:widow-orphan;text-align:center;" ><img width="314"  height="81"  src="Practical4_Report.files/Practical4_Report5383.png" ><span style="mso-spacerun:'yes';font-family:SimSun;color:rgb(0,0,0);
font-size:9.5000pt;mso-font-kerning:0.0000pt;" ><br></span><span style="mso-spacerun:'yes';font-family:Calibri;mso-fareast-font-family:'Segoe UI';
mso-hansi-font-family:'Segoe UI';mso-bidi-font-family:SimSun;color:rgb(0,0,0);
letter-spacing:0.0000pt;font-weight:normal;text-transform:none;
font-style:normal;font-size:10.0000pt;mso-font-kerning:0.0000pt;
background:rgb(255,255,255);mso-shading:rgb(255,255,255);" ><o:p></o:p></span></p><p class=pre  align=justify  style="text-align:justify;text-justify:inter-ideograph;" ><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" >&nbsp;&nbsp;</span><span style="mso-spacerun:'yes';font-family:SimSun;mso-ascii-font-family:Calibri;
font-size:10.0000pt;mso-font-kerning:0.0000pt;" ><o:p></o:p></span></p></div><!--EndFragment--></body></html>