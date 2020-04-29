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
  
Описывает именованное свойство, используемое с формой. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
   
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
  
> Флаги, используемые для различения формата строк в структуре **смапиформпроп** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Возвращаемые строки имеют формат Юникод. Если MAPI_UNICODE не заданы, строки представлены в формате ANSI.
    
 **нпроптипе**
  
> Тип именованного свойства с наиболее значительным набором слов, равным нулю. 
    
 **нмид**
  
> Имя для именованного свойства, которое включает структуру **GUID** , определяющую набор свойств, а также числовое или строковое значение, представляющее идентификатор интерфейса и имя формы. 
    
 **псздисплайнаме**
  
> Указатель на отображаемое имя именованного свойства.
    
 **нспеЦиалтипе**
  
> Значение, описывающее тип данных, включенных в элемент **u** . Возможны следующие значения: 
    
FPST_VANILLA 
  
> Член **u** не содержит перечисление. 
    
FPST_ENUM_PROP 
  
> Член **u** содержит структуру, описывающую перечисление. 
    
 **u**
  
> Объединение, описывающее связь между именем и номером именованного свойства. При использовании некоторых свойств член **u** пуст. С другими свойствами она представлена в структуре, состоящей из следующих элементов: 
    
 **нмидидкс**
  
> Структура [мапинамеид](mapinameid.md) , содержащая набор свойств и идентификатор для именованного свойства. 
    
 **кфпеваваилабле**
  
> Количество структур [смапиформпропенумвал](smapiformpropenumval.md) в массиве, на которое указывает элемент **пфпеваваилабле** . 
    
 **пфпеваваилабле**
  
> Указатель на массив структур **смапиформпропенумвал** , каждый из которых содержит значение именованного свойства. 
    
## <a name="remarks"></a>Примечания

Структура **смапиформпроп** содержит сведения о свойстве формы, используемом в составе определений интерфейса [имапиформинфо](imapiforminfoimapiprop.md) ; **нспеЦиалтипе** содержит тег, который применяется к объединению **u** , которое входит в состав **смапиформпроп**.
  
## <a name="see-also"></a>См. также



[MAPINAMEID](mapinameid.md)
  
[SMAPIFormPropEnumVal](smapiformpropenumval.md)


[Структуры MAPI](mapi-structures.md)

