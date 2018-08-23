---
title: Constants (Outlook exported APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: В этом разделе содержатся определения констант для API, которые экспортируются Outlook.
ms.openlocfilehash: 8b7a9d70b2fc5d26c52a8729797221a44526360c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564467"
---
# <a name="constants-outlook-exported-apis"></a>Constants (Outlook exported APIs)

В этом разделе содержатся определения констант для API, которые экспортируются Outlook.
  
## <a name="definitions-for-time-zone-support"></a>Поддерживает определения для часового пояса

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a>Поддерживает определения для категории

|**Constant**|**Определение**|
|:-----|:-----|
|PCAFSIF_MSGEID_IS_SEARCH_KEY  <br/> |0x00000001  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a>Идентификаторы прочие диспетчера

Outlook предоставляет следующие идентификаторов отправки (DISPID), чтобы [IDispatch::Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) могут использоваться разработчиками для доступа к соответствующее свойство или метод или прослушивание для соответствующих событий. 
  
|**Связанные константа**|**Значение DispId**|**Описание**|**Доступный интерфейс**|
|:-----|:-----|:-----|:-----|
|**dispidFDirty** <br/> |0xF024  <br/> |Используется для вызова соответствующее свойство элемента для проверки, является ли элемент был изменен, но не был сохранен.  <br/> |Объекты на уровне элементов  <br/> |
|**dispidShowSenderPhoto** <br/> |0xF0D0  <br/> |Используется для вызова на проводника или инспектора, укажите, нужно ли отображать фотографии контакта, на основании данный аргумент через соответствующий метод.  <br/> |Проводника или инспектора  <br/> |
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Используется для обработки событий из функции **IDispatch::Invoke** , которое вызывается перед операцией печати.  <br/> |Для приложения  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Используется для обработки событий из функции **IDispatch::Invoke** , которое вызывается после завершения чтение свойств элемента Outlook.  <br/> |Объекты на уровне элементов  <br/> |
   
## <a name="see-also"></a>См. также

- [Экспортированные API Outlook](outlook-exported-apis.md)
- [Сведения об интерфейсах API, экспортируемых Outlook](about-apis-exported-by-outlook.md)
- [Определить, является ли элемент Outlook был изменен, но не сохраняются (Outlook дополнительные справочные материалы по)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [Укажите, нужно ли отображать фотографии контакта в Outlook (Outlook дополнительные справочные материалы по)](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
- [Доступные события и их идентификаторы DISPID (Outlook экспортировать API-интерфейсы)](available-events-and-their-dispids-outlook-exported-apis.md)

