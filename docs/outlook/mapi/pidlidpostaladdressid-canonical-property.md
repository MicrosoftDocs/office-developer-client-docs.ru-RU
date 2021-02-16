---
title: Каноническое свойство PidLidPostalAddressId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPostalAddressId
api_type:
- COM
ms.assetid: 30fdfb20-1e12-442a-bfa0-8c18c15fa5c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 83f3c0559a3317de3789f8c93d024f08ada3e735
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315997"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>Каноническое свойство PidLidPostalAddressId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, какой физический адрес является адресом электронной почты контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidPostalAddressId  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008022  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если задан, это свойство должно иметь одно из значений, указанных в таблице ниже или [в [MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx). Если значение не за установлено, приложение должно предполагать, что значением является "0x00000000".
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |В качестве адреса для рассылки не выбран ни один адрес. **PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([PidTagCountry](pidtagcountry-canonical-property.md)), **dispidAddressCountryCode** ([PidLidAddressCountryCode)](pidlidaddresscountrycode-canonical-property.md)и **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) не должны быть установлены.  <br/> |
|0x00000001  <br/> |Домашний адрес — это адрес электронной почты. Значения свойств **PR_STREET_ADDRESS,** **PR_LOCALITY,** **PR_STATE_OR_PROVINCE,** **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode** и **PR_POSTAL_ADDRESS** должны быть равны значениям свойств **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet),](pidtaghomeaddressstreet-canonical-property.md) **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)), **PR_HOME_ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeHome)AddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md)), **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode),](pidtaghomeaddresspostalcode-canonical-property.md) **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md)), **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry),](pidtaghomeaddresscountry-canonical-property.md) **dispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode)](pidlidhomeaddresscountrycode-canonical-property.md)и **dispidHomeAddress** ([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) соответственно.  <br/> |
|0x00000002  <br/> |Рабочий адрес — это адрес электронной почты. Значения свойств **PR_STREET_ADDRESS,** **PR_LOCALITY,** **PR_STATE_OR_PROVINCE,** **PR_POSTAL_CODE,** **PR_POST_OFFICE_BOX,** **PR_COUNTRY,** **dispidAddressCountryCode** и **PR_POSTAL_ADDRESS** должны быть равны значениям. of the **dispidWorkAddressStreet** ([PidLidWorkAddressStreet),](pidlidworkaddressstreet-canonical-property.md) **dispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)), **dispidWorkAddressState** ([PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)), **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode),](pidlidworkaddresspostalcode-canonical-property.md) **dispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)), **dispidWorkAddressCountry** ([Свойства PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)), **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode)](pidlidworkaddresscountrycode-canonical-property.md)и **dispidWorkAddress** ([PidLidWorkAddress)](pidlidworkaddress-canonical-property.md)соответственно.  <br/> |
|0x00000003  <br/> |Другой адрес — это адрес электронной почты. Значения свойств **PR_STREET_ADDRESS,** **PR_LOCALITY,** **PR_STATE_OR_PROVINCE,** **PR_POSTAL_CODE,** **PR_POST_OFFICE_BOX,** **PR_COUNTRY,** **dispidAddressCountryCode** и **PR_POSTAL_ADDRESS** должны быть равны значениям свойств **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet),](pidtagotheraddressstreet-canonical-property.md) **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)), **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** ([PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)), **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)), **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), **dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode),](pidlidotheraddresscountrycode-canonical-property.md)and **dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) properties, соответственно.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

