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
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415658"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, к каков потоку сообщений относится сообщение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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
  
> [in] Количествобайтов в родительском индексе беседы.
    
 _lpbParent_
  
> [in] Указатель на bytes в родительском индексе беседы. Это может быть NULL,  _если cbParent_ — ноль. 
    
 _lpcbIndex_
  
> [out] Указатель на количествобайтов в новом индексе беседы, возвращаемом вызовом. 
    
 _lppbIndex_
  
> [out] Указатель на указатель на новый индекс беседы, возвращаемой вызовом.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    

