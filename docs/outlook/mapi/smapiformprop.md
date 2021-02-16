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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает именуемую свойство, используемую с формой. 
  
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
  
> Возвращенные строки имеют формат Юникод. Если MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
 **nPropType**
  
> Тип именоваемого свойства, для которого для наиболее важного слова установлено значение "ноль". 
    
 **nmid**
  
> Имя имененного свойства, которое включает в себя структуру **GUID,** определяя набор свойств, и числовые или строковые значения, которые представляют идентификатор интерфейса и имя формы. 
    
 **pszDisplayName**
  
> Указатель на отображаемого имени именоваемого свойства.
    
 **nSpecialType**
  
> Значение, описывающие тип данных, включенных в **член u.** Возможные значения: 
    
FPST_VANILLA 
  
> Член **u** не содержит enumeration. 
    
FPST_ENUM_PROP 
  
> Член **u** содержит структуру, описываемую в описании. 
    
 **u**
  
> Объединение, описывающие связь между именем и номером именоваемого свойства. При использовании некоторых свойств член **u** пуст. С другими свойствами он представлен в структуре, состоящей из следующих членов: 
    
 **nmidIdx**
  
> Структура [MAPINAMEID,](mapinameid.md) которая содержит набор свойств и идентификатор для именоваемой свойства. 
    
 **cfpevAvailable**
  
> Количество структур [SMAPIFormPropEnumVal в](smapiformpropenumval.md) массиве, на который указывает **член pfpevAvailable.** 
    
 **pfpevAvailable**
  
> Указатель на массив структур **SMAPIFormPropEnumVal,** каждая из которых содержит значение для именоваемого свойства. 
    
## <a name="remarks"></a>Примечания

Структура **SMAPIFormProp** содержит сведения о свойстве формы, используемом как часть определений интерфейса [IMAPIFormInfo;](imapiforminfoimapiprop.md) **nSpecialType** содержит тег, который применяется к объединение **u,** которое является частью **SMAPIFormProp**.
  
## <a name="see-also"></a>См. также



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Структуры MAPI](mapi-structures.md)

