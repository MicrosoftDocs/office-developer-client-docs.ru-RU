---
title: Каноническое свойство PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335800"
---
# <a name="pidtagemsabserver-canonical-property"></a>Каноническое свойство PidTagEmsAbServer

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает путь к контейнеру адресной книги в автономном сценарии или полное доменное имя сервера глобального каталога, на котором находится контейнер адресной книги, в сетевом сценарии.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A PR_EMS_AB_SERVER_W  <br/> |
|Идентификатор:  <br/> |0xFFFE  <br/> |
|Тип данных:  <br/> |PT_TSTRING  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство имеет тип свойства reseted to **PT_UNICODE** при компиляции с `UNICODE` символом на платформе Юникода и **PT_STRING8** , если он не компилируется вместе с `UNICODE` символом. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Задает определения свойств.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

