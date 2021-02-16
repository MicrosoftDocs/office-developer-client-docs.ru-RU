---
title: Каноническое свойство PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319512"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Каноническое свойство PidLidContactItemData

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Используется для отображения контактных данных.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidContactItemData  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008007  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если имеется, свойство должно иметь шесть записей, каждая из которых соответствует видимому полю в пользовательском интерфейсе приложения.
  
|**Один индекс в много значение свойства**|**Значение должно быть одним из следующих значений:**|**Описание**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |Приложение должно отображать домашний адрес контакта.  <br/> |
|1   <br/> |0x00000002 или 0x00000000  <br/> |Приложение должно отображать работу контакта.  <br/> |
|1   <br/> |0x00000003  <br/> |Приложение должно отобразить другой адрес контакта.  <br/> |
|2   <br/> |0x00008080  <br/> |В приложении должен отображаться адрес Email1.  <br/> |
|2   <br/> |0x00008090  <br/> |В приложении должен отображаться адрес Email2.  <br/> |
|2   <br/> |0x000080A0  <br/> |В приложении должен отображаться адрес Email3.  <br/> |
|3,4,5,6  <br/> |PropertyID любого из свойств телефона или номеров факсов, указанных [в [MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |Приложение должно отобразить соответствующее свойство.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
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

