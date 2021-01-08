# tfe_migration_poc


## Azure Region Code
```
DisplayName               Name                 RegionalDisplayName
------------------------  -------------------  -------------------------------------
East US                   eastus               (US) East US
East US 2                 eastus2              (US) East US 2
East US STG               eastusstg            (US) East US STG
South Central US          southcentralus       (US) South Central US
South Central US STG      southcentralusstg    (US) South Central US STG
West US 2                 westus2              (US) West US 2
Australia East            australiaeast        (Asia Pacific) Australia East
Southeast Asia            southeastasia        (Asia Pacific) Southeast Asia
North Europe              northeurope          (Europe) North Europe
UK South                  uksouth              (Europe) UK South
West Europe               westeurope           (Europe) West Europe
Central US                centralus            (US) Central US
North Central US          northcentralus       (US) North Central US
West US                   westus               (US) West US
South Africa North        southafricanorth     (Africa) South Africa North
Central India             centralindia         (Asia Pacific) Central India
East Asia                 eastasia             (Asia Pacific) East Asia
Japan East                japaneast            (Asia Pacific) Japan East
Korea Central             koreacentral         (Asia Pacific) Korea Central
Canada Central            canadacentral        (Canada) Canada Central
France Central            francecentral        (Europe) France Central
Germany West Central      germanywestcentral   (Europe) Germany West Central
Norway East               norwayeast           (Europe) Norway East
Switzerland North         switzerlandnorth     (Europe) Switzerland North
UAE North                 uaenorth             (Middle East) UAE North
Brazil South              brazilsouth          (South America) Brazil South
Central US (Stage)        centralusstage       (US) Central US (Stage)
East US (Stage)           eastusstage          (US) East US (Stage)
East US 2 (Stage)         eastus2stage         (US) East US 2 (Stage)
North Central US (Stage)  northcentralusstage  (US) North Central US (Stage)
South Central US (Stage)  southcentralusstage  (US) South Central US (Stage)
West US (Stage)           westusstage          (US) West US (Stage)
West US 2 (Stage)         westus2stage         (US) West US 2 (Stage)
Asia                      asia                 Asia
Asia Pacific              asiapacific          Asia Pacific
Australia                 australia            Australia
Brazil                    brazil               Brazil
Canada                    canada               Canada
Europe                    europe               Europe
Global                    global               Global
India                     india                India
Japan                     japan                Japan
United Kingdom            uk                   United Kingdom
United States             unitedstates         United States
East Asia (Stage)         eastasiastage        (Asia Pacific) East Asia (Stage)
Southeast Asia (Stage)    southeastasiastage   (Asia Pacific) Southeast Asia (Stage)
Central US EUAP           centraluseuap        (US) Central US EUAP
East US 2 EUAP            eastus2euap          (US) East US 2 EUAP
West Central US           westcentralus        (US) West Central US
South Africa West         southafricawest      (Africa) South Africa West
Australia Central         australiacentral     (Asia Pacific) Australia Central
Australia Central 2       australiacentral2    (Asia Pacific) Australia Central 2
Australia Southeast       australiasoutheast   (Asia Pacific) Australia Southeast
Japan West                japanwest            (Asia Pacific) Japan West
Korea South               koreasouth           (Asia Pacific) Korea South
South India               southindia           (Asia Pacific) South India
West India                westindia            (Asia Pacific) West India
Canada East               canadaeast           (Canada) Canada East
France South              francesouth          (Europe) France South
Germany North             germanynorth         (Europe) Germany North
Norway West               norwaywest           (Europe) Norway West
Switzerland West          switzerlandwest      (Europe) Switzerland West
UK West                   ukwest               (Europe) UK West
UAE Central               uaecentral           (Middle East) UAE Central
Brazil Southeast          brazilsoutheast      (South America) Brazil Southeast
```




### Reference
- Azure [Define your naming convention](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-naming)
- Azure [Naming rules and restrictions for Azure resources](https://docs.microsoft.com/en-gb/azure/azure-resource-manager/management/resource-name-rules)
- AWS [Standardize Names for AWS Resources for EC2 Instance](https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/ec2-instances.html)
- AWS [Standardize Names for AWS Resources for Other AWS Resources](https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/other-aws-resource-types.html)
- [Cloud Naming Convention](https://stepan.wtf/cloud-naming-convention/)
- [Workspace Naming](https://www.terraform.io/docs/cloud/workspaces/naming.html)


### Workspace rule

{서비스}{용도}\_{대분류}\_{중분류}\_{소분류}

- 서비스 : cjfw

- 용도

  | 용도                     | 표기  |
  | ----------------------- | ---- |
  | 공통 (ALL)               | A    |
  | 개발 (Development)       | D    |
  | 검증 (Quality Assurance) | Q    |
  | 관리 (Management)        | M    |
  | 운영 (Production)        | P    |
  
|Environment |	Code|
| ----------------------- | ---- |
|Development|	dev|
|Test	|test|
|System Integration Testing	|sit |
|User Acceptance Test	|uat|
|Staging |	stag |
|Pre-production	|pre |
|Production	|prod|

- 대분류 :

  - Private
  - Public
  - ALL
  - {Region code}

-  중분류 :

  - 용도 : `before` `after`
  - 서비스 단위 : `net` `inf` `db`

- 소분류 :  리소스 이름



### region code

| Code  | Original Code    | 이름                            |
| :---- | :--------------- | :------------------------------ |
| usea2 | us-east-2      | 미국 동부(오하이오)             |
| usea1 | us-east-1      | 미국 동부(버지니아 북부)        |
| uswe1 | us-west-1      | 미국 서부(캘리포니아 북부 지역) |
| uswe2 | us-west-2      | 미국 서부(오레곤)               |
| afso1 | af-south-1     | 아프리카(케이프타운)            |
| apea1 | ap-east-1      | 아시아 태평양(홍콩)             |
| apso1 | ap-south-1     | 아시아 태평양(뭄바이)           |
| apne3 | ap-northeast-3 | 아시아 태평양(오사카-로컬)      |
| apne2 | ap-northeast-2 | 아시아 태평양(서울)             |
| apse1 | ap-southeast-1 | 아시아 태평양(싱가포르)         |
| apse2 | ap-southeast-2 | 아시아 태평양(시드니)           |
| apne1 | ap-northeast-1 | 아시아 태평양(도쿄)             |
| cace1 | ca-central-1   | 캐나다(중부)                    |
| euce1 | eu-central-1   | 유럽(프랑크푸르트)              |
| euwe1 | eu-west-1      | 유럽(아일랜드)                  |
| euwe2 | eu-west-2      | 유럽(런던)                      |
| euso1 | eu-south-1     | 유럽(밀라노)                    |
| euwe3 | eu-west-3      | 유럽(파리)                      |
| euno1 | eu-north-1     | 유럽(스톡홀름)                  |
| meso1 | me-south-1     | 중동(바레인)                    |
| saea1 | sa-east-1      | 남아메리카(상파울루)            |
