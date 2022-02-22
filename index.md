

# Intelligent home pregnancy management method based on multi-modal data fusion

Yin Wang<sup>1,2</sup>, LiQun Yu<sup>3</sup>, Zhiwei Zuo<sup>1,2</sup>, Wei Wang<sup>1,2</sup>, Nuan Qiu<sup>1,2</sup>\*

<sup>1</sup> Beijing Aikangtai Technology Co., Ltd., Haidian District, Beijing, China

<sup>2</sup> Zhejiang Yuncheng Medical Technology Co., Ltd., Jiaxing District, Hangzhou,
Zhejiang Province, China

<sup>3</sup> Aviation General Hospital of China Medical University, Chaoyang District,
Beijing, China

\*qiun@ikangtai.com

*Abstract*—With the promulgation of the national three-child policy, the field
of female reproduction has received more and more attention. In order to care
for female reproductive health and help the implementation of the government's
three-child policy, we propose a smart home pregnancy preparation based on
multimodal data fusion Management method, namely iFAM (Intellgent Fertility
Awareness Method, iFAM). This method introduces big data, multi-modal data
fusion and image recognition technology. By inputting multi-modal data such as
menstrual cycle, basal body temperature, ovulation test strips and cervical
mucus of pregnant women, it can intelligently predict ovulation day and
menstrual period information, breaking the traditional Methods The limitation of
ovulation day was found through unimodal data, so as to improve the pregnancy
success rate of pregnant women. In addition, the method has been successfully
deployed in the Shecare APP, which enables women who are preparing to conceive
to monitor the ovulation day at home. Finally, the qualitative and quantitative
comparison between the iFAM method and the traditional method of predicting
ovulation day, preliminary experimental results show that the accuracy of FAM
method in identifying ovulation day is as high as 89%, the accuracy in
predicting menstrual period is as high as 93%, and the pregnancy success rate of
pregnant women can be improved. to 273%.

Keywords- multimodal data fusion; iFAM; ovulation day; menstrual period
information

## INCTRODCTION

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
results show that the accuracy of the iFAM method in identifying ovulation days
is as high as 89%, and the accuracy in predicting menstruation is as high as
93%, and the pregnancy success rate of pregnant women can be increased to 273%.

## METHOD

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
recognition line is converted into the LAB color space[6]. Then, extract the
image brightness value corresponding to the identification line position in the
LAB color space, compare it with the brightness value range in the detection
line information, and determine the preset ratio range in the detection line
information corresponding to the type of test paper. To determine the test paper
detection result corresponding to the ratio.

![Fig1](https://raw.githubusercontent.com/chenzhiyuanding/czy.GitHub.io/gh-pages/image/fig1.png)

Fig 1 iFAM model predicts ovulation day and menstrual period

## EXPERIMENT

We compared the proposed iFAM method with several traditional methods for
predicting the day of ovulation. In this section, we describe the dataset and
implementation details and ablation experiments, qualitative and quantitative
results to the effectiveness of the iFAM method.

### Dataset

This experiment recruited 1866 women who were over 20 years old who were
preparing for pregnancy. Through statistics of the physical conditions of these
women, we found the following four types, and we classified them, as shown in
Table 1. Women between the ages of 26 and 30 have the most people in a healthy
state. This also shows that the age of women who are preparing for pregnancy in
our country is getting older, and there are more and more cases of late marriage
and late childbirth.


TABLE I. 	DETAILS OF PREGNANT WOMEN

| **AGE**                        | **20\~25** | **26\~30** | **31\~35** | **36\~40** | **Over 40** |
|--------------------------------|------------|------------|------------|------------|-------------|
| **Healthy**                    | 380        | 568        | 229        | 77         | 22          |
| **Insufficient corpus luteum** | 2          | 12         | 10         | 3          | 0           |
| **Polycystic**                 | 80         | 106        | 25         | 6          | 0           |
| **Infertility**                | 60         | 99         | 49         | 16         | 5           |


In order to ensure the validity of the experiment, we excluded the pregnant
women with infertility in Table 1, and divided the remaining 1636 pregnant women
into four groups, with 409 pregnant women in each group, using Shecare according
to our requirements. The APP (the iFAM method has been deployed into the Shecare
APP) will last for up to 9 cycles of pregnancy preparation. Among them, the
first group of pregnant women only entered the menstrual period information to
predict the ovulation day and menstrual period according to the calendar method;
the second group of pregnant women uploaded ovulation test strips to the Shecare
APP based on the calendar method; and the third group of pregnant women used the
calendar. method, ovulation test strips and measuring basal body temperature to
prepare for pregnancy; finally, the fourth group of pregnant women signed a
nine-month pregnancy guarantee plan with us, that is, every cycle of this group
of pregnant women during pregnancy will continue in the APP Record menstrual
information, ovulation test strips, cervical mucus, basal body temperature and
intercourse data.

Among them, the thermometers used by the above-mentioned women preparing to
upload their basal body temperature data include the Shecare basic model
(BL-T980) and the smart model (YC-K399B), and the ovulation test strips used are
Shecare ovulation test strips. In addition, the ovulation test strip pictures
obtained in the iFAM method were marked with Labelme software. Labelme is an
image annotation tool developed by the Computer Science and Artificial
Intelligence Laboratory (CSAIL) of MIT. People can use this tool to create
customized annotation tasks or perform image annotation. The source code of the
project has been open sourced.

### Ablation experiment

Firstly, we compared the accuracy of the iFAM method in predicting ovulation
days and menstrual periods with single-, two-, or three-dimensional data
prediction methods using the above-mentioned control group for 9 months of
pregnancy. From Table 2, it can be seen that the accuracy of iFAM method in
identifying ovulation day (Accuracy1) is as high as 89%, and the accuracy in
predicting menstrual period (Accuracy2) is as high as 93%. Higher accuracy than
predictions of ovulation day and menstrual period by unimodal, two-dimensional
or three-dimensional modal data methods.

Secondly, we analyzed the effect of the iFAM method and the traditional
ovulation day method on pregnancy success in age-based women trying to conceive.
It is widely believed that the prime time to have children is in the 20s. Eggs
are of the highest quality when you are in your 20s, and sperm quality is
generally healthy for men of that age. Generally speaking, people are at their
best fertile during this time, but many may not be mentally or financially ready
for it. In your 30s, your chances of getting pregnant are only slightly lower
than in your 20s. 35s is often emphasized because that's about when the decline
gets faster. Although fertility does decline over time, it declines more rapidly
after age 35. The number of pregnancies in your 40s is increasing every year,
largely because of assisted reproductive technology (ART) procedures such as in
vitro fertilization (IVF)[7].

TABLE II. 	TABLE OF RESULTS OF ABLATION EXPERIMENTS

| **Method**            | **LH** | **BBT** | **Cervical mucus** | **Calendar method** | **Accuracy1(%)** | **Accuracy2(%)** |
|-----------------------|--------|---------|--------------------|---------------------|------------------|------------------|
| **Single mode**       | -      | -       | -                  | √                   | 72.6%            | -                |
| **Two-dimensional**   | √      | -       | -                  | √                   | 81.3%            | -                |
| **Three-dimensional** | √      | √       | -                  | √                   | 85.2%            | 89.8%            |
| **iFAM**              | √      | √       | √                  | √                   | 88.9%            | 93%              |


TABLE III. 	DETAILS OF PREGNANCY SUCCESS RATE OF WOMEN BEFORE PREGNANCY PREPARATION

| **AGE**                    | **20\~25** | **26\~30** | **31\~35** | **36\~40** | **over 40** |
|----------------------------|------------|------------|------------|------------|-------------|
| **Pregnancy success rate** | 25%        | 20%        | 15%        | 10%        | 5%          |


TABLE IV. 	USING THE TRADITIONAL SINGLE, TWO-DIMENSIONAL OR THREE-DIMENSIONAL MODAL METHOD AND IFAM METHOD, THE PREGNANCY SUCCESS RATE OF WOMEN WITH 9 CYCLES OF BACKUP PREGNANCY WAS DETAILED

| **AGE**               | **20\~25** | **26\~30** | **31\~35** | **36\~40** | **over 40** |
|-----------------------|------------|------------|------------|------------|-------------|
| **Single mode**       | 45%        | 41%        | 38%        | 13%        | 7%          |
| **Two-dimensional**   | 53%        | 46%        | 44%        | 15%        | 7%          |
| **Three-dimensional** | 58%        | 52%        | 49%        | 15%        | 8%          |
| **iFAM**              | 69%        | 63%        | 55%        | 21%        | 10%         |


However, according to Table 3 and Table 4, although the probability of pregnancy
is limited by age, after signing a guarantee plan with us, by using the iFAM
method in the APP, the compliance of pregnant women is strengthened, thereby
increasing the pregnancy success rate by 173%. That is, the pregnancy success
rate after nine cycles is about 3 times higher than the pregnancy success rate
at the beginning. From this, we can also see the importance of identifying the
ovulation day, which is in response to the above-mentioned, the key to fast and
natural pregnancy is to find the ovulation day of the pregnant woman. As long as
the ovulation day is found, and the intercourse is arranged in time, pregnancy
is a natural thing.

## CONCLUSION

In this paper, we focus on solving the problem of home pregnancy monitoring and
management of pregnant women. The iFAM model we proposed introduces the hed and
crnn framework, and uses deep learning and opencv technology to fuse multimodal
data to obtain more fusion information, to predict the ovulation date and
menstrual period of pregnant women, to improve the success rate of women's
pregnancy.

In the future work, we seek to cooperate with the hospital to combine the
multimodal data with the data in the B-ultrasound measurement report, six
hormone reports or AMH monitoring report, to achieve higher accuracy in
predicting the ovulation day of pregnant women.

## REFERENCES

>   [1] Guida M, Tommaselli G A, Palomba S, et al. Efficacy of methods for
>   determining ovulation in a natural family planning program[J]. Fertility and
>   sterility, 1999, 72(5): 900-904.

>   [2] Arévalo M, Sinai I, Jennings V. A fixed formula to define the fertile
>   window of the menstrual cycle as the basis of a simple method of natural
>   family planning[J]. Contraception, 1999, 60(6): 357-360.

>   [3] P. Frank-Herrmann, etc. The effectiveness of a fertility awareness based
>   method to avoid pregnancy in relation to a couple’s sexual behavior during
>   the fertile time: a prospective longitudinal study. Human Reproduction
>   pp.1-10, 2007.

>   [4] Ferreira-Poblete A. The probability of conception on different days of
>   the cycle with respect to ovulation: an overview[J]. Advances in
>   Contraception, 1997, 13(2-3): 83-95.

>   [5] Su H W, Yi Y C, Wei T Y, et al. Detection of ovulation, a review of
>   currently available methods[J]. Bioengineering & translational medicine,
>   2017, 2(3): 238-246.
