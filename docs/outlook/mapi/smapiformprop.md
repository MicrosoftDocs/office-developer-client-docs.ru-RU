---
title: SMAPIFormProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormProp
api_type:
- COM
ms.assetid: 80f1c2e0-3567-4b16-86cb-d5e6ac95c2ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 968f9e1dad3a233b31f0ce29d3ce935b1257948c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416701"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает имя свойства, используемой с помощью формы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct _SMAPIFormProp
{
  ULONG ulFlags;
  ULONG nPropType;
  MAPINAMEID nmid;
  LPSTR pszDisplayName;
  FORMPROPSPECIALTYPE nSpecialType;
  union
  {
    struct
    {
      MAPINAMEID nmidIdx;
      ULONG cfpevAvailable;
      LPMAPIFORMPROPENUMVAL pfpevAvailable;
    } s1;
  } u;
} SMAPIFormProp, FAR * LPMAPIFORMPROP;

```

## <a name="members"></a>Элементы

 **ulFlags**
  
> Флаги, используемые для различия формата строк в **структуре SMAPIFormProp.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Возвращенные строки находятся в формате Unicode. Если MAPI_UNICODE не установлено, строки находятся в формате ANSI.
    
 **nPropType**
  
> Тип имени свойства, с самым значительным значением слова до нуля. 
    
 **nmid**
  
> Имя имени свойства, которое включает в себя структуру **GUID,** определяя набор свойств, а также числовые или строковые значения, которые представляют идентификатор интерфейса и имя формы. 
    
 **pszDisplayName**
  
> Указатель на отображаемого имени имени свойства.
    
 **nSpecialType**
  
> Значение, описывающие тип данных,  включенных в u-member. Возможные значения: 
    
FPST_VANILLA 
  
> Член **u** не содержит переумерия. 
    
FPST_ENUM_PROP 
  
> Член **u** содержит структуру, описываемую переумерия. 
    
 **u**
  
> Союз, описывающий связь между именем и номером имени свойства. Используя некоторые свойства, **u-член** пуст. С другими свойствами он представлен в структуре, состоящей из следующих участников: 
    
 **nmidIdx**
  
> Структура [MAPINAMEID,](mapinameid.md) которая содержит набор свойств и идентификатор для имени свойства. 
    
 **cfpevAvailable**
  
> Количество структур [SMAPIFormPropEnumVal](smapiformpropenumval.md) в массиве, на который указывает **член pfpevAvailable.** 
    
 **pfpevAvailable**
  
> Указатель на массив структур **SMAPIFormPropEnumVal,** каждая из которых содержит значение для имени свойства. 
    
## <a name="remarks"></a>Примечания

Структура **SMAPIFormProp** содержит сведения о свойстве формы, используемом в рамках определений интерфейса [IMAPIFormInfo;](imapiforminfoimapiprop.md) **nSpecialType** содержит тег, применимый к **союзу u,** который является частью **SMAPIFormProp**.
  
## <a name="see-also"></a>См. также



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Структуры MAPI](mapi-structures.md)

