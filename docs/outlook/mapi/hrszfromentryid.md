---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411556"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Кодирует идентификатор записи в строку ASCII. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Параметры

 _cb_
  
> возврата Размер (в байтах) идентификатора записи, на который указывает параметр _пентри_ . 
    
 _пентри_
  
> возврата Указатель на структуру [EntryID](entryid.md) , содержащую идентификатор записи, который необходимо закодировать. 
    
 _ПСЗ_
  
> вышли Указатель на возвращаемую строку ASCII.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Функции [хрентридфромсз](hrentryidfromsz.md) и **хрсзфроментрид** обеспечивают преобразование между строковым и двоичным форматами идентификаторов записей. С помощью MAPI следует использовать структуры с двоичными данными. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **хрсзфроментрид** выделяет память для строки ASCII с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) . 
  

