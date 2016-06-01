# -
这是pepXML数据模型的代码
<html><head>

	  <style type="text/css">
	      body {  font-family: Helvetica, Arial, sans-serif; font-size: 9pt; background-color: #ffffff;}
	      table{  border: 1px solid black; border-collapse: collapse; }
	       th   {  border: 1px solid black; font-family: Helvetica, Arial, sans-serif; font-size: 9pt; font-weight: bold;
	       background-color: #dddddd;}
	       td   {  border: 1px solid black; font-family: Helvetica, Arial, sans-serif; font-size: 9pt; padding:3px; vertical-align:top;}
	       table.zero{  border: 0px ; border-collapse: collapse; }
	       td.zero {  border: 0px ; font-family: Helvetica, Arial, sans-serif; font-size: 9pt; padding:3px; vertical-align:top;}
	       form   {  font-family: Helvetica, Arial, sans-serif; font-size: 9pt}
	       pre    {  font-family: Courier New, Courier; font-size: 8pt}
	       h1   {  font-family: Helvetica, Arial, sans-serif; font-size: 14pt; font-weight: bold}
	       h2   {  font-family: Helvetica, Arial, sans-serif; font-size: 12pt; font-weight: bold;
		     padding: 5px;
		     border: 2px dotted black;
		       background-color: #ddddff;
		   }
	       h3   {  font-family: Helvetica, Arial, sans-serif; font-size: 12pt}
	       h4   {  font-family: AHelvetica, rial, sans-serif; font-size: 12pt}
		.popup { COLOR: #9F141A; CURSOR: help; TEXT-DECORATION: none }
	    </style>
		</head>
<body>
<h2>Element &lt;<a name="msms_pipeline_analysis">msms_pipeline_analysis</a>&gt;</h2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>This is the root element for the Proteomics Standards Initiative (PSI) mzML schema, which is intended to capture the use of a mass spectrometer, the data generated, and the initial processing of that data (to the level of the peak list).
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:msms_pipeline_analysisType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD></TD><TD>Summary name (currently not used).</TD></TR>
<TR><TD>data</TD><TD>xs:data Time</TD><TD>required</TD><TD>Date pepXML file was written.</TD></TR>
<TR><TD>summary_xml</TD><TD>xs:string</TD><TD>required</TD><TD>Full path self reference.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#analysis_summary">analysis_summary</a></TD><TD>0</TD><TD>unlim</TD><TD>Summary of analysis subjected to run(s).</TD></TR>
<TR><TD><a href="#dataset_derivation">dataset_derivation</a></TD><TD>1</TD><TD>1</TD><TD>Source and filtering criteria used to generate dataset</TD></TR>
<TR><TD><a href="#msms_run_summary">msms_run_summary</a></TD><TD>1</TD><TD>unlim</TD><TD>Search results for LC/MS/MS run</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="01.png">
<br/>
<img width="530" src="1.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;msms_pipeline_analysis xmlns=&quot;http://reqis_web.systembiology.net/pepXML&quot; xmlns:xsi=&quot;http://www.w3.org/2001/XMLSchema-instance&quot; xsi:schemaLocation=&quot;http://regis-web.systembiology.net/pepXML/tools/bin/TPP/tpp/schema/pepXML_v18.xsd&quot; summary_xml=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/interact-highprob.pep.xml&quot; version=&quot;1.0&quot;&gt;
  &lt;ananlysis_summary count=&quot;2&quot;&gt;
    &lt;analysis analysis=&quot;database_refresh&quot; time=&quot;2009-01-22T22:29:04&quot;  /&gt;
    &lt;analysis analysis=&quot;peptideprophet&quot; time=&quot;209-01-22-T22:28:58;/&gt;
  &lt;/analysis_summary&gt;
  &lt;dataset_derivation&gt;
    &lt;msms_run_summary&gt;
  ...
&lt;/msms_pipeline_anlysis&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="peptideprophet_summary">peptideprophet_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Summary information for PeptideProphet analysis.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:peptideprophet_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>version</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>author</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>min_prob</TD><TD>xs:float</TD><TD>required</TD><TD>Min probability to be included in output</TD></TR>
<TR><TD>options</TD><TD>xs:string</TD><TD></TD><TD>User specified run options</TD></TR>
<TR><TD>est_tot_num_correct</TD><TD>xs:float</TD><TD></TD><TD>Total inferred number of correct results</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#inputfile">inputfile</a></TD><TD>1</TD><TD>unlim</TD><TD>Information about an ontology or CV source and a short 'lookup' tag to refer to.</TD></TR>
<TR><TD><a href="#roc_error_data">roc_error_data</a></TD><TD>0</TD><TD>unlim</TD><TD>Information about an ontology or CV source and a short 'lookup' tag to refer to.</TD></TR>
<TR><TD><a href="#distribution">distribution</a></TD><TD>0</TD><TD>unlim</TD><TD>Information about an ontology or CV source and a short 'lookup' tag to refer to.</TD></TR>
<TR><TD><a href="#mixture_model">mixture_model</a></TD><TD>0</TD><TD>unlim</TD><TD>Information about an ontology or CV source and a short 'lookup' tag to refer to.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="02.png">
<br/>
<img width="530" src="2.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;peptideprophet_summary count=&quot;4&quot;&gt;
  &lt;inputfile name=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/hivs100_05_1";/&gt;
  &lt;roc_data_point min_prob=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/hivs100_05_2"&quot;/&gt;
  &lt;distribution_point favlue=&quot;obs_1_distr="15" model_1_pos_distr="0.00" model_1_neg_distr="0.00" obs_2_distr="0" model_2_pos_distr="0.00" model_2_neg_distr="0.00" obs_3_distr="0" model_3_pos_distr="0.00" model_3_neg_distr="0.00" obs_4_distr="0" model_4_pos_distr="0.00" model_4_neg_distr="0.00" obs_5_distr="0" model_5_pos_distr="0.00" model_5_neg_distr="0.00" obs_6_distr="0" model_6_pos_distr="0.00" model_6_neg_distr="0.00" obs_7_distr="0" model_7_pos_distr="0.00" model_7_neg_distr="0.00";/&gt;
  &lt;mixture_model precursor_ion_charge=&quot;"1" comments="using 2+ positive distributions to identify candidates ('-1') above background ('0')" prior_probability="0.000" est_tot_correct="0.0" tot_num_spectra="8687" num_iterations="6";/&gt;
&lt;/peptideprophet_summary&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="interprophet_summary">interprophet_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Summary information for InterprophetProphet analysis.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:interprophet_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>version</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>options</TD><TD>xs:string</TD><TD></TD><TD>User specified run options</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#inutfile">inputfile</a></TD><TD>1</TD><TD>unlim</TD><TD></TD></TR>
<TR><TD><a href="#roc_error_data">roc_error_data</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
<TR><TD><a href="#mixturemodel">mixturemodel</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="03.png">
<br/>
<img width="530" src="14.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asapratio_summary">asapratio_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Quantitation
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:asapratio_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>version</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>author</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>elution</TD><TD>xs:integer</TD><TD>required</TD><TD>Elution order of light vs heavy labeled peptide</TD></TR>
<TR><TD>labeled_residues</TD><TD>xs:string</TD><TD>required</TD><TD>Aminoacids and termini that are differentially labeled for quantitaiton</TD></TR>
<TR><TD>area_flag</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD></TD></TR>
<TR><TD>static_quant</TD><TD>xs:string</TD><TD>required</TD><TD>Y if dataset is all light or heavy labeled, N if dataset is mixed heavy and light labeled</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="04.png">
<br/>
<img width="530" src="7.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="xpressratio_summary">xpressratio_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Quantitation
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:xpressratio_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>version</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>author</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>same_scan_range</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>labeled_residues</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>xpress_light</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD></TD></TR>
<TR><TD>massdiff</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>masstol</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>ppmtol</TD><TD>xs:integer</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="05.png">
<br/>
<img width="530" src="27.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="peptideprophet_result">peptideprophet_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>PeptideProphet validation results for search hit.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:peptideprophet_resultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>probability</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>all_ntt_prob</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>analysis</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#search_score_summary">search_score_summary</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="06.png">
<br/>
<img width="530" src="24.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;peptideprophet_result count=&quot;1&quot;&gt;
  &lt;search_score_summary&gt;
  &lt;parameter name=&quot;fval&quot; value=&quot;2.2193&quot;/&gt;
 &lt;/search_score_summary&gt;
 &lt;/peptideprophet_result&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="interprophet_result">interprophet_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>InterProphet validation results for search hit
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:interprophet_resultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>probability</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>all_ntt_prob</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#search_score_summary">search_score_summary</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="07.png">
<br/>
<img width="530" src="13.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asapratio_result">asapratio_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>ASAPRatio quantitation results for search hit.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:asapratio_resultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>mean</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>error</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy2light_mean</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy2light_error</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#asapratio_peptide_data">asapratio_peptide_data</a></TD><TD>1</TD><TD>1</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="08.png">
<br/>
<img width="530" src="6.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asapratio_peptide_data">asapratio_peptide_data</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:asapratio_peptide_dataType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>status</TD><TD>xs:byte</TD><TD>required</TD><TD></TD></TR>
<TR><TD>cidIndex</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>light_mass</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy_mass</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>area_flag</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#asapratio_contribution">asapratio_contribution</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="09.png">
<br/>
<img width="530" src="5.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asapratio_contribution">asapratio_contribution</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:RunType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>ratio</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>error</TD><TD>xs:float</TD><TD>optional</TD><TD></TD></TR>
<TR><TD>charge</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD></TD></TR>
<TR><TD>use</TD><TD>xs:unsignedByte</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#asapratio_lc_lightpeak">asapratio_lc_lightpeak</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
<TR><TD><a href="#asapratio_lc_heavypeak">asapratio_lc_heavypeak</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="010.png">
<br/>
<img width="530" src="3.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asaprastio_lc_lightpeak">asaprastio_lc_lightpeak</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:asaprastio_lc_lightpeakType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>status</TD><TD>xs:byte</TD><TD>required</TD><TD></TD></TR>
<TR><TD>left_valley</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>right_valley</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>background</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>area</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>area_error</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>time</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>time_width</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>is_heavy</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="011.png">
<br>
<img width="530" src="4.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asapratio_lc_heavylight">asapratio_lc_heavylight</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'></td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:asapratio_lc_heavylightType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Byte</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>status</TD><TD>xs:byte</TD><TD>required</TD><TD></TD></TR>
<TR><TD>left_valley</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>right_valley</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>background</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>area</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>area_error</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>time</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>time_width</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>is_heavy</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="012.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="database_refresh_timestamp">database_refresh_timestamp</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:database_refresh_timestampType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>database</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>min_num_enz_term</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD>minimum number of termini compaitble with enzyme used (should correspond with search enzyme constraint)</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="013.png">
<br/>
<img width="530" src="9.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>    &lt;database_refresh_timestamp&gt;
        &lt;database=&quot;/dbase/users/sbeams/ipi.HUMAN.v3.21plus.fasta&quot;/&gt;
   &lt;/analysis_timestamp&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="xpressratio_timestamp">xpressratio_timestamp</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Structure allowing the use of a controlled (cvParam) or uncontrolled vocabulary (userParam), or a reference to a predefined set of these in this mzML file (paramGroupRef).
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:xpressratio_timestampType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>xpress_light</TD><TD>xs:integer</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="014.png">
<br/>
<img width="530" src="28.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="asapratio_timestamp">asapratio_timestamp</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:asapratio_timestampType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>quant_label_masses</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>static_quant_label</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="015.png">
<br/>
<img width="530" src="8.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="xpressratio_result">xpressratio_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Quantitation.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:xpressratio_resultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>light_firstscan</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD></TD></TR>
<TR><TD>light_lastscan</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD></TD></TR>
<TR><TD>light_mass</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy_firstscan</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy_lastscan</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy_mass</TD><TD>xs:ufloat</TD><TD>required</TD><TD></TD></TR>
<TR><TD>masstol</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>ratio</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy2light_ratio</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>light_area</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>heavy_area</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>decimal_ratio</TD><TD>xs:decimal</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="016.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="interact_summary">interact_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Combined datasets
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:interact_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>filename</TD><TD>xs:string</TD><TD>required</TD><TD>Self reference</TD></TR>
<TR><TD>directory</TD><TD>xs:string</TD><TD>required</TD><TD>Directory of self</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#inputfile">inputfile</a></TD><TD>1</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="017.png">
<br/>
<img width="530" src="12.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>    &lt;interact_summary filename=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/interact-highprob.pep.xml&quot; directory=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus;&gt;
      &lt;inputfile name=&quot;hivs100_05_1.xml&quot;/&gt;
     ...
&lt;/interact_summary&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="libra_result">libra_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>libra quantitation for search hit
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:libra_resultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>is_rejected</TD><TD>xs:boolean</TD><TD>optional</TD><TD>whether or not to reject this ratio as valid</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#intensity">intensity</a></TD><TD>0</TD><TD>unlim</TD><TD>integrated mass intensity</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="018.png">
<br/>
<img width="530" src="15.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="libra_summary">libra_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>summary info for libra quantitation analysis
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:libra_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>mass_tolerance</TD><TD>xs:float</TD><TD>required</TD><TD>channel mass width</TD></TR>
<TR><TD>centroiding_preference</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>normalization</TD><TD>xs:int</TD><TD>required</TD><TD>channel used as denominator for normalized integrated intensities (0 means use channel with strongest absolute integrated intensity)</TD></TR>
<TR><TD>output_type</TD><TD>xs:int</TD><TD>required</TD><TD></TD></TR>
<TR><TD>channel_code</TD><TD>xs:string</TD><TD></TD><TD>concatenated channel masses (used as signature for defined channel masses)</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#fragment_masses">fragment_masses</a></TD><TD>0</TD><TD>unlim</TD><TD>quantitation channel</TD></TR>
<TR><TD><a href="#isotopic_contributions">isotopic_contributions</a></TD><TD>1</TD><TD>1</TD><TD>isotopic contributions from one channel to others</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="019.png">
<br/>
<img width="530" src="16.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="analysis_summary">analysis_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Summary of analysis subjected to run(s)
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:analysis_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>time</TD><TD>xs:datatime</TD><TD>required</TD><TD>Time analysis complete (unique id)</TD></TR>
<TR><TD>analysis</TD><TD>xs:string</TD><TD>required</TD><TD>Name of analysis program</TD></TR>
<TR><TD>version</TD><TD>xs:string</TD><TD></TD><TD>Release</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="###any">##any</a></TD><TD>1</TD><TD>1</TD><TD>Wildcard for summary info customized for a particular analysis</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="020.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;analysis_summary analysis=&quot;interact&quot;time=&quot;2009-01-22T22:28:51&quot;/&gt;
  &lt;interact_summary filename=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/interact-highprob.pep.xml&quot;/&gt;
    &lt;inputfile name=&quot;hivs100_05_1.xml&quot; /&gt;
    &lt;inputfile name=&quot;hivs100_05_2.xml&quot; /&gt;
   &lt;inputfile name=&quot;hivs100_06_1.xml&quot; /&gt;
   &lt;inputfile name=&quot;hivs100_06_2.xml&quot; /&gt;
  ...
&lt;/analysis_summary&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="dataset_derivation">dataset_derivation</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Source and filtering criteria used to generate dataset.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:dataset_derivationType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>generation_no</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>number preceding filter generations</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="data_filter">data_filter</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="021.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="msms_run_summary">msms_run_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Search results for LC/MS/MS run.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:msms_run_maummaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>base_name</TD><TD>xs:string</TD><TD>required</TD><TD>full path file name of mzXML (minus the .mzXML).</TD></TR>
<TR><TD>raw_data_type</TD><TD>xs:string</TD><TD>required</TD><TD>raw data type extension (e.g. .mzXML).</TD></TR>
<TR><TD>raw_data</TD><TD>xs:string</TD><TD>required</TD><TD>raw data type extension (e.g. .mzXML).</TD></TR>
<TR><TD>msManufacturer</TD><TD>xs:string</TD><TD></TD><TD>Manufacturer of MS/MS instrument.</TD></TR>
<TR><TD>msModel</TD><TD>xs:string</TD><TD></TD><TD>Instrument model (cf mzXML).</TD></TR>
<TR><TD>msIonization</TD><TD>xs:string</TD><TD></TD><TD>Instrument model (cf mzXML).</TD></TR>
<TR><TD>msMassanalyzer</TD><TD>xs:string</TD><TD></TD><TD>Ion trap, etc (cf mzXML).</TD></TR>
<TR><TD>msDetector</TD><TD>xs:string</TD><TD></TD><TD>EMT, etc(cf mzXML).</TD></TR>
<TR><TD>search_engine</TD><TD>xs:engineTypr</TD><TD></TD><TD>SEQUEST, Mascot, Comet, etc.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="sample_enzyme">sample_enzyme</a></TD><TD>1</TD><TD>1</TD><TD>Defines the net cleavage specificity of an enzyme, chemical reagent, or a mixture of these, for mass spectrometry purposes</TD></TR>
<TR><TD><a href="search_summary">search_summary</a></TD><TD>0</TD><TD>unlim</TD><TD>Database search settings</TD></TR>
<TR><TD><a href="analysis_timestamp">analysis_timestamp</a></TD><TD>0</TD><TD>unlim</TD><TD>Reference for analysis applied to current run (time corresponds with analysis_summary/@time, id corresponds with analysis_result/@id)</TD></TR>
<TR><TD><a href="spectrum_query">spctrum_query</a></TD><TD>0</TD><TD>unlim</TD><TD>MS/MS spectrum, precursor ion charge and mass</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="022.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;msms_run_summary basename=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/hivs100_05_1&quot; msManufacturer=&quot;ThermoFinnigan&quot; msModel=&quot;unknown&quot;/&gt;
     &lt;sample_enzyme name=&quot;trypsin&quot;/&gt;
      &lt;specificitye cut=&quot;KR&quot;no_cut=&quot;P&quot;/&gt;
      &lt;/sample_enzyme name/&gt;
      &lt;search_summary base_name=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/hivs100_05_1&quot; /&gt;
 ...
  &lt;/msms_run_summary&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="inputfile">inputfile</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Input file
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:inputfileType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE boeder="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none <BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="11.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;inputfile name=&quot;/regis/sbeams/archive/wyan/HIVHuCell/HIV_S100/HsIPI_v3.21plus/hivs100_05_1&quot;/&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="roc_error_data">roc_error_data</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Tag for encapsulating roc curves for pepXML
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:rocErrorDataType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE boeder="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>charge</TD><TD>xs:string</TD><TD>required</TD><TD>Charge specified or all</TD></TR>
<TR><TD>charge_est_correct</TD><TD>xs:float</TD><TD>required</TD><TD>Confidence in the esimate of the charge state</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="023.png">
<br>
<img width="530" src="26.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="distribution_point">distribtion_point</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:distribution_pointType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>fvalue</TD><TD>xs:float</TD><TD>required</TD><TD>Discriminant Score (fval) bin</TD></TR>
<TR><TD>obs_1_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 1+ spectra</TD></TR>
<TR><TD>model_1_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 1+ spectra</TD></TR>
<TR><TD>model_1_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 1+ spectra</TD></TR>
<TR><TD>obs_2_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 2+ spectra</TD></TR>
<TR><TD>model_2_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 2+ spectra</TD></TR>
<TR><TD>model_2_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 2+ spectra</TD></TR>
<TR><TD>obs_3_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 3+ spectra</TD></TR>
<TR><TD>model_3_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 3+ spectra</TD></TR>
<TR><TD>model_3_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 3+ spectra</TD></TR>
<TR><TD>obs_4_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 4+ spectra</TD></TR>
<TR><TD>model_4_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 4+ spectra</TD></TR>
<TR><TD>model_4_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 4+ spectra</TD></TR>
<TR><TD>obs_5_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 5+ spectra</TD></TR>
<TR><TD>model_5_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 5+ spectra</TD></TR>
<TR><TD>model_5_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 5+ spectra</TD></TR>
<TR><TD>obs_6_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 6+ spectra</TD></TR>
<TR><TD>model_6_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 6+ spectra</TD></TR>
<TR><TD>model_6_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 6+ spectra</TD></TR>
<TR><TD>obs_7_distr</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of 7+ spectra</TD></TR>
<TR><TD>model_7_pos_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of correct 7+ spectra</TD></TR>
<TR><TD>model_7_neg_distr</TD><TD>xs:float</TD><TD>required</TD><TD>Inferred number of incorrect 7+ spectra</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;chromatogramList count=&quot;2&quot; defaultDataProcessingRef=&quot;pwizconversion&quot;&gt;
  &lt;chromatogram index=&quot;0&quot; id=&quot;tic&quot; defaultArrayLength=&quot;15&quot; dataProcessingRef=&quot;XcaliburProcessing&quot;&gt;
    &lt;cvParam cvRef=&quot;MS&quot; accession=&quot;MS:1000235&quot; name=&quot;total ion current chromatogram&quot; value=&quot;&quot;/&gt;
    &lt;binaryDataArrayList count=&quot;2&quot;&gt;
      &lt;binaryDataArray encodedLength=&quot;160&quot; dataProcessingRef=&quot;pwizconversion&quot;&gt;
        &lt;cvParam cvRef=&quot;MS&quot; accession=&quot;MS:1000523&quot; name=&quot;64-bit float&quot; value=&quot;&quot;/&gt;
        &lt;cvParam cvRef=&quot;MS&quot; accession=&quot;MS:1000576&quot; name=&quot;no compression&quot; value=&quot;&quot;/&gt;
  ...
&lt;/chromatogramList&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="mixture_model">mixture_model</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:mixturemodelType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>precursor_ion_charge</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD></TD></TR>
<TR><TD>comment</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>prior_probability</TD><TD>xs:float</TD><TD>required</TD><TD>Fraction of results inferred to be correct</TD></TR>
<TR><TD>est_tot_corret</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>tot_num_spectra</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of input spectra</TD></TR>
<TR><TD>num_iterations</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Number of EM interations prior to convergence</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#mixturemodel_distribution">mixturemodel_distribution</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
<TR><TD><a href="#mixturemodel">mixturemodel</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="024.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>  &lt;mixture_model precursor_ion_charge=&quot;1&quot; comments=&quot;using 2+ positive diatributions to identify candidates('-1')sbove background('0')&quot;&gt;
        &lt;mixturemodel_distribuion name=&quot;SEQUEST discrimscore[]fval negmean: -1.83&quot; /&gt;
        &lt;posmodel_distribution type=&quot;gaussian&quot;/&gt;
        &lt;parameter name=&quot;mean&quot; value=&quot;1.36&quot;/&gt;
      &lt;/mixture_model&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="mixturemodel">mixturmodel</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:mixtureModelType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>pos_bandwidth</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>neg_bandwidth</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#point">point</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="025.png">
<br>
<img width="530" src="18.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="search_score_summary">search_score_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:search_score_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#parameter">parameter</a></TD><TD>2</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="026.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;search_score_summary count=&quot;5&quot;&gt;
  &lt;parameter name=&quot;fval&quot;/&gt;
  &lt;parameter name=&quot;ntt&quot;/&gt;
  &lt;parameter name=&quot;nmc&quot;/&gt;
  &lt;parameter name=&quot;massd&quot;/&gt;
  &lt;parameter name=&quot;icat&quot;/&gt;
&lt;/search_score_summary&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="intensity">intensity</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>integrated mass intensity
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:intensityType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>channel</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>mass channel number.</TD></TR>
<TR><TD>target_mass</TD><TD>xs:float</TD><TD>required</TD><TD>mass of channel.</TD></TR>
<TR><TD>absolute</TD><TD>xs:float</TD><TD>required</TD><TD>normalized integrated intensity (normalization channel stored in libra_summary).</TD></TR>
<TR><TD>normalized</TD><TD>xs:float</TD><TD>required</TD><TD>mass channel number.</TD></TR>
<TR><TD>reject</TD><TD>xs:boolean</TD><TD>optional</TD><TD>whether or not to reject this ratio as valid.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="fragment_masses">fragment_masses</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>quantitation channel
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:fragmentMassesType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>channel</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>channel number</TD></TR>
<TR><TD>mz</TD><TD>xs:flost</TD><TD>required</TD><TD>channel mass</TD></TR>
<TR><TD>offset</TD><TD>xs:float</TD><TD></TD><TD>mass offset from mz value</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>


<H2>Element &lt;<a name="isotopic_contributions">isotopic_contributions</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>isotopic contributions from one channel to others
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:isotopicContributionsType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#contributing_channel">contributing_channel</a></TD><TD>0</TD><TD>unlim</TD><TD>channel donnor.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="027.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>      &lt;softwareRef ref=&quot;Xcalibur&quot;/&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="##any">##any</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Wildcard for summary info customized for a particular analysis
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:##anyType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="data_filter">data_filter</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:data_filterType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>number</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD></TD></TR>
<TR><TD>parent_file</TD><TD>xs:string</TD><TD>required</TD><TD>File from which derived</TD></TR>
<TR><TD>windows_parent</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>description</TD><TD>xs:string</TD><TD>required</TD><TD>filtering criteria applied to data</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="sample_enzyme">sample_enzyme</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Defines the net cleavage specificity of an enzyme, chemical reagent, or a mixture of these, for mass spectrometry purposes
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:sample_enzymeType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:</TD><TD>required</TD><TD>Controlled code name for the enzyme that can be referred to by applications</TD></TR>
<TR><TD>description</TD><TD>xs:string</TD><TD>optional</TD><TD>Free text to describe alternative names, special conditions, etc</TD></TR>
<TR><TD>fidelity</TD><TD>xs:</TD><TD>optional</TD><TD>Semispecific means that at least one end of a pepide must conform to the cleavage specificity, (unless the peptide was at the terminus of the parent sequence). Nonspecific means that neither end of a peptide must conform to the cleavage specificity.</TD></TR>
<TR><TD>independent</TD><TD>xs:boolean</TD><TD>optional</TD><TD>If there are multiple specificities and independent is true, then a single peptide cannot exhibit one specificity at one terminus and a different specificity at the other. If independent is false, then a single peptide can exhibit mixed specificities.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#specificity">specificity</a></TD><TD>0</TD><TD>unlim</TD><TD>Component cleavage specificity. Must be at least one specificity unless enzymeType:fidelity is nonspecific</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="028.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;asmple_enzyme name=&quot;trypsin&quot;&gt;
  &lt;specifity cut=&quot;KR&quot; no_cut=&quot;P&quot; sense=&quot;C&quot;/&gt;
 &lt;/sample_enzyme&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="search_summary">search_summary</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Database search settings
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:search_summaryType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>base_name</TD><TD>xs:string</TD><TD>required</TD><TD>Full path location of mzXML file for this search run (without the .mzXML extension)</TD></TR>
<TR><TD>search_engine</TD><TD>xs:engineType</TD><TD>required</TD><TD>SEQUEST, Mascot, Comet, etc</TD></TR>
<TR><TD>search_engine_version</TD><TD>xs:string</TD><TD>optional</TD><TD>Search engine version string</TD></TR>
<TR><TD>precursor_mass_type</TD><TD>xs:massType</TD><TD>required</TD><TD>average or monoisotopic</TD></TR>
<TR><TD>fragment_mass_type</TD><TD>xs:massType</TD><TD>required</TD><TD>average or monoisotopic</TD></TR>
<TR><TD>out_data_type</TD><TD>xs:string</TD><TD>optional</TD><TD>Format of file storing the runner up peptides (if not present in pepXML)</TD></TR>
<TR><TD>out_data</TD><TD>xs:string</TD><TD>optional</TD><TD>runner up search hit data type extension (e.g. .tgz)</TD></TR>
<TR><TD>search_id</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>matches id in search hit</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#search_database">search_databasef</a></TD><TD>1</TD><TD>1</TD><TD>Full path address of database on local computer</TD></TR>
<TR><TD><a href="#enzymatic_search_constraint">enzymatic_search_constraint</a></TD><TD>1</TD><TD>1</TD><TD>Required peptide termini</TD></TR>
<TR><TD><a href="#sequence_search_constraint">sequence_search_constraint</a></TD><TD>0</TD><TD>unlim</TD><TD>Required amino acid string</TD></TR>
<TR><TD><a href="#aminoacid_modification">aminoacid_modification</a></TD><TD>0</TD><TD>unlim</TD><TD>Modified aminoacid, static or variable</TD></TR>
<TR><TD><a href="#terminal_modification">terminal_modification</a></TD><TD>0</TD><TD>unlim</TD><TD>Modification to the N or C terminus, static or variable</TD></TR>
<TR><TD><a href="#parmeter">parameter</a></TD><TD></TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="029.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;sourceFileRef ref=&quot;sf_parameters&quot;/&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="analysis_timestamp">analysis_timestamp</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Reference for analysis applied to current run (time corresponds with analysis_summary/@time, id corresponds with analysis_result/@id).
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:analysis_timestampType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>time</TD><TD>xs:dateTime</TD><TD>required</TD><TD>Date of analysis</TD></TR>
<TR><TD>analysis</TD><TD>xs:string</TD><TD>required</TD><TD>Analysis name</TD></TR>
<TR><TD>id</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>Unique identifier for each type of analysis</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="###any">##any</a></TD><TD>1</TD><TD>1</TD><TD>Wildcard for timestamp info customized for a particular analysis.</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;target&gt;
  &lt;userParam name=&quot;precursorMz&quot; value=&quot;123.456&quot;/&gt;
  &lt;userParam name=&quot;fragmentMz&quot; value=&quot;456.789&quot;/&gt;
  &lt;userParam name=&quot;dwell time&quot; value=&quot;1&quot; type=&quot;seconds&quot;/&gt;
  &lt;userParam name=&quot;active time&quot; value=&quot;0.5&quot; type=&quot;seconds&quot;/&gt;
&lt;/target&gt;
</PRE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="030.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example cvParams:</b></td>
<td class='zero'><PRE>&lt;cvParam cvRef=&quot;MS&quot; accession=&quot;MS:1000744&quot; name=&quot;selected ion m/z&quot; value=&quot;1000&quot; unitCvRef=&quot;MS&quot; unitAccession=&quot;MS:1000040&quot; unitName=&quot;m/z&quot;/&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="spectrum_query">spectrum_query</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>MS/MS spectrum, precursor ion charge and mass.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:spectrumType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>specturm</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>start_scan</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD>first scan number integrated into MS/MS spectrum</TD></TR>
<TR><TD>end_scan</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD>last scan number integrated into MS/MS spectrum</TD></TR>
<TR><TD>retention_time_sec</TD><TD>xs:float</TD><TD>optional</TD><TD>retention time associated with start_scan</TD></TR>
<TR><TD>collision_energy</TD><TD>xs:float</TD><TD>optional</TD><TD>Collision energy used to fragment the parent ion.</TD></TR>
<TR><TD>compensation_voltage</TD><TD>xs:float</TD><TD>optional</TD><TD>The DC potential applied to the asymmetric waveform in FAIMS that compensates for the difference between high and low field mobility of an ion.</TD></TR>
<TR><TD>precursor_intensity</TD><TD>xs:float</TD><TD>optional</TD><TD>Intensity of precursor ion.</TD></TR>
<TR><TD>activation_method</TD><TD>xs:activationMethodType</TD><TD>optional</TD><TD>Activation or fragmentation method: ETD, ECD, CID, etc</TD></TR>
<TR><TD>precursor_neutral_mass</TD><TD>xs:float</TD><TD>required</TD><TD></TD></TR>
<TR><TD>assumed_chasrge</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Precursor ion charge used for search</TD></TR>
<TR><TD>search_specification</TD><TD>xs:string</TD><TD></TD><TD>Search constraint applied specifically to this query</TD></TR>
<TR><TD>index</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>Unique identifier</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#search_result">search_result</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="031.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;spectrum_query spectrum=&quot;hivs100_05_2.3568.3568.3&quot;&gt;
  &lt;search_result&gt
  &lt;search_hit hit_rank=&quot;1&quot; peptide=&quot;AEDLDACNLKRR&quot; peptide_prev_aa=&quot;K&quot; protein=&quot;IPI00294749&quot;/&gt;
  &lt;modification modified_peptide=&quot;AEDLDAC[339]NLKRR&quot; /&gt;
  &lt;mod_aminoacid_mass position=&quot;7&quot; mass=&quot;339.268800&quot; /&gt;
  ...
&lt;/spectrum_query&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="mixturemodel_distribution">mixturemodel_distribution</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:mixturemodel_distributionType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#posmodel_distribution">posmodel_distribution</a></TD><TD>1</TD><TD>1</TD><TD></TD></TR>
<TR><TD><a href="#negmodel_distribution">negmodel_distribution</a></TD><TD>1</TD><TD>1</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="032.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;mixture_distribution name=&quot;SEQUEST discrim score[fval]  negmean: -1.83&quot;&gt;
  &lt;posmodel_distribution type=&quot;gaussian&quot; /&gt;
  &lt;parameter name=&quot;mean&quot;value=&quot;1.36&quot; /&gt;
....
&lt;/mixture_distribution&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="mixturemodel">mixturemodel</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:mixturemodelType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>pos_bandwidth</TD><TD>xs:float</TD><TD></TD><TD></TD></TR>
<TR><TD>neg_bandwidth</TD><TD>xs:float</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#point">point</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="033.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>bone<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="parameter">parameter</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:nameValueType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>value</TD><TD>xs:anySimpleType</TD><TD>required</TD><TD></TD></TR>
<TR><TD>type</TD><TD>xs:anySimpleType</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="21.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;parameter name=&quot;mean&quot;value=&quot;&quot;&gt;
  ...
&lt;/parameter&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="contributing_channel">contributing_channel</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>channel donor
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:conbutringChannelType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>channel</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>channel number</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#affected_channel">affected_channel</a></TD><TD>0</TD><TD>unlim</TD><TD>channel recipient</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="034.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="specificity">specificity</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Component cleavage specificity. Must be at least one specificity unless enzymeType:fidelity is nonspecific
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:specificityType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>sense</TD><TD>xs:string</TD><TD>required</TD><TD>Defines whether cleavage occurs on the C-terminal or N-terminal side of the residue(s) listed in cut</TD></TR>
<TR><TD>min_spacing</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD>minimum separation between adjacent cleavages</TD></TR>
<TR><TD>cut</TD><TD>xs:string</TD><TD>required</TD><TD>One or more 1-letter residue codes. Enzyme cleaves on the sense side of the residue(s) listed in cut unless one of the residues listed in no_cut is adjacent to the potential cleavage site</TD></TR>
<TR><TD>no_cut</TD><TD>xs:string</TD><TD>required</TD><TD>Zero or more 1-letter residue codes. Enzyme cleaves on the sense side of the residue(s) listed in cut unless one of the residues listed in no_cut is adjacent to the potential cleavage site</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;specifity cut=&quot;KR&quot;no_cut=&quot;P&quot;sense=&quot;C&quot;&gt;
 &lt;/specificity&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="search_database">search_database</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:search_databaseType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>local_path</TD><TD>xs:string</TD><TD>required</TD><TD>Full path address of database on local computer</TD></TR>
<TR><TD>URl</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>database_name</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>orig_database_url</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>database_release_data</TD><TD>xs:dataTime</TD><TD></TD><TD></TD></TR>
<TR><TD>database_release_identifier</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>size_in_db_entries</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD></TD></TR>
<TR><TD>size_of_residues</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD></TD></TR>
<TR><TD>type</TD><TD>xs:string</TD><TD>required</TD><TD>Database type (AA=amino acid, NA=nucleic acid)</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;search_database local_path=&quot;/dbase/users/sbeams/ipi.HUMAN.v3.21plus.fasta&quot;type=&quot;AA&quot;&gt;
&lt;/search_database&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="enzymatic_search_constraint">enzymatic_search_constraint</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Required peptide termini
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:enzymaticSearchConstraintType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>enzyme</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>max_num_internal_cleavage</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Maximum number of enzyme cleavage sites allowable within peptide</TD></TR>
<TR><TD>min_number_termini</TD><TD>xs:nonNegativeInteger</TD><TD>required</TD><TD>Minimum number of termini compatible with enzymatic cleavage</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;enzymatic_search_constrait enzyme=&quot;Trypsin&quot;max_num_internal_cleavages=&quot;2&quot;min_number_termini=&quot;1&quot;&gt;
  &lt;/enzymatic_search_constrait&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="sequence_search_constraint">sequence_search_constraint</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Required amino acid string
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:SequenceSearchCconstraintType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>sequence</TD><TD>xs:string</TD><TD>required</TD><TD>Required amino acid string</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="aminoacid_modification">aminoacid_modification"</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Modified aminoacid, static or variable
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:aminoacidModificationType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>aminoacid</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>massdiff</TD><TD>xs:string</TD><TD>required</TD><TD>Mass difference with respect to unmodified aminoacid, must begin with either + (nonnegative) or - [e.g. +1.05446 or -2.3342]</TD></TR>
<TR><TD>mass</TD><TD>xs:float</TD><TD>required</TD><TD>Mass of modified aminoacid</TD></TR>
<TR><TD>varible</TD><TD>xs:string</TD><TD>required</TD><TD>Y if both modified and unmodified aminoacid could be present in the dataset, N if only modified aminoacid can be present</TD></TR>
<TR><TD>peptide_terminus</TD><TD>xs:string</TD><TD>required</TD><TD>whether modification can reside only at protein terminus (specified 'n', 'c', or 'nc')</TD></TR>
<TR><TD>symbol</TD><TD>xs:aa_symbolType</TD><TD>required</TD><TD>Special symbol used by search engine to designate this modification</TD></TR>
<TR><TD>binary</TD><TD>xs:string</TD><TD>required</TD><TD>Y if each peptide must have only modified or unmodified aminoacid, N if a peptide may contain both modified and unmodified aminoacid</TD></TR>
<TR><TD>description</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;aminoacid_modification aminoacid=&quot;C&quot;mass=&quot;9.0000&quot;mass=&quot;339.2688&quot;&gt;
  &lt;/amonoacid_modification&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="terminal_modification">terminal_modification</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Modification to the N or C terminus, static or variable
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:TerminalModificationType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>terminus</TD><TD>xs:string</TD><TD>required</TD><TD>n for N-terminus, c for C-terminus</TD></TR>
<TR><TD>massdiff</TD><TD>xs:string</TD><TD>required</TD><TD>Mass difference with respect to unmodified terminus</TD></TR>
<TR><TD>mass</TD><TD>xs:float</TD><TD>required</TD><TD>Mass of modified terminus</TD></TR>
<TR><TD>varible</TD><TD>xs:string</TD><TD>required</TD><TD>Y if both modified and unmodified terminus could be present in the dataset, N if only modified terminus can be present</TD></TR>
<TR><TD>symbol</TD><TD>xs:term_symbolType</TD><TD></TD><TD>Special symbol used by search engine to designate this modification</TD></TR>
<TR><TD>protein_terminus</TD><TD>xs:string</TD><TD>required</TD><TD>whether modification can reside only at protein terminus (specified n or c)</TD></TR>
<TR><TD>description</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="parameter">parameter</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:parameterType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>value</TD><TD>xs:anySimpleType</TD><TD>required</TD><TD></TD></TR>
<TR><TD>type</TD><TD>xs:anySimpleType</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>

<H2>Element &lt;<a name="search_result">search_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:searchresultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>search_id</TD><TD>xs:positiveInt</TD><TD></TD><TD>Unique identifier to search summary</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#search_hit">search_hit</a></TD><TD>0</TD><TD>unlim</TD><TD>Peptide assignment</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="035.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;search_result&gt;
  &lt;search_hit hit_rank=&quot;1&quot; peptide=&quot;AEDLDACNLKRR&quot; peptide_prev_aa=&quotK&quot;/&gt;
  &lt;modification_info modified_peptide=&quot;AEDLDAC[339.268800]NLKRR&quot; /&gt;
  ...
  &lt;search_score name=&quot;xcorr&quot; value=&quot;02.644&quot; /&gt;
..
&lt;/search_result&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="posmodel_distribution">posmodel_distribution</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:posmodel_distributionType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>type</TD><TD>xs:model_dis_type</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#parameter">parameter</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="036.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>            &lt;posmodel_distribution type=&quot;gaussian&quot;&gt;
             &lt;parameter name=&quot;mean&quot;value=&quot;1.36&quot;/&gt;
                &lt;parameter name=&quot;stdev&quot;value=&quot;0.39&quot;/&gt   
            &lt;/posmodel_distribution&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="negmodel_distribution">negmodel_distribution</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:negmodelDiatributionType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>type</TD><TD>xs:model_dis_type</TD><TD>required</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#parameter">parameter</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;negmodel_distribution&gt;
  &lt;parameter name=&quot;m1&quot; value=&quot;0.91&quot;0.75&quot;/&gt;
&lt;/negmodel_distribution&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="point">point</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:PointType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>value</TD><TD>xs:float</TD><TD></TD><TD></TD></TR>
<TR><TD>pos_dens</TD><TD>xs:float</TD><TD></TD><TD></TD></TR>
<TR><TD>neg_dens</TD><TD>xs:float</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="affected_channel">affected_channel</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>channel recipient.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>xs:affectedChannelType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>channel</TD><TD>xs:positiveInt</TD><TD>required</TD><TD>channel number</TD></TR>
<TR><TD>correction</TD><TD>xs:float</TD><TD>required</TD><TD>fraction of affected channel due to contributing</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>&lt;binary&gt;&lt;/binary&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="search_hit">search_hit</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Peptide assignmen.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:search_hitType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>hit_rank</TD><TD>xs:positiveInt</TD><TD>required</TD><TD></TD></TR>
<TR><TD>peptide</TD><TD>xs:string</TD><TD>required</TD><TD>Peptide aminoacid sequence (with no indicated modifications)</TD></TR>
<TR><TD>peptide_prev_aa</TD><TD>xs:string</TD><TD></TD><TD>Aminoacid preceding peptide (- if none)</TD></TR>
<TR><TD>peptide_next_aa</TD><TD>xs:string</TD><TD></TD><TD> Aminoacid following peptide (- if none)</TD></TR>
<TR><TD>protein</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>num_tot_proteins</TD><TD>xs:unsignedInt</TD><TD>required</TD><TD>Number of unique proteins in search database containing peptide</TD></TR>
<TR><TD>num_matched_ions</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD>Number of unique proteins in search database containing peptide</TD></TR>
<TR><TD>tot_num_ions</TD><TD>xs:nonNefativeInteger</TD><TD></TD><TD>Number of peptide fragment ions found in spectrum</TD></TR>
<TR><TD>calc_neutral_pep_mass</TD><TD>xs:float</TD><TD>required</TD><TD>Number of peptide fragment ions predicted for peptide</TD></TR>
<TR><TD>massdiff</TD><TD>xs:string</TD><TD></TD><TD>Mass(precursor ion) - Mass(peptide)</TD></TR>
<TR><TD>num_tol_term</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD>Number of peptide termini consistent with cleavage by sample enzyme</TD></TR>
<TR><TD>num_missed_cleavages</TD><TD>integer</TD><TD></TD><TD>Number of sample enzyme cleavage sites internal to peptide</TD></TR>
<TR><TD>num_matched_peptides</TD><TD>integer</TD><TD></TD><TD>Number of matched peptide entries in the sequence database</TD></TR>
<TR><TD>is_rejected</TD><TD>nonNegativeInteger</TD><TD></TD><TD>Potential use in future for user manual validation (0 or 1)</TD></TR>
<TR><TD>protein_descr</TD><TD>string</TD><TD></TD><TD>Extracted from search database</TD></TR>
<TR><TD>calc_pI</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>protein_mw </TD><TD>xs:double</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#alternative_proein">alternative_protein</a></TD><TD>0</TD><TD>unlim</TD><TD>Other protein in search database that contains peptide</TD></TR>
<TR><TD><a href="#modification_info">modification_info</a></TD><TD>1</TD><TD>1</TD><TD>Positions and masses of modifications</TD></TR>
<TR><TD><a href="#search_score">search_score</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
<TR><TD><a href="#analysis_result">analysis_result</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
<TR><TD><a href="#parameter">parameter</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="037.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>              &lt;search_hit hit_rank=&quot;1&quot; peptide=&quot;QNPDIPQLEPSDYLK&quot;peptide_prev_aa=&quot;R&quot;peptide_next_aa=&quot;K&quot;&gt;
                &lt;search_score name=&quot;xcorr&quot; value=&quot;2.104&quot;/&gt;
                ...
                &lt;analysis_result nanlysis=&quot;peptideprophetS&quot;/&gt;
                ....
                 &lt;/analysis_resul&gt;
              ....
&lt;/selectedIon&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="parameter">parameter</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Peptide assignmen.
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:parameterType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>value</TD><TD>xs:anySimpleType</TD><TD>required</TD><TD></TD></TR>
<TR><TD>type</TD><TD>xs:anySimpleType</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>              &lt;parameter&gt;
                &lt;parameter name=&quot;fval&quot; value=&quot2.1683&quot;/&gt;
            &lt;/parameter&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="alternative_protein">alternative_protein</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Other protein in search database that contains peptide
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:alternativeType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>protein</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>protein_descr</TD><TD>xs:string</TD><TD></TD><TD></TD></TR>
<TR><TD>num_tol_term</TD><TD>xs:nonNegativeInteger</TD><TD></TD><TD></TD></TR>
<TR><TD>protein_mw</TD><TD>xs:double</TD><TD></TD><TD></TD></TR>
<TR><TD>peptide_prev_aa</TD><TD>xs:string</TD><TD></TD><TD> Aminoacid following peptide (- if none)</TD></TR>
<TR><TD>peptide_next_aa</TD><TD>xs:string</TD><TD></TD><TD>Aminoacid following peptide (- if none)</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>              &lt;alternative_protein&gt;
                &lt;protein=&quot;IPI00643732&quot; protein_descr=&quot;IPI:IPI00643270.1|TREMBL:Q5TBN4|VEGA:OTTHUMP00000018361 Tax_Id=9606 Lymphocyte cytosolic protein 1&quot; num_tol_term=&quot;2&quot; peptide_prev_aa=&quot;K&quot; peptide_next_aa=&quot;E&quot;/&gt;
           &lt;/alternative_protein&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="modification_info">mdification_info</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>Positions and masses of modifications
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:modificatonType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>mod_nterm_mass</TD><TD>xs:double</TD><TD></TD><TD>Mass of modified N terminus</TD></TR>
<TR><TD>mod_cterm_mass</TD><TD>xs:double</TD><TD></TD><TD>Mass of modified C terminus</TD></TR>
<TR><TD>modified_pepitide</TD><TD>xs:string</TD><TD></TD><TD>Peptide sequence (with indicated modifications)</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="#mod_aminoacid_mass">mod_aminoacid_mass</a></TD><TD>0</TD><TD>unlim</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="038.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>     &lt;modification_info modified-peptide=&quot;IENC[339]NYAVEGKNKAK&gt;
                &lt;mod_aminoacid_mass position=&quot;4&quot; mass=&quot;339.268800&quot;/&gt;
        &lt;/modification_info&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="search_score">search_score</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:search_scoreType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>name</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>value</TD><TD>xs:anySimpleType</TD><TD>required</TD><TD></TD></TR>
<TR><TD>type</TD><TD>xs:anySimpleType</TD><TD></TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>   &lt;search_score name=&quot;xcorr&quot;value=&quot;3.965&quot;&gt;
  &lt;/search_score&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="analysis_result">analysis_result</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:analysis_resultType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>analysis</TD><TD>xs:string</TD><TD>required</TD><TD></TD></TR>
<TR><TD>id</TD><TD>xs:positiveInt</TD><TD>1</TD><TD></TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Subelement Name</TH><TH>min</TH><TH>max</TH><TH>Definition</TH></TR>
<TR><TD><a href="###any">##any</a></TD><TD>0</TD><TD>unlim</TD><TD>Wildcard for result info customized for a particular analysis</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Graphical Context:</b></td>
<td class='zero'><img width="530" src="039.png">
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE>              &lt;analysis_result analysis=&quot;peptideprophet&quot;&gt;
                &lt;peptideprophet_result probability=&quot;0.9985&quot;all_ntt_prob=&quot;(0.0000,0.8600,0.9985)&quot;/&gt;
                &lt;search_score_summary&gt;
                &lt;/search_score_summary&gt;
 &lt;/analysis_result&gt;
</PRE>
</td>
</tr>
</table><br/>

<H2>Element &lt;<a name="mod_aminoacid_mass">mod_aminoacid_mass</a>&gt;</H2>

<table class='zero'>
<tr>
<td class='zero'><b>Definition:</b></td>
<td class='zero'>
</td>
</tr>
<tr>
<td class='zero'><b>Type:</b></td>
<td class='zero'>dx:mod_aminoacid_massType
</td>
</tr>
<tr>
<td class='zero'><b>Attributes:</b></td>
<td class='zero'><TABLE border="1">
<TR><TH>Attribute Name</TH><TH>Data Type</TH><TH>Use</TH><TH>Definition</TH></TR>
<TR><TD>position</TD><TD>xs:nonNedativeInteger</TD><TD>required</TD><TD>modified aminoacid position in peptide [ranging from 1 to peptide length]</TD></TR>
<TR><TD>mass</TD><TD>xs:double</TD><TD>required</TD><TD>modified mass of aminoacid</TD></TR>
</TABLE>
</td>
</tr>
<tr>
<td class='zero'><b>Subelements:</b></td>
<td class='zero'>none<BR>
</td>
</tr>
<tr>
<td class='zero'><b>Example Context:</b></td>
<td class='zero'><PRE> &lt;mod_aminoacid_mass position=&quot;6&quot;mass=&quot;339.268800&quot;&gt;
              
 &lt;/mod_aminoacid_mass&gt;
</PRE>
</td>
</tr>
</table><br/>


</body></html>
