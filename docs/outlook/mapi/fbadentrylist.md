---
title: FBadEntryList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadEntryList
api_type:
- HeaderDef
ms.assetid: 270c47c3-ae68-4995-b304-27f861b350d6
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: aae2e97b987414fc5e46b410465d3232b61f1ffe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808406"
---
# <a name="fbadentrylist"></a>FBadEntryList

  
  
**Применимо к**: Outlook 
  
Проверяет список идентификаторов запись MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadEntryList(
  LPENTRYLIST lpEntryList
);
```

## <a name="parameters"></a>Parameters

 _lpEntryList_
  
> [in] Указатель на структуру [ENTRYLIST](entrylist.md) , который содержит массив идентификаторов запись для проверки. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Один или несколько идентификаторов указанного элемента являются недопустимыми. 
    
FALSE 
  
> Все идентификаторы перечисленных записи являются допустимыми.
    
## <a name="remarks"></a>Замечания

Функция **FBadEntryList** определяет, если список идентификаторов запись был создан неправильно. Пример недопустимый идентификатор — один для неправильно выделенной памяти или идентификатор неправильный размер. 
  

