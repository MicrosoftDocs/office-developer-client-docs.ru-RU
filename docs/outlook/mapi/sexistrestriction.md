---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571950"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описание ограничений exist, который используется для проверки, является ли определенное свойство существует в виде столбцов в таблице. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Зарезервировано; должно быть равно нулю. 
    
 **ulPropTag**
  
> Свойство tag определение столбца проверяется на наличие в каждой строке.
    
 **ulReserved2**
  
> Зарезервировано; должно быть равно нулю.
    
## <a name="remarks"></a>Замечания

Ограничение exist используется для обеспечения достоверные результаты для других типов ограничений, в которых используются свойства, такие как свойства и содержимое ограничения. Если свойство не существует ограничение, которое включает в себя свойства передается [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md) , результаты ограничение не определено. Путем создания **и** ограничение, которое присоединяется ограничение свойства ограничению exist Звонящий может гарантировать точных результатов. 
  
Существуют ограничения не может использоваться со свойствами дочерний объект, имеющие тип PT_OBJECT. 
  
Дополнительные сведения о структуре **SExistRestriction** [О ограничения](about-restrictions.md)см. 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

