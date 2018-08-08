---
title: FBadRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadRestriction
api_type:
- HeaderDef
ms.assetid: 6ad3638c-d088-4a89-9b0d-f5b672162203
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 43e0d8d28836b3114ab2029bc1f241197c569ffc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808417"
---
# <a name="fbadrestriction"></a>FBadRestriction

  
  
**Относится к**: Outlook 
  
Проверка ограничений, используются для ограничения представлении таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadRestriction(
  LPSRestriction lpres
);
```

## <a name="parameters"></a>Параметры

 _lpres_
  
> [in] Структура [SRestriction](srestriction.md) , определение ограничения для проверки. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Указанный ограничение, или одно или несколько его subrestrictions является недопустимым. 
    
FALSE 
  
> Указанный ограничение и все его subrestrictions являются допустимыми.
    
## <a name="remarks"></a>Замечания

После проверки ограничения может быть передан в вызовы метода [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице, определенные строки, метод [IMAPITable::FindRow](imapitable-findrow.md) , найдите строку в таблице и методы [IMAPIContainer](imapicontainerimapiprop.md) интерфейс для выполнения ограничения для объекта-контейнера. 
  

