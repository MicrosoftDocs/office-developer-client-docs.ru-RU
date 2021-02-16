---
title: Constants (Outlook exported APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: В этом разделе содержатся определения констант для API, экспортируемой Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319875"
---
# <a name="constants-outlook-exported-apis"></a>Constants (Outlook exported APIs)

В этом разделе содержатся определения констант для API, экспортируемой Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Определения для поддержки часовой пояс

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Определения для поддержки категорий

|**Константа**|**Определение**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Прочие идентификаторы диспетчера

Outlook предоставляет следующие идентификаторы диспетчера (dispids), чтобы разработчики могли использовать [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) для доступа к соответствующему свойству или методу или прослушивать соответствующее событие. 
  
|**Связанная константа**|**Непись значения**|**Описание**|**Применимый интерфейс**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Используется для вызова соответствующего свойства элемента, чтобы проверить, был ли элемент изменен, но не был сохранен.  <br/> |Объекты уровня элемента  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Используется для вызова соответствующего метода в проводнике или инспекторе, чтобы указать, следует ли отображать изображение контакта на основе заданного аргумента.  <br/> |Проводник или инспектор  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Используется для обработки события из функции **IDispatch::Invoke,** которая сгорает перед операцией печати.  <br/> |Для приложений  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Используется для обработки события из функции **IDispatch::Invoke,** которая активна, когда Outlook завершил чтение свойств элемента.  <br/> |Объекты уровня элемента  <br/> |
   
## <a name="see-also"></a>См. также

- [Экспортированные API Outlook](outlook-exported-apis.md)
- [Сведения об интерфейсах API, экспортируемых Outlook](about-apis-exported-by-outlook.md)
- [Определение того, был ли элемент Outlook изменен, но не сохранен (Вспомогательная справка по Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)  
- [Указание на необходимость отображать изображение контакта в Outlook (Дополнительная справка по Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [Доступные события и их dispids (экспортные API Outlook)](available-events-and-their-dispids-outlook-exported-apis.md)

