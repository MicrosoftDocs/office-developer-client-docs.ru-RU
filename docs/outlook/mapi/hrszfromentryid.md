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
ms.openlocfilehash: 366208b8288aeb61bf1bb78f2c9f10b400a3dc26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567596"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Кодирует идентификатор запись в строку ASCII. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Параметры

 _cb_
  
> [in] Размер, в байтах, идентификатор записи, на который указывает параметр _pentry_ . 
    
 _pentry_
  
> [in] Указатель на структуру [ENTRYID](entryid.md) , содержащее идентификатор записи для кодирования. 
    
 _psz_
  
> [out] Указатель на Возвращенная строка ASCII.
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Функции [HrEntryIDFromSz](hrentryidfromsz.md) и **HrSzFromEntryID** преобразование между строки и двоичного формата идентификаторы записей. С помощью интерфейса MAPI следует использовать структуры с двоичных данных. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrSzFromEntryID** выделение памяти для строки ASCII, с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

