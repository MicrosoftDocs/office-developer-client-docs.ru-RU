---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299435"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет кодовую страницу для потока Transport-Neutral формата инкапсуляции (TNEF).
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |tnef.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Параметры

 _lpStream_
  
> [in] Указатель на объект потока хранилища OLE **IStream,** предоставляющий источник для сообщения потока TNEF. 
    
 _lpulCodepage_
  
> [out] Указатель на кодовую страницу потока.
    
 _lpulSubCodepage_
  
> [out] Указатель на страницу подкода потока.
    
## <a name="return-value"></a>Возвращаемое значение

 **S_OK**
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Произошла ошибка при чтении атрибута в потоке TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> Либо поток не был потоком TNEF, либо произошла ошибка считывания атрибута attOemCodepage.
    
## <a name="remarks"></a>Примечания

Используйте **функцию GetTnefStreamCodepage** для чтения атрибута **attOemCodepage** потока TNEF, чтобы определить кодовую страницу и страницу в коде. Если **attOemCodepage** не найден, **GetTnefStreamCodepage** возвращает кодовую страницу 437 и страницу подкода 0. 
  
## <a name="see-also"></a>См. также



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

