---
title: Каноническое свойство PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327484"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Каноническое свойство PidLidSharingFlavor

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обозначается как свойство общего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingFlavor  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008A18  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общий доступ  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства должно быть одним из следующих значений:
  
|**Значение**|**Тип объекта Sharing Message**|
|:-----|:-----|
|0x00020310  <br/> |Приглашение к совместному доступу для специальной папки.  <br/> |
|0x00000310  <br/> |Приглашение к совместному доступу для папки, которая не является специальной.  <br/> |
|0x00020500  <br/> |Запрос на общий доступ.  <br/> |
|0x00020710  <br/> |Приглашение к совместному доступу для специальной папки и запрос на общий доступ для эквивалентной специальной папки получателя.  <br/> |
|0x00025100  <br/> |Ответ на совместное использование, отвеяющий запрос.  <br/> |
|0x00023310  <br/> |Ответ общего доступа, который принимает запрос (также тип приглашения к совместному доступу).  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Папки почтовых ящиков разделяются между клиентами.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

