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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, какой физический адрес является почтовым адресом контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидпосталаддрессид  <br/> |
|Набор свойств:  <br/> |Псетид_аддресс  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008022  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство задано, это свойство должно иметь одно из значений, указанных в таблице ниже или в [[MS – оксокнтк]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx). Если не задано, то приложение должно предполагать, что значение равно "0x00000000".
  
|**Value**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |В качестве почтового адреса не выбран адрес. **Пр_стрит_аддресс** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)), **пр_локалити** ([PidTagLocality](pidtaglocality-canonical-property.md)), **пр_стате_ор_провинце** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)), **пр_постал_коде** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)), **пр_каунтри** ([ PidTagCountry](pidtagcountry-canonical-property.md)), **диспидаддресскаунтрикоде** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) и **пр_постал_аддресс** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) не должны быть заданы.  <br/> |
|0x00000001  <br/> |Домашний адрес — это почтовый адрес. Значения параметров **пр_стрит_аддресс**, **пр_локалити**, **пр_стате_ор_провинце**, **Пр_постал_коде**, **пр_пост_оффице_бокс** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)), **PR_COUNTRY**, **dispidAddressCountryCode **, а свойства **пр_постал_аддресс** должны быть равны значениям **пр_хоме_аддресс_стрит** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md)), **пр_хоме_аддресс_Цити** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)), **пр_хоме_ АДДРЕСС_СТАТЕ_ОР_ПРОВИНЦЕ** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md)), **пр_хоме_аддресс_постал_коде** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md)), **пр_хоме_аддресс_пост_оффице_бокс** ([ PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md)), **пр_хоме_аддресс_каунтри** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md)), **диспидхомеаддресскаунтрикоде** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)) и **диспидхомеаддресс** ( [PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) соответственно.  <br/> |
|0x00000002  <br/> |Рабочий адрес — это почтовый адрес. Значения параметров **пр_стрит_аддресс**, **пр_локалити**, **пр_стате_ор_провинце**, **пр_постал_коде**, **пр_пост_оффице_бокс**, **PR_COUNTRY**, **dispidAddressCountryCode**и **PR_POSTAL_ADDRESS **свойства должны быть равны значениям параметра **диспидворкаддрессстрит** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)), **диспидворкаддрессЦити** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)), **диспидворкаддрессстате** ([ PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md)), **диспидворкаддресспосталкоде** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md)), **диспидворкаддресспостоффицебокс** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)), **диспидворкаддресскаунтри **([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md)), **диспидворкаддресскаунтрикоде** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)) и **диспидворкаддресс** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)) соответственно.  <br/> |
|0x00000003  <br/> |Другой адрес является почтовым адресом. Значения параметров, **пр_стрит_аддресс**, **пр_локалити**, **пр_стате_ор_провинце**, **пр_постал_коде**, **пр_пост_оффице_бокс**, **PR_COUNTRY**, **dispidAddressCountryCode**и **PR_POSTAL_ADDRESS. **свойства должны быть равны значениям параметра **пр_осер_аддресс_стрит** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)), **пр_осер_аддресс_Цити** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)), **пр_осер_аддресс_стате_ор_провинце** ( [PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)), **пр_осер_аддресс_постал_коде** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)), **пр_осер_аддресс_пост_оффице_бокс** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)), ** свойства Диспидосераддресскаунтрикоде** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) и **диспидосераддресс** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) соответственно.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

