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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399657"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет кодовую страницу для потока Transport-Neutral Encapsulation формата TNEF ().
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |TNEF.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Параметры

 _lpStream_
  
> [in] Указатель на хранилище потока объекта OLE **IStream** интерфейс предоставление источника для потока сообщения в формате TNEF. 
    
 _lpulCodepage_
  
> [out] Указатель на страницу кода потока.
    
 _lpulSubCodepage_
  
> [out] Указатель на страницу subcode потока.
    
## <a name="return-value"></a>Возвращаемое значение

 **S_OK**
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Возникла ошибка при чтении атрибута в поток TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> Поток не поток TNEF либо произошла ошибка при чтении атрибута attOemCodepage.
    
## <a name="remarks"></a>Замечания

Используйте функцию **GetTnefStreamCodepage** для чтения атрибута **attOemCodepage** поток TNEF для определения кода страницы и страницы дополнительный код. Если **attOemCodepage** не найден, **GetTnefStreamCodepage** возвращает кодовую страницу 437 и страницы subcode 0. 
  
## <a name="see-also"></a>См. также



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

