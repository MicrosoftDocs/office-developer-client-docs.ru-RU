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
  
Указывает, какой физический адрес является почтовым адресом контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидпосталаддрессид  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008022  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство задано, это свойство должно иметь одно из значений, указанных в таблице ниже или в [[MS – оксокнтк]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx). Если не задано, то приложение должно предполагать, что значение равно "0x00000000".
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |В качестве почтового адреса не выбран адрес. **PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md)), **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **PR_COUNTRY** ([PidTagCountry](pidtagcountry-canonical-property.md)), **диспидаддресскаунтрикоде** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) и **PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) не должно быть задано.  <br/> |
|0x00000001  <br/> |Домашний адрес — это почтовый адрес. Значения свойств **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **диспидаддресскаунтрикоде**и **PR_POSTAL_ADDRESS** должны совпадать со значениями **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md)), **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)), **PR_HOME_ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md) **), PR_HOME_ADDRESS_POSTAL_CODE (PidTagHomeAddressPostalCode** [),](pidtaghomeaddresspostalcode-canonical-property.md) **PR_HOME_ADDRESS_POST_OFFICE_BOX** [(PidTagHomeAddressPostOfficeBox),](pidtaghomeaddresspostofficebox-canonical-property.md) **PR_HOME_ADDRESS_COUNTRY** (PidTagHomeAddressCountry), диспидхомеаддресскаунтрикоде ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)),[(диспидхомеаддресс)](pidtaghomeaddresscountry-canonical-property.md), **PidLidHomeAddress** () и **dispidHomeAddress** ([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) соответственно.  <br/> |
|0x00000002  <br/> |Рабочий адрес — это почтовый адрес. Значения свойств **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE**, **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, PidLidWorkAddressStreet и **dispidAddressCountryCode** **PR_POSTAL_ADDRESS** должны совпадать со значениями **диспидворкаддрессстрит** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)), **диспидворкаддрессЦити** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)[),](pidlidworkaddressstate-canonical-property.md) **диспидворкаддрессстате** (PidLidWorkAddressState), **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)), **dispidWorkAddressPostOfficeBox (PidLidWorkAddressPostOfficeBox** [),](pidlidworkaddresspostofficebox-canonical-property.md) **dispidWorkAddressCountry (** [PidLidWorkAddressCountry),](pidlidworkaddresscountry-canonical-property.md)dispidWorkAddressCountryCode (PidLidWorkAddressCountryCode), dispidWorkAddress (PidLidWorkAddress), **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)) и **dispidWorkAddress** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)) соответственно.  <br/> |
|0x00000003  <br/> |Другой адрес является почтовым адресом. Свойства, **PR_STREET_ADDRESS**, **PR_LOCALITY**, **PR_STATE_OR_PROVINCE** **,** **PR_POSTAL_CODE**, **PR_POST_OFFICE_BOX**, **PR_COUNTRY**, PidTagOtherAddressCity и **PR_POSTAL_ADDRESS** должны совпадать со значениями **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)), **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md) **), PR_OTHER_ADDRESS_STATE_OR_PROVINCE (** [PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)), **PR_OTHER_ADDRESS_POSTAL_CODE** [(PidTagOtherAddressPostalCode),](pidtagotheraddresspostalcode-canonical-property.md) **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), **диспидосераддресскаунтрикоде** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) и **диспидосераддресс** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) соответственно.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

