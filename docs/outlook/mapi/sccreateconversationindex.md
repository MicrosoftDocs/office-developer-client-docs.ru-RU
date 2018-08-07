---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 43765cddb2f06bfbe58e0a4000c7eadfdc5f3347
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812208"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Относится к**: Outlook 
  
Указывает, где принадлежит сообщение в поток сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>Параметры

 _cbParent_
  
> [in] Число байт в индексе родительского беседы.
    
 _lpbParent_
  
> [in] Указатель на байт в индексе родительского беседы. Это может быть NULL, если _cbParent_ равно нулю. 
    
 _lpcbIndex_
  
> [out] Указатель на число байт в новый индекс беседы, возвращаемого при вызове. 
    
 _lppbIndex_
  
> [out] Указатель на указатель на новый индекс беседы, возвращаемого при вызове.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    

