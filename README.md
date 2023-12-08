# TMID: Trademark Infringement Detection Dataset

![Ant Group Logo](https://gw.alipayobjects.com/mdn/rms_27e257/afts/img/A*70AsSL23VKYAAAAAAAAAAAAAARQnAQ)
![Monash University Logo](https://www.monash.edu/__data/assets/git_bridge/0006/509343/deploy/mysource_files/monash-logo-mono.svg)

## Description
This repository hosts the "TMID: A Comprehensive Real-world Dataset for Trademark Infringement Detection in E-Commerce," a dataset developed by Ant Group and Monash University. The dataset supports machine learning models in identifying potential trademark infringements based on merchant registration data and trademark identifiers.

## Dataset Files
The dataset comprises three CSV files:
- `data_with_rt.csv`: Includes reasoning traces.
- `data.csv`: Same structure as `data_with_rt.csv` but without the reasoning traces column.

## Data Format
Each record in the CSV files is composed of the following fields:
- `target_content`: The specific content related to the trademark topic.
- `label`: Binary label (`1` for infringement, `0` for non-infringement).
- `registration_name`: The name used by merchants for registration.
- `service_description`: Description of services provided by the merchant.
- `slogan`: The merchant's slogan, if any.
- `merchant_name`: The legal name of the merchant's company.
- `merchant_industry_category`: The industry category to which the merchant belongs.
- `trademark_name`: The name of the potentially infringed trademark.
- `trademark_industry_category`: The industry category of the trademark.
- `ecommerce_type`: The type of e-commerce service related to the trademark.
- `reasoning_trace`: (Only in `data_with_rt.csv`) The reasoning behind the judgment for potential infringement.

## Example Entry from `data_with_rt.csv`
```csv
target_content,label,registration_name,service_description,slogan,merchant_name,merchant_industry_category,trademark_name,trademark_industry_category,ecommerce_type,reasoning_trace
得知物流,1,得知物流,,,音手哩品司实挑（中山）有限公司,'交通运输、仓储和邮政业',徳知物流,['邮政业'],快递物流,The text [得知物流] uses a name that is identical or similar to the brand [徳知物流], potentially causing confusion. Considering the text [得知物流], the registration information and the services or goods offered by the brand [徳知物流] belong to the same industry category. The merchant name [音手哩品司实挑（中山）有限公司] is not associated with the brand [徳知物流].
```

## Usage
This dataset is designed for academic and educational purposes within the field of legal compliance and trademark infringement detection. When using this dataset, please ensure to cite the associated paper and attribute the source as outlined in the citation section below.

## Citation
If you use this dataset in your research or work, please cite the following paper:
```
@inproceedings{hu-etal-2023-tmid,
    title = "{TMID}: A Comprehensive Real-world Dataset for Trademark Infringement Detection in {E}-Commerce",
    author = "Hu, Tongxin  and
      Li, Zhuang  and
      Jin, Xin  and
      Qu, Lizhen  and
      Zhang, Xin",
    editor = "Wang, Mingxuan  and
      Zitouni, Imed",
    booktitle = "Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing: Industry Track",
    month = dec,
    year = "2023",
    address = "Singapore",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.emnlp-industry.18",
    pages = "176--184",
    abstract = "Annually, e-commerce platforms incur substantial financial losses due to trademark infringements, making it crucial to identify and mitigate potential legal risks tied to merchant information registered to the platforms. However, the absence of high-quality datasets hampers research in this area. To address this gap, our study introduces TMID, a novel dataset to detect trademark infringement in merchant registrations. This is a real-world dataset sourced directly from Alipay, one of the world{'}s largest e-commerce and digital payment platforms. As infringement detection is a legal reasoning task requiring an understanding of the contexts and legal rules, we offer a thorough collection of legal rules and merchant and trademark-related contextual information with annotations from legal experts. We ensure the data quality by performing an extensive statistical analysis. Furthermore, we conduct an empirical study on this dataset to highlight its value and the key challenges. Through this study, we aim to contribute valuable resources to advance research into legal compliance related to trademark infringement within the e-commerce sphere.",
}
```
## Contact
For queries or further information regarding this dataset, please open an issue in this repository or refer to the [paper](https://aclanthology.org/2023.emnlp-industry.18/) for contact details.