Intelligent home pregnancy management method based on multi-modal data fusion

Yin Wang1, Zhiwei Zuo1, Wei Wang1, Nuan Qiu 1\*

1 Beijing Aikangtai Technology Co., Ltd., Beijing, China

Email: [qiun@ikangtai.com](mailto:qiun@ikangtai.com)

Abstract: With the issuance of the national three-child policy, the field of
female reproduction has attracted more and more attention. To care for female
reproductive health and help the implementation of the government's three child
policy, we have proposed an intelligent home pregnancy preparation management
method based on multimodal data fusion, namely FAM (Fertility Awareness Method,
FAM). This method introduces big data, multimodal data fusion and image
recognition technology. By inputting multi-modal data such as menstrual cycle,
basal body temperature, ovulation test paper and cervical mucus of the pregnant
woman, it can automatically predict the ovulation day and menstrual period
information of the pregnant woman. This improves the pregnancy success rate of
pregnant women, breaks the limitations of the traditional method of finding the
ovulation day through monomodal data, and facilitates the monitoring of pregnant
women at home. Finally, compared with the single-mode method qualitatively and
quantitatively, the preliminary experimental results show that the accuracy of
FAM method in identifying ovulation date is as high as 89%, and the accuracy in
predicting menstrual period is as high as 93%, and the pregnancy success rate of
pregnant women can be increased to 273% in at least nine cycles.

Key words: multimodal data fusion; FAM; ovulation day; menstrual period
information

INCTRODCTION

In recent years, multimodal data fusion technology has become popular in the
medical field as a kind of deep learning technology, and it plays a very
important role in assisting clinical diagnosis and condition prediction of
diseases. With the country's full liberalization and encouragement of three
births, female reproductive health will become a major focus of the medical
field, and the application of deep learning technology to the field of female
reproductive health is bound to become a major trend. Therefore, to care for
female reproductive health and help the government implement the three-child
policy, we propose an intelligent home pregnancy management method based on
multi-modal data fusion.

First of all, this method can help pregnant women to get pregnant quickly and
naturally by predicting the next menstrual period and finding the ovulation day.
The key to rapid natural pregnancy is to find the ovulation date of pregnant
women. As long as the ovulation date is found, the roommate shall be arranged in
time, pregnancy is a natural thing (except for patients with reproductive
diseases)! However, the traditional methods of finding the ovulation day mostly
use monomodal data, two-dimensional or three-dimensional modal data to predict
the ovulation day of pregnant women.

For example, the basal body temperature prediction method for ovulation is the
oldest, simplest and most widely used method, which is still used today. But
most people think that this method is retrospective and can only determine the
presence or absence of ovulation, and cannot predict the time of ovulation.
There is also the earliest cervical mucus observation method proposed by
Australian doctor Dr. Billings [1], which predicts the occurrence of ovulation
by feeling, touching and observing the properties of cervical mucus with the
naked eye. This method usually requires continuous observation for multiple
cycles, a long time and the evaluation of cervical mucus is subjective. Or the
menstrual calendar method developed later, Marcos et al. [2] designed a fixed
formula to input the menstrual information of the previous cycle to calculate
the next menstrual period and the fertile period, thereby predicting the
ovulation day, although it is more convenient than the cervical mucus
observation method It saves time, but this method is not suitable for women with
irregular cycles.

Later, Yussman et al. [3] used the method of measuring the blood LH value and
Kratochvil first reported in 1972 that the follicles were examined by ultrasound
[4], which was later the B-ultrasound used in the hospital. Although the above
two methods are accurate, they both require patients to go to the hospital for
multiple inspections. The inspection costs are relatively high, which is bound
to increase the financial burden of the family. Later, the LH test strips were
produced so that all women who were preparing for pregnancy could be tested at
home to predict the day of ovulation. It is also very important for many
infertility patients to predict ovulation. This was also verified in the
experiment of Corson et al [5]. However, LH test paper testing is usually
combined with basal body temperature testing.

In summary, through the understanding and analysis of the above methods for
finding ovulation days, we found that few people can integrate these important
data together. Therefore, based on the above-mentioned multiple modal data, an
iFAM model based on deep learning and big data technology is proposed. This
model uses the theoretical knowledge of convolutional neural network as the
basis, and inputs the menstrual cycle data and basal body temperature data of
each pregnant woman, Ovulation test paper data and cervical mucus data, combined
with the information of these data, automatically predict the ovulation day and
menstrual period information of the pregnant woman. Preliminary experimental
results show that the accuracy of the FAM method in identifying ovulation days
is as high as 89%, and the accuracy in predicting menstruation is as high as
93%, and the pregnancy success rate of pregnant women can be increased to 273%.

METHOD

To meet the needs of pregnant women who can carry out pregnancy preparation
management at home and reach the level of medical assistance, and in view of the
lack of multimodal data fusion and intelligent analysis in the field of female
reproductive health, we propose a menstrual and ovulation day prediction model
iFAM model based on deep learning and big data technology. The model consists of
three parts: test paper image recognition structure, data fusion structure and
intelligent prediction and analysis structure, as shown in the Fig1.

Firstly, the test paper image recognition structure uses the HED model and
OpenCV technology to extract the test paper image from the image to be
recognized to avoid the influence of complex backgrounds. Secondly, by using the
CRNN model, the position of the recognition line in the image of the test paper
to be recognized is obtained, and the color space of the position of the
recognition line is converted into the LAB color space. Then, extract the image
brightness value corresponding to the identification line position in the LAB
color space, compare it with the brightness value range in the detection line
information, and determine the preset ratio range in the detection line
information corresponding to the type of test paper. To determine the test paper
detection result corresponding to the ratio.

The data fusion structure adopts data post fusion technology, inputs four or
more kinds of reference data into the neural network, obtains the weight of each
reference data through training, and can more accurately lock the ovulation day.

![](media/52b8f56303c91f88cc98148af8aaaac8.png)

Fig 1 iFAM model predicts ovulation day and menstrual period

EXPERIMENT

1.  Dataset

This experiment recruited 1866 women who were over 20 years old who were
preparing for pregnancy. Through statistics of the physical conditions of these
women, we found the following four types, and we classified them, as shown in
Table 1. Women between the ages of 26 and 30 have the most people in a healthy
state. This also shows that the age of women who are preparing for pregnancy in
our country is getting older, and there are more and more cases of late marriage
and late childbirth.

Table 1 Details of pregnant women

| Age                        | 20\~25 | 26\~30 | 31\~35 | 36\~40 | Above 40 |
|----------------------------|--------|--------|--------|--------|----------|
| Healthy                    | 380    | 568    | 229    | 77     | 22       |
| Insufficient corpus luteum | 2      | 12     | 10     | 3      | 0        |
| Polycystic                 | 80     | 106    | 25     | 6      | 0        |
| Infertility                | 60     | 99     | 49     | 16     | 5        |

These women will continue to prepare for pregnancy for up to 9 cycles. During
each cycle during pregnancy, menstrual information, basal body temperature and
cervical mucus trait data will be continuously recorded, and LH test strips and
pictures of early pregnancy test strips will be uploaded to the database.

Among them, the pictures of LH test strips are marked with Labelme software.
Labelme is an image labeling tool developed by the Computer Science and
Artificial Intelligence Laboratory (CSAIL) of MIT. People can use this tool to
create customized labeling tasks or perform image labeling. The source code of
the project is open source.

1.  Ablation experiment

In the ablation experiment, the accuracy of predicting ovulation day and
menstrual period was compared with multi-modal data fusion and single-modal,
two-dimensional or three-dimensional modal data fusion. The accuracy of the FAM
method in identifying ovulation days (Accuracy1) is as high as 89%, and the
accuracy in predicting menstruation (Accuracy2) is as high as 93%. The accuracy
of predicting ovulation day and menstrual period is higher than that of
single-modal, two-dimensional or three-dimensional modal data fusion.

Table 2 Table of results of ablation experiments

| Method            | LH | BBT | Cervical mucus | Calendar method | Accuracy1(%) | Accuracy2(%) |
|-------------------|----|-----|----------------|-----------------|--------------|--------------|
| Single mode       | √  | -   | -              | -               | 72.6%        | -            |
| Two-dimensional   | √  | √   | -              | -               | 81.3%        | -            |
| Three-dimensional | √  | √   | -              | √               | 85.2%        | 89.8%        |
| FAM               | √  | √   | √              | √               | 88.9%        | 93%          |

Table 3 Details of the pregnancy success rate of 9-cycle pregnant women

| Age                                 | 20\~25 | 26\~30 | 31\~35 | 36\~40 | 40以上 |
|-------------------------------------|--------|--------|--------|--------|--------|
| Healthy/ Insufficient corpus luteum | 98%    | 97%    | 92%    | 89%    | 70%    |
| Polycystic                          | 87.5%  | 80.1%  | 68.0%  | 50%    | -      |

Table 2 and Table 3 show that using the FAM method, the pregnancy success rate
of pregnant women is the highest. From this, we can see the importance of
finding the ovulation day. In response to the above-mentioned, the key to a fast
and natural pregnancy is to find the ovulation day of the pregnant woman. As
long as the ovulation day is found and the intercourse is arranged in time,
pregnancy is a natural thing.

CONCLUSION

In this paper, we focus on solving the problem of home pregnancy monitoring and
management of pregnant women. The IFAM model we proposed introduces the hed and
crnn framework, and uses deep learning and opencv technology to fuse multimodal
data to obtain more fusion information, to predict the ovulation date and
menstrual period of pregnant women, to improve the success rate of women's
pregnancy.

In the future work, we seek to cooperate with the hospital to combine the
multimodal data with the data in the B-ultrasound measurement report, six
hormone reports or AMH monitoring report, to achieve higher accuracy in
predicting the ovulation day of pregnant women.

REFERENCES

[1] Guida M, Tommaselli G A, Palomba S, et al. Efficacy of methods for
determining ovulation in a natural family planning program[J]. Fertility and
sterility, 1999, 72(5): 900-904.

[2] Arévalo M, Sinai I, Jennings V. A fixed formula to define the fertile window
of the menstrual cycle as the basis of a simple method of natural family
planning[J]. Contraception, 1999, 60(6): 357-360.

[3] P. Frank-Herrmann, etc. The effectiveness of a fertility awareness based
method to avoid pregnancy in relation to a couple’s sexual behavior during the
fertile time: a prospective longitudinal study. Human Reproduction pp.1-10,
2007.

[4] Ferreira-Poblete A. The probability of conception on different days of the
cycle with respect to ovulation: an overview[J]. Advances in Contraception,
1997, 13(2-3): 83-95.

[5] Su H W, Yi Y C, Wei T Y, et al. Detection of ovulation, a review of
currently available methods[J]. Bioengineering & translational medicine, 2017,
2(3): 238-246.
