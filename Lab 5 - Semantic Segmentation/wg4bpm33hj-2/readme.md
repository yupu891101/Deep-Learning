# CCAgT dataset: Images of Cervical Cells with AgNOR Stain Technique

This is a computer vision dataset, created by some collaborators from different departments at [Universidade Federal de Santa Catarina (UFSC)](https://en.ufsc.br/).

The utilized images where patches/tiles of whole slide images (WSIs) from cervical samples stained with AgNOR technique. These images being a possible alternative to investigate cervical samples, because make possible the detection of nucleolus organizer regions (NORs). NORs are DNA loops containing genes responsible for the transcription of ribosomal RNA located in the cell nucleolus. They contain a set of argyrophilic proteins, selectively stained by silver nitrate, which can be identified as black dots located throughout the nucleoli area and called AgNORs.


## About

Contains 9339 images (1600x1200 where each pixel is 0.111µmX0.111µm) from 15 different slides, having at least one label per image. Have a total of 63190 annotations. The images were obtained from examinations that were performed on women who were treated at the Gynecology and Colposcopy Outpatient Clinic of the University Hospital Professor Polydoro Ernani de São Thiago of Federal University of Santa Catarina (HU-UFSC). These women, presenting cytological alterations in the oncotic cytology of previous exams, were referred to the [Ane Francyne Costa](https://repositorio.ufsc.br/handle/123456789/191940) for a gynecological exam, colposcopy and biopsy. This research was approved by the UFSC Research Ethics Committee (CEPSH), protocol number 57423616.3.0000.0121. All participating patients were previously approached and informed about the study objectives. Those who agreed to participate signed an Informed Consent Form.

### Highlights
- Contains 9339 images with resolution of 1600x1200 pixel, where each pixel is 0.111µmX0.111µm;
- Images from 15 patients with six different diagnostics;
- A total of 63190 instances of annotated objects;
  - Seven categories to describe the objects, where include two categories to differentiate NORs;
- Labels that can be used for: Semantic Segmentation, Object Detection, Instance Segmentation, Classification, Panoptic Segmentation;
- A tool for assist into the conversion, visualization and other things. [CCAgT-utils](https://github.com/johnnv1/CCAgT-utils)  


### Contributors

- [João Gustavo Atkinson Amorim](https://orcid.org/0000-0003-3361-6891) - [@johnnv1](https://github.com/johnnv1/)
- [André Victória Matias](https://orcid.org/0000-0003-0268-0233) - [@Andrevmatias](https://github.com/Andrevmatias)
- Tainee Bottamedi
- [Vinícius Moreno Sanches](https://orcid.org/0000-0001-9069-7726)
- [Ane Francyne Costa](https://orcid.org/0000-0003-1467-4877)
- [Fabiana Botelho Onofre](https://orcid.org/0000-0003-4857-5770)
- [Alexandre Sherlley Onofre](https://orcid.org/0000-0002-3833-8694)
- [Aldo von Wangenheim](https://orcid.org/0000-0003-4532-1417) - [@awangenh](https://github.com/awangenh)

### Old version

The first version of this dataset was published as contribution to the [paper](https://doi.org/10.1109/CBMS49503.2020.00110), and can be accessed at [UFSC data repository](https://arquivos.ufsc.br/d/373be2177a33426a9e6c/).

## Organization and information's of the dataset


### Filenames of images
Each image has a unique name with the format `<slide id>_<tile id>_<microscopy x position>_<microscopy y position>`. The `slide id` to differentiate the slides, and the patients respectively. The other's information is just complementary.

### The list of lesions
- Cervical intraepithelial neoplasia 1 (CIN 1)
- Cervical intraepithelial neoplasia 2 (CIN 2)
- Cervical intraepithelial neoplasia 3 (CIN 3)
- Squamous cell carcinoma (SCC)
- Adenocarcinoma (AC)
- No lesion


### About the slides

| Slide id  | Diagnostics | images | annotations | Nucleus | Clusters | Satellite | Nucleus out of focus | Overlapped nuclei | Non-viable nuclei | Leukocyte |
| :-------: | :---------: | :----: | :---------: | :-----: | :------: | :-------: | :------------------: | :---------------: | :---------------: | :-------: |
|     A     |    CIN 3    |  1311  |    3164     |   763   |   1038   |    922    |         381          |        46         |        14         |     0     |
|     B     |     SCC     |  561   |     911     |   224   |   307    |    112    |         132          |         5         |         1         |    130    |
|     C     |     AC      |  385   |    11420    |  2420   |   3584   |   1112    |         1692         |        228        |        477        |   1907    |
|     D     |    CIN 3    |  2125  |    1258     |   233   |   337    |    107    |         149          |        12         |         8         |    412    |
|     E     |    CIN 3    |  506   |    11131    |  2611   |   6249   |   1648    |         476          |        113        |        34         |     0     |
|     F     |    CIN 1    |  318   |    3365     |   954   |   1406   |    204    |         354          |        51         |        326        |    70     |
|     G     |    CIN 2    |  249   |    2759     |   691   |   1279   |    336    |         268          |        49         |        51         |    85     |
|     H     |    CIN 2    |  650   |    5216     |   993   |   983    |    425    |         2562         |        38         |        214        |     1     |
|     I     |  No lesion  |  309   |     474     |   56    |    55    |    19     |         170          |         2         |        23         |    149    |
|     J     |    CIN 1    |  261   |    1786     |   355   |   304    |    174    |         743          |        18         |        33         |    159    |
|     K     |  No lesion  |  1503  |    13102    |  2464   |   6669   |    638    |         620          |        670        |        138        |   1903    |
|     L     |    CIN 2    |  396   |    3289     |   842   |   796    |    387    |         1209         |        27         |        23         |     5     |
|     M     |    CIN 2    |  254   |    1500     |   357   |   752    |    99     |         245          |        16         |        12         |    19     |
|     N     |    CIN 3    |  248   |     911     |   258   |   402    |    67     |         136          |        10         |         6         |    32     |
|     O     |     AC      |  262   |    2904     |   792   |   1549   |    228    |         133          |        88         |        52         |    62     |
| **Total** |      -      |  9339  |    63190    |  14013  |  25710   |   6478    |         9270         |       1373        |       1412        |   4934    |
