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
<img src="https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/_images/ready/resource-naming.png">

- Azure [Naming rules and restrictions for Azure resources](https://docs.microsoft.com/en-gb/azure/azure-resource-manager/management/resource-name-rules)
- AWS [Standardize Names for AWS Resources for EC2 Instance](https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/ec2-instances.html)
<img src="https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/images/tagimage3.png">

- AWS [Standardize Names for AWS Resources for Other AWS Resources](https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/other-aws-resource-types.html) : account-name(enviroment) : resource-name	: resource-type
- [Cloud Naming Convention](https://stepan.wtf/cloud-naming-convention/) : [prefix]-[project]-[env]-[resource]-[location]-[description]-[suffix]
- [Workspace Naming](https://www.terraform.io/docs/cloud/workspaces/naming.html) : COMPONENT-ENVIRONMENT-REGION


### Workspace rule

{서비스|프로젝트명}{환경}\_{대분류}\_{중분류}\_{소분류}

- 서비스 : hcp_tfe

- 환경
 
|Environment |	Code|
| ----------------------- | ---- |
|Development|	dev / D|
|Test	|test / T|
| Quality Assurance | qa /Q   |
|System Integration Testing	|sit /I| 
|User Acceptance Test	|uat/ A|
|Staging |	stag /S|
|Production	|prod / P|
|Disaster Recovery	|dr /R|


- 대분류 : 용도

  - Private (pri)
  - Public (pub)
  - common (공통) com
  - 

-  중분류 : Region Code
-  소분류 : 
  - 서비스 단위 `net` `inf` `db`
  - 리소스 타입: `aks`
  
예) tfeD_A_kc_inf_aks : TFE로 관리하는 개발 환경, 한국 중부, 인프라, AKS


### region code

<table class="tg">
  <tr>
    <th class="tg-fymr">Geography</th>
    <th class="tg-fymr">Country</th>
    <th class="tg-fymr">Region</th>
    <th class="tg-7btt">Code</th>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">Central US</td>
    <td class="tg-c3ow">CUS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">East US 2</td>
    <td class="tg-c3ow">EUS2</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">East US</td>
    <td class="tg-c3ow">EUS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">North Central US</td>
    <td class="tg-c3ow">NCUS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">South Central US</td>
    <td class="tg-c3ow">NSUS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">West US 2</td>
    <td class="tg-c3ow">WUS2</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">USA</td>
    <td class="tg-0pky">West Central US</td>
    <td class="tg-c3ow">WCUS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">West US,US DoD Central</td>
    <td class="tg-c3ow">WUSD</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US DoD East</td>
    <td class="tg-c3ow">USDE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US Gov. Arizona</td>
    <td class="tg-c3ow">USGA</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US Gov. Iowa</td>
    <td class="tg-c3ow">USGI</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US Gov. Texas</td>
    <td class="tg-c3ow">USGT</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US Gov. Virginia</td>
    <td class="tg-c3ow">USGV</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US Sec East</td>
    <td class="tg-c3ow">USSE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Azure Gov</td>
    <td class="tg-0pky">US Sec West</td>
    <td class="tg-c3ow">USSW</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Canada</td>
    <td class="tg-0pky">Canada Central</td>
    <td class="tg-c3ow">CC</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Canada</td>
    <td class="tg-0pky">Canade East</td>
    <td class="tg-c3ow">CE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Americas</td>
    <td class="tg-0pky">Brazil</td>
    <td class="tg-0pky">Brazil South</td>
    <td class="tg-c3ow">BS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">North Europe</td>
    <td class="tg-c3ow">NE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">West Europe</td>
    <td class="tg-c3ow">WE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">UK</td>
    <td class="tg-0pky">UK South</td>
    <td class="tg-c3ow">UKS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">UK</td>
    <td class="tg-0pky">UK West</td>
    <td class="tg-c3ow">UKW</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Germany</td>
    <td class="tg-0pky">Germany North</td>
    <td class="tg-c3ow">GN</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Germany</td>
    <td class="tg-0pky">Germany West Central</td>
    <td class="tg-c3ow">GWC</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Switzerland</td>
    <td class="tg-0pky">Switzerland North</td>
    <td class="tg-c3ow">SN</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Switzerland</td>
    <td class="tg-0pky">Switzerland West</td>
    <td class="tg-c3ow">SW</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Norway</td>
    <td class="tg-0pky">Norway West</td>
    <td class="tg-c3ow">NW</td>
  </tr>
  <tr>
    <td class="tg-0pky">Europe</td>
    <td class="tg-0pky">Norway</td>
    <td class="tg-0pky">Norway East</td>
    <td class="tg-c3ow">NE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">East Asia</td>
    <td class="tg-c3ow">EA</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Southeast Asia</td>
    <td class="tg-c3ow">SA</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Australia</td>
    <td class="tg-0pky">Australia Central</td>
    <td class="tg-c3ow">AC</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Australia</td>
    <td class="tg-0pky">Australia Central 2</td>
    <td class="tg-c3ow">AC2</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Australia</td>
    <td class="tg-0pky">Australia East</td>
    <td class="tg-c3ow">AE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Australia</td>
    <td class="tg-0pky">Australia Southeast</td>
    <td class="tg-c3ow">AS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">China</td>
    <td class="tg-0pky">China East</td>
    <td class="tg-c3ow">CE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">China</td>
    <td class="tg-0pky">China North</td>
    <td class="tg-c3ow">CN</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">China</td>
    <td class="tg-0pky">China East 2</td>
    <td class="tg-c3ow">CE2</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">China</td>
    <td class="tg-0pky">China North 2</td>
    <td class="tg-c3ow">CN2</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">India</td>
    <td class="tg-0pky">Central India</td>
    <td class="tg-c3ow">CI</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">India</td>
    <td class="tg-0pky">South India</td>
    <td class="tg-c3ow">SI</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">India</td>
    <td class="tg-0pky">West India</td>
    <td class="tg-c3ow">WI</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Japan</td>
    <td class="tg-0pky">Japan East</td>
    <td class="tg-c3ow">JE</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Japan</td>
    <td class="tg-0pky">Japan West</td>
    <td class="tg-c3ow">JW</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Korea</td>
    <td class="tg-0pky">Korea Central</td>
    <td class="tg-c3ow">KC</td>
  </tr>
  <tr>
    <td class="tg-0pky">Asia Pacific</td>
    <td class="tg-0pky">Korea</td>
    <td class="tg-0pky">Korea South</td>
    <td class="tg-c3ow">KS</td>
  </tr>
  <tr>
    <td class="tg-0pky">Middle East and Africa</td>
    <td class="tg-0pky">South Africa</td>
    <td class="tg-0pky">South Africa North</td>
    <td class="tg-c3ow">SAN</td>
  </tr>
  <tr>
    <td class="tg-0pky">Middle East and Africa</td>
    <td class="tg-0pky">South Africa</td>
    <td class="tg-0pky">South Africa West</td>
    <td class="tg-c3ow">SAW</td>
  </tr>
  <tr>
    <td class="tg-0pky">Middle East and Africa</td>
    <td class="tg-0pky">UAE</td>
    <td class="tg-0pky">UAE Central</td>
    <td class="tg-c3ow">UC</td>
  </tr>
  <tr>
    <td class="tg-0pky">Middle East and Africa</td>
    <td class="tg-0pky">UAE</td>
    <td class="tg-0pky">UAE North</td>
    <td class="tg-c3ow">UN</td>
  </tr>
</table>
