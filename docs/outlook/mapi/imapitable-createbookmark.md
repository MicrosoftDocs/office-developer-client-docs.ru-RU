---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408826"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает закладки в текущем положении таблицы.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parameters

 _lpbkPosition_
  
> [вышел] Указатель на возвращенное 32-битное значение закладки. Эта закладки позже может быть передана в вызове к [методу IMAPITable::SeekRow.](imapitable-seekrow.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Не удалось завершить запрашиваемую операцию.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::CreateBookmark** отмечает положение таблицы путем создания значения, называемого закладкой. Закладки можно использовать для возвращения в позицию, определенную закладкой. Закладки связаны с объектом в этой строке в таблице. 
  
Закладки не поддерживаются на таблицах вложений, а реализация таблицы вложений **в createBookmark** возвращает MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Из-за расходов памяти на поддержание позиций курсоров с помощью закладок ограничивайте количество закладки, которые можно создать. Когда вы достигнете этого номера, MAPI_E_UNABLE_TO_COMPLETE все последующие вызовы **в CreateBookmark**.
  
Иногда закладки указывает на строку, которая больше не находится в представлении таблицы. Если вызыватель использует такую закладки, переместите курсор в следующую видимую строку и остановитесь на этом. 
  
Когда вызывающий пытается использовать закладки, указывающие на незаметную строку, так как она была свернута, MAPI_W_POSITION_CHANGED после перемещения закладки. Закладки можно переместить в следующую видимую строку либо в это время, либо при коллапсе метода **SetCollapseState.** При перемещении закладки при обрушении строки необходимо сохранить в закладке немного, что указывает точно, когда закладки были перемещены: с момента ее последнего использования или если она никогда не использовалась с момента ее создания. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CreateBookmark** выделяет память для создаваемой закладки. Освободите ресурсы для закладки, назвав [метод IMAPITable::FreeBookmark.](imapitable-freebookmark.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

