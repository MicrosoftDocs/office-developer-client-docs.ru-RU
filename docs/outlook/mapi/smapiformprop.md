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
ms.openlocfilehash: 73475c5ee4e715796e06642756c05746b271d128
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812323"
---
# <a name="smapiformprop"></a>SMAPIFormProp

  
  
**Относится к**: Outlook 
  
Описание именованного свойства, используемые с формой. 
  
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

## <a name="members"></a>Members

 **ulFlags**
  
> Флаги, используемые для различения формат строк в структуре **SMAPIFormProp** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Строк, возвращаемых находятся в формате Юникод. Если MAPI_UNICODE не задано, они в формате ANSI.
    
 **nPropType**
  
> Тип именованного свойства с наиболее важных word, равным нулю. 
    
 **nmid**
  
> Имя для именованного свойства, который включает структуру **идентификатор GUID** , идентифицирующий значение свойства set и числовой или строка, которая представляет имя интерфейса идентификатор и формы. 
    
 **pszDisplayName**
  
> Указатель на отображаемое имя именованное свойство.
    
 **nSpecialType**
  
> Значение, указывающее тип данных, включенных в член **u** . Ниже приведены возможные значения: 
    
FPST_VANILLA 
  
> Член **u** не содержит перечисление. 
    
FPST_ENUM_PROP 
  
> Член **u** содержит структуру, которая описывает перечисление. 
    
 **u**
  
> Объединение, описывающие связь между имя и номер именованное свойство. С помощью некоторых свойств, **u** элемента будет пустым. С другими свойствами представленным в структуре, состоящий из следующих элементов: 
    
 **nmidIdx**
  
> Структура [MAPINAMEID](mapinameid.md) , содержащая набор свойств и идентификатор для именованного свойства. 
    
 **cfpevAvailable**
  
> Число структур [SMAPIFormPropEnumVal](smapiformpropenumval.md) в массиве, на который указывает член **pfpevAvailable** . 
    
 **pfpevAvailable**
  
> Указатель на массив структур **SMAPIFormPropEnumVal** , каждая из которых содержит значение именованного свойства. 
    
## <a name="remarks"></a>Замечания

Структура **SMAPIFormProp** содержит информацию о свойствах формы, используется как часть определения интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) ; **nSpecialType** содержит тег, которое применяется для объединения **u** , который является частью **SMAPIFormProp**.
  
## <a name="see-also"></a>См. также



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Структуры MAPI](mapi-structures.md)

