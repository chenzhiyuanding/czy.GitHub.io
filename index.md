<html xmlns:v="urn:schemas-microsoft-com:vml"
xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:w="urn:schemas-microsoft-com:office:word"
xmlns:m="http://schemas.microsoft.com/office/2004/12/omml"
xmlns="http://www.w3.org/TR/REC-html40">

<body lang=ZH-CN link="#0563C1" vlink="#954F72" style='tab-interval:21.0pt;
word-wrap:break-word;text-justify-trim:punctuation'>

<div class=WordSection1 style='layout-grid:15.6pt'>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>Intelligent home pregnancy
management method based on multi-modal data fusion<o:p></o:p></span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>Yin Wang<sup>1</sup>, <span
class=SpellE>Zhiwei</span> Zuo<sup>1</sup>, Wei Wang<sup>1</sup>, <span
class=SpellE>Nuan</span> <span class=SpellE>Qiu</span> <sup>1*</sup><o:p></o:p></span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><sup><span lang=EN-US style='font-size:14.0pt'>1</span></sup><span
lang=EN-US> </span><span lang=EN-US style='font-size:14.0pt'>Beijing <span
class=SpellE>Aikangtai</span> Technology Co., Ltd., Beijing, China<o:p></o:p></span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>Email: </span><span lang=EN-US><a
href="mailto:qiun@ikangtai.com"><span style='font-size:14.0pt'>qiun@ikangtai.com</span></a></span><span
class=MsoHyperlink><span lang=EN-US style='font-size:14.0pt'><o:p></o:p></span></span></p>

<p class=MsoNormal><span lang=EN-US>Abstract: With the issuance of the national
three-child policy, the field of female reproduction has attracted more and
more attention. To care for female reproductive health and help the implementation
of the government's three child policy, we have proposed an intelligent home
pregnancy preparation management method based on multimodal data fusion, namely
FAM (Fertility Awareness Method, FAM). This method introduces big data,
multimodal data fusion and image recognition technology. By inputting
multi-modal data such as menstrual cycle, basal body temperature, ovulation
test paper and cervical mucus of the pregnant woman, it can automatically
predict the ovulation day and menstrual period information of the pregnant
woman. This improves the pregnancy success rate of pregnant women, breaks the
limitations of the traditional method of finding the ovulation day through
monomodal data, and facilitates the monitoring of pregnant women at home.
Finally, compared with the single-mode method qualitatively and quantitatively,
the preliminary experimental results show that the accuracy of FAM method in
identifying ovulation date is as high as 89%, and the accuracy in predicting menstrual
period is as high as 93%, and the pregnancy success rate of pregnant women can
be increased to 273% in at least nine cycles. </span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>Key words: multimodal
data fusion; FAM; ovulation day; menstrual period information</span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>INCTRODCTION<o:p></o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>In recent years,
multimodal data fusion technology has become popular in the medical field as a
kind of deep learning technology, and it plays a very important role in
assisting clinical diagnosis and condition prediction of diseases. With the
country's full liberalization and encouragement of three births, female
reproductive health will become a major focus of the medical field, and the
application of deep learning technology to the field of female reproductive
health is bound to become a major trend. Therefore, to care for female
reproductive health and help the government implement the three-child policy,
we propose an intelligent home pregnancy management method based on multi-modal
data fusion.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>First of all,
this method can help pregnant women to get pregnant quickly and naturally by
predicting the next menstrual period and finding the ovulation day. The key to
rapid natural pregnancy is to find the ovulation date of pregnant women. As
long as the ovulation date is found, the roommate shall be arranged in time, pregnancy
is a natural thing (except for patients with reproductive diseases)! However,
the traditional methods of finding the ovulation day mostly use monomodal data,
two-dimensional or three-dimensional modal data to predict the ovulation day of
pregnant women. </span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>For example, the
basal body temperature prediction method for ovulation is the oldest, simplest
and most widely used method, which is still used today. But most people think
that this method is retrospective and can only determine the presence or
absence of ovulation, and cannot predict the time of ovulation. There is also
the earliest cervical mucus observation method proposed by Australian doctor
Dr. Billings<sup> [1]</sup>, which predicts the occurrence of ovulation by
feeling, touching and observing the properties of cervical mucus with the naked
eye. This method usually requires continuous observation for multiple cycles, a
long time and the evaluation of cervical mucus is subjective. Or the menstrual
calendar method developed later, Marcos et al.<sup> [2]</sup> designed a fixed
formula to input the menstrual information of the previous cycle to calculate
the next menstrual period and the fertile period, thereby predicting the ovulation
day, although it is more convenient than the cervical mucus observation method
It saves time, but this method is not suitable for women with irregular cycles.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>Later, <span
class=SpellE>Yussman</span> et al.<sup> [3]</sup> used the method of measuring
the blood LH value and <span class=SpellE>Kratochvil</span> first reported in
1972 that the follicles were examined by ultrasound<sup> [4]</sup>, which was
later the B-ultrasound used in the hospital. Although the above two methods are
accurate, they both require patients to go to the hospital for multiple
inspections. The inspection costs are relatively high, which is bound to
increase the financial burden of the family. Later, the LH test strips were
produced so that all women who were preparing for pregnancy could be tested at
home to predict the day of ovulation. It is also very important for many
infertility patients to predict ovulation. This was also verified in the
experiment of Corson et al<sup> [5]</sup>. However, LH test paper testing is
usually combined with basal body temperature testing.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>In summary,
through the understanding and analysis of the above methods for finding
ovulation days, we found that few people can integrate these important data
together. Therefore, based on the above-mentioned multiple modal data, an <span
class=SpellE>iFAM</span> model based on deep learning and big data technology
is proposed. This model uses the theoretical knowledge of convolutional neural
network as the basis, and inputs the menstrual cycle data and basal body
temperature data of each pregnant woman, Ovulation test paper data and cervical
mucus data, combined with the information of these data, automatically predict
the ovulation day and menstrual period information of the pregnant woman.
Preliminary experimental results show that the accuracy of the FAM method in
identifying ovulation days is as high as 89%, and the accuracy in predicting
menstruation is as high as 93%, and the pregnancy success rate of pregnant
women can be increased to 273%.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>METHOD<o:p></o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>To meet the
needs of pregnant women who can carry out pregnancy preparation management at
home and reach the level of medical assistance, and in view of the lack of
multimodal data fusion and intelligent analysis in the field of female
reproductive health, we propose a menstrual and ovulation day prediction model <span
class=SpellE>iFAM</span> model based on deep learning and big data technology.
The model consists of three parts: test paper image recognition structure, data
fusion structure and intelligent prediction and analysis structure, as shown in
the Fig1.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>Firstly, the
test paper image recognition structure uses the HED model and OpenCV technology
to extract the test paper image from the image to be recognized to avoid the
influence of complex backgrounds. Secondly, by using the CRNN model, the
position of the recognition line in the image of the test paper to be
recognized is obtained, and the color space of the position of the recognition
line is converted into the LAB color space. Then, extract the image brightness
value corresponding to the identification line position in the LAB color space,
compare it with the brightness value range in the detection line information,
and determine the preset ratio range in the detection line information
corresponding to the type of test paper. To determine the test paper <span
class=GramE>detection</span> result corresponding to the ratio.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>The data fusion
structure adopts data post fusion technology, inputs four or more kinds of
reference data into the neural network, obtains the weight of each reference
data through training, and can more accurately lock the ovulation day.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
style='mso-no-proof:yes'><!--[if gte vml 1]><v:shapetype id="_x0000_t75"
 coordsize="21600,21600" o:spt="75" o:preferrelative="t" path="m@4@5l@4@11@9@11@9@5xe"
 filled="f" stroked="f">
 <v:stroke joinstyle="miter"/>
 <v:formulas>
  <v:f eqn="if lineDrawn pixelLineWidth 0"/>
  <v:f eqn="sum @0 1 0"/>
  <v:f eqn="sum 0 0 @1"/>
  <v:f eqn="prod @2 1 2"/>
  <v:f eqn="prod @3 21600 pixelWidth"/>
  <v:f eqn="prod @3 21600 pixelHeight"/>
  <v:f eqn="sum @0 0 1"/>
  <v:f eqn="prod @6 1 2"/>
  <v:f eqn="prod @7 21600 pixelWidth"/>
  <v:f eqn="sum @8 21600 0"/>
  <v:f eqn="prod @7 21600 pixelHeight"/>
  <v:f eqn="sum @10 21600 0"/>
 </v:formulas>
 <v:path o:extrusionok="f" gradientshapeok="t" o:connecttype="rect"/>
 <o:lock v:ext="edit" aspectratio="t"/>
</v:shapetype><v:shape id="Í¼Æ¬_x0020_1" o:spid="_x0000_i1025" type="#_x0000_t75"
 style='width:380.4pt;height:307.2pt;visibility:visible;mso-wrap-style:square'>
 <v:imagedata src="Intelligent%20home%20pregnancy%20management%20method%20based%20on%20multi(1).files/image001.png"
  o:title=""/>
</v:shape><![endif]--><![if !vml]><img border=0 width=507 height=410
src="Intelligent%20home%20pregnancy%20management%20method%20based%20on%20multi(1).files/image002.png"
v:shapes="Í¼Æ¬_x0020_1"><![endif]></span></p>

<p class=MsoNormal align=center style='text-align:center'><span lang=EN-US
style='font-size:10.5pt'>Fig 1 <span class=SpellE>iFAM</span> model predicts
ovulation day and menstrual period<o:p></o:p></span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>EXPERIMENT<o:p></o:p></span></p>

<p class=MsoListParagraph style='margin-left:21.0pt;text-indent:-21.0pt;
mso-char-indent-count:0;mso-outline-level:1;mso-list:l0 level1 lfo1'><![if !supportLists]><span
lang=EN-US style='font-size:14.0pt;mso-fareast-font-family:"Times New Roman";
mso-bidi-font-family:"Times New Roman"'><span style='mso-list:Ignore'>1.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><![endif]><span
lang=EN-US style='font-size:14.0pt'>Dataset<o:p></o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>This experiment
recruited 1866 women who were over 20 years old who were preparing for
pregnancy. Through statistics of the physical conditions of these women, we
found the following four types, and we classified them, as shown in Table 1.
Women between the ages of 26 and 30 have the most people in a healthy state.
This also shows that the age of women who are preparing for pregnancy in our
country is getting older, and there are more and more cases of late marriage
and late childbirth.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoListParagraph align=center style='margin-left:21.0pt;text-align:
center;mso-pagination:widow-orphan;vertical-align:baseline'><span lang=EN-US
style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:
0pt'>Table 1 Details of pregnant women<o:p></o:p></span></p>

<div align=center>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=113 valign=top style='width:3.0cm;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Age<o:p></o:p></span></p>
  </td>
  <td width=97 valign=top style='width:72.95pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>20~25<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>26~30<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:3.0pt;margin-right:0cm;
  margin-bottom:3.0pt;margin-left:0cm;text-align:center;mso-pagination:widow-orphan;
  vertical-align:baseline'><span lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:
  ËÎÌå;color:#333333;mso-font-kerning:0pt'>31~35<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>36~40<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Above 40<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=113 valign=top style='width:3.0cm;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Healthy<o:p></o:p></span></p>
  </td>
  <td width=97 valign=top style='width:72.95pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>380<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>568<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>229<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>77<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>22<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=113 valign=top style='width:3.0cm;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Insufficient corpus luteum<o:p></o:p></span></p>
  </td>
  <td width=97 valign=top style='width:72.95pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>2<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>12<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>10<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>3<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>0<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td width=113 valign=top style='width:3.0cm;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Polycystic<o:p></o:p></span></p>
  </td>
  <td width=97 valign=top style='width:72.95pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>80<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>106<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>25<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>6<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>0<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;mso-yfti-lastrow:yes'>
  <td width=113 valign=top style='width:3.0cm;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Infertility<o:p></o:p></span></p>
  </td>
  <td width=97 valign=top style='width:72.95pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>60<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>99<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>49<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>16<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>5<o:p></o:p></span></p>
  </td>
 </tr>
</table>

</div>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>These women will
continue to prepare for pregnancy for up to 9 cycles. During each cycle during
pregnancy, menstrual information, basal body temperature and cervical mucus
trait data will be continuously recorded, and LH test strips and pictures of
early pregnancy test strips will be uploaded to the database.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>Among them, the
pictures of LH test strips are marked with <span class=SpellE>Labelme</span>
software. <span class=SpellE>Labelme</span> is an image labeling tool developed
by the Computer Science and Artificial Intelligence Laboratory (CSAIL) of MIT.
People can use this tool to create customized labeling tasks or perform image
labeling. The source code of the project is open source.</span></p>

<p class=MsoListParagraph style='margin-left:21.0pt;text-indent:-21.0pt;
mso-char-indent-count:0;mso-outline-level:1;mso-list:l0 level1 lfo1'><![if !supportLists]><span
lang=EN-US style='font-size:14.0pt;mso-fareast-font-family:"Times New Roman";
mso-bidi-font-family:"Times New Roman"'><span style='mso-list:Ignore'>2.<span
style='font:7.0pt "Times New Roman"'>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><![endif]><span
lang=EN-US style='font-size:14.0pt'>Ablation experiment<o:p></o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>In the ablation
experiment, the accuracy of predicting ovulation day and menstrual period was
compared with multi-modal data fusion and single-modal, two-dimensional or
three-dimensional modal data fusion. The accuracy of the FAM method in
identifying ovulation days (Accuracy1) is as high as 89%, and the accuracy in
predicting menstruation (Accuracy2) is as high as 93%. The accuracy of
predicting ovulation day and menstrual period is higher than that of
single-modal, two-dimensional or three-dimensional modal data fusion.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoListParagraph align=center style='margin-left:21.0pt;text-align:
center;mso-pagination:widow-orphan;vertical-align:baseline'><span lang=EN-US
style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:
0pt'>Table 2 Table of results of ablation experiments<o:p></o:p></span></p>

<div align=center>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=85 valign=top style='width:64.05pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Method<o:p></o:p></span></p>
  </td>
  <td width=43 valign=top style='width:32.35pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>LH<o:p></o:p></span></p>
  </td>
  <td width=42 valign=top style='width:31.2pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>BBT<o:p></o:p></span></p>
  </td>
  <td width=76 valign=top style='width:2.0cm;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:3.0pt;margin-right:0cm;
  margin-bottom:3.0pt;margin-left:0cm;text-align:center;mso-pagination:widow-orphan;
  vertical-align:baseline'><span lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:
  ËÎÌå;color:#333333;mso-font-kerning:0pt'>Cervical mucus<o:p></o:p></span></p>
  </td>
  <td width=70 valign=top style='width:52.8pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Calendar method<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.55pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph style='margin-top:3.0pt;margin-right:0cm;
  margin-bottom:3.0pt;margin-left:0cm;text-indent:0cm;mso-char-indent-count:
  0;mso-pagination:widow-orphan;vertical-align:baseline'><span lang=EN-US
  style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:
  0pt'>Accuracy1(%)<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.65pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph style='margin-top:3.0pt;margin-right:0cm;
  margin-bottom:3.0pt;margin-left:0cm;text-indent:0cm;mso-char-indent-count:
  0;mso-pagination:widow-orphan;vertical-align:baseline'><span lang=EN-US
  style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:
  0pt'>Accuracy2(%)<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=85 valign=top style='width:64.05pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Single mode<o:p></o:p></span></p>
  </td>
  <td width=43 valign=top style='width:32.35pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=42 valign=top style='width:31.2pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
  <td width=76 valign=top style='width:2.0cm;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
  <td width=70 valign=top style='width:52.8pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.55pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>72.6%<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.65pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=85 valign=top style='width:64.05pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Two-dimensional<o:p></o:p></span></p>
  </td>
  <td width=43 valign=top style='width:32.35pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=42 valign=top style='width:31.2pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=76 valign=top style='width:2.0cm;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
  <td width=70 valign=top style='width:52.8pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.55pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>81.3%<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.65pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td width=85 valign=top style='width:64.05pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Three-dimensional<o:p></o:p></span></p>
  </td>
  <td width=43 valign=top style='width:32.35pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=42 valign=top style='width:31.2pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=76 valign=top style='width:2.0cm;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
  <td width=70 valign=top style='width:52.8pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.55pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>85.2%<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.65pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>89.8%<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4;mso-yfti-lastrow:yes'>
  <td width=85 valign=top style='width:64.05pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>FAM<o:p></o:p></span></p>
  </td>
  <td width=43 valign=top style='width:32.35pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=42 valign=top style='width:31.2pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=76 valign=top style='width:2.0cm;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=70 valign=top style='width:52.8pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  style='font-size:10.0pt;font-family:ËÎÌå;mso-ascii-font-family:"Times New Roman";
  mso-hansi-font-family:"Times New Roman";mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>√</span><span lang=EN-US style='font-size:10.0pt;
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.55pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>88.9%<o:p></o:p></span></p>
  </td>
  <td width=105 valign=top style='width:78.65pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>93%<o:p></o:p></span></p>
  </td>
 </tr>
</table>

</div>

<p class=MsoListParagraph style='margin-left:21.0pt;mso-pagination:widow-orphan;
vertical-align:baseline'><span lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:
ËÎÌå;color:#333333;mso-font-kerning:0pt'><o:p>&nbsp;</o:p></span></p>

<p class=MsoListParagraph align=center style='margin-left:21.0pt;text-align:
center;mso-pagination:widow-orphan;vertical-align:baseline'><span lang=EN-US
style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:
0pt'>Table 3 Details of the pregnancy success rate of 9-cycle pregnant women<o:p></o:p></span></p>

<div align=center>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=95 valign=top style='width:70.9pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Age<o:p></o:p></span></p>
  </td>
  <td width=59 valign=top style='width:44.6pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>20~25<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>26~30<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoNormal align=center style='margin-top:3.0pt;margin-right:0cm;
  margin-bottom:3.0pt;margin-left:0cm;text-align:center;mso-pagination:widow-orphan;
  vertical-align:baseline'><span lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:
  ËÎÌå;color:#333333;mso-font-kerning:0pt'>31~35<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>36~40<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:none;
  mso-border-top-alt:solid windowtext .5pt;mso-border-bottom-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>40</span><span style='font-size:10.5pt;font-family:
  ËÎÌå;mso-ascii-font-family:"Times New Roman";mso-hansi-font-family:"Times New Roman";
  mso-bidi-font-family:ËÎÌå;color:#333333;mso-font-kerning:0pt'>ÒÔÉÏ</span><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=95 valign=top style='width:70.9pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Healthy/ Insufficient corpus luteum<o:p></o:p></span></p>
  </td>
  <td width=59 valign=top style='width:44.6pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>98%<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>97%<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>92%<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>89%<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border:none;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>70%<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2;mso-yfti-lastrow:yes'>
  <td width=95 valign=top style='width:70.9pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.5pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>Polycystic<o:p></o:p></span></p>
  </td>
  <td width=59 valign=top style='width:44.6pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>87.5%<o:p></o:p></span></p>
  </td>
  <td width=67 valign=top style='width:50.3pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>80.1%<o:p></o:p></span></p>
  </td>
  <td width=71 valign=top style='width:53.4pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>68.0%<o:p></o:p></span></p>
  </td>
  <td width=60 valign=top style='width:44.9pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>50%<o:p></o:p></span></p>
  </td>
  <td width=82 valign=top style='width:61.15pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt'>
  <p class=MsoListParagraph align=center style='margin-top:3.0pt;margin-right:
  0cm;margin-bottom:3.0pt;margin-left:0cm;text-align:center;text-indent:0cm;
  mso-char-indent-count:0;mso-pagination:widow-orphan;vertical-align:baseline'><span
  lang=EN-US style='font-size:10.0pt;mso-bidi-font-family:ËÎÌå;color:#333333;
  mso-font-kerning:0pt'>-<o:p></o:p></span></p>
  </td>
 </tr>
</table>

</div>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>Table 2 and
Table 3 show that using the FAM method, the pregnancy success rate of pregnant
women is the highest. From this, we can see the importance of finding the
ovulation day. In response to the above-mentioned, the key to a fast and
natural pregnancy is to find the ovulation day of the pregnant woman. As long
as the ovulation day is found and the intercourse is arranged in time,
pregnancy is a natural thing.</span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>CONCLUSION<o:p></o:p></span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>In this paper,
we focus on solving the problem of home pregnancy monitoring and management of
pregnant women. The IFAM model we proposed introduces the <span class=SpellE>hed</span>
and <span class=SpellE>crnn</span> framework, and uses deep learning and <span
class=SpellE>opencv</span> technology to fuse multimodal data to obtain more
fusion information, to predict the ovulation date and menstrual period of
pregnant women, to improve the success rate of women's pregnancy.</span></p>

<p class=MsoNormal style='text-indent:21.0pt'><span lang=EN-US>In the future
work, we seek to cooperate with the hospital to combine the multimodal data
with the data in the B-ultrasound measurement report, six hormone reports or
AMH monitoring report, to achieve higher accuracy in predicting the ovulation
day of pregnant women.</span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'>REFERENCES<o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:7.5pt;mso-pagination:widow-orphan'><span
lang=EN-US style='mso-bidi-font-family:"Times New Roman";color:#333333;
mso-font-kerning:0pt'>[1]</span><span lang=EN-US style='mso-bidi-font-family:
"Times New Roman";color:#222222;background:white'> <span class=SpellE>Guida</span>
M, <span class=SpellE>Tommaselli</span> G A, <span class=SpellE>Palomba</span>
S, et al. Efficacy of methods for determining ovulation in a natural family
planning program[J]. Fertility and sterility, 1999, 72(5): 900-904.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:7.5pt;mso-pagination:widow-orphan'><span
lang=EN-US style='mso-bidi-font-family:"Times New Roman";color:#333333;
mso-font-kerning:0pt'>[2]</span><span lang=EN-US style='mso-bidi-font-family:
"Times New Roman";color:#222222;background:white'> <span class=SpellE>Ar¨¦valo</span>
M, Sinai I, Jennings V. A fixed formula to define the fertile window of the
menstrual cycle as the basis of a simple method of natural family planning[J].
Contraception, 1999, 60(6): 357-360.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:7.5pt;mso-pagination:widow-orphan'><span
lang=EN-US style='mso-bidi-font-family:"Times New Roman";color:#333333;
mso-font-kerning:0pt'>[3] P. Frank-Herrmann, etc. The effectiveness of a
fertility <span class=GramE>awareness based</span> method to avoid pregnancy in
relation to a couple¡¯s sexual behavior during the fertile time: a prospective
longitudinal study. Human Reproduction pp.1-10, 2007.</span><span lang=EN-US
style='mso-bidi-font-family:"Times New Roman";mso-font-kerning:0pt'><o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:7.5pt;mso-pagination:widow-orphan'><span
lang=EN-US style='mso-bidi-font-family:"Times New Roman";color:#333333;
mso-font-kerning:0pt'>[4] Ferreira-Poblete A. The probability of conception on
different days of the cycle with respect to ovulation: an overview[J]. Advances
in Contraception, 1997, 13(2-3): 83-95.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:7.5pt;mso-pagination:widow-orphan'><span
lang=EN-US style='mso-bidi-font-family:"Times New Roman";color:#222222;
background:white'>[5] <span class=SpellE>Su</span> H W, Yi Y C, Wei T Y, et al.
Detection of ovulation, a review of currently available methods[J].
Bioengineering &amp; translational medicine, 2017, 2(3): 238-246.</span><span
lang=EN-US style='mso-bidi-font-family:"Times New Roman";mso-font-kerning:0pt'><o:p></o:p></span></p>

<p class=MsoNormal align=center style='text-align:center;mso-outline-level:
1'><span lang=EN-US style='font-size:14.0pt'><o:p>&nbsp;</o:p></span></p>

</div>

</body>

</html>
