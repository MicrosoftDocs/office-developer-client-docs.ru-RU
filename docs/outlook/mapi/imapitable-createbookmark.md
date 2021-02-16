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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает закладку в текущем положении таблицы.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Параметры

 _lpbkPosition_
  
> [out] Указатель на возвращенное значение 32-битной закладки. Позже эту закладку можно передать в вызове метода [IMAPITable::SeekRow.](imapitable-seekrow.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Не удалось завершить запрашиваемую операцию.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::CreateBookmark** помечает позицию таблицы, создавая значение, называемое закладкой. Закладку можно использовать для возврата на позицию, которая определена закладкой. Положение с закладкой связано с объектом в этой строке таблицы. 
  
Закладки не поддерживаются в таблицах вложений, а реализации таблиц **вложений, возвращаемого с MAPI_E_NO_SUPPORT.** 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Из-за расходов на память, которые расходуется на поддержание позиций курсора с закладки, ограничивайте количество закладок, которые можно создать. Когда вы достигнете этого номера, MAPI_E_UNABLE_TO_COMPLETE всех последующих вызовов **CreateBookmark.**
  
Иногда закладка указывает на строку, которая больше не находится в представлении таблицы. Если звонячая использует такую закладку, переместите курсор к следующей видимой строке и остановите ее. 
  
Когда вызывающий пытается использовать закладку, указываую на незаметную строку, так как она была свернута, MAPI_W_POSITION_CHANGED после перемещения закладки. Закладку можно переместить к следующей видимой строке либо в это время, либо при схватке в **методе SetCollapseState.** Если закладка перемещается во время свернутой строки, необходимо сохранить в ней бит, который указывает точное время перемещения закладки: с момента последнего использования или если она никогда не использовалась с момента ее создания. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CreateBookmark** выделяет память для создаемой закладки. Освободите ресурсы для закладки, вызывая метод [IMAPITable::FreeBookmark.](imapitable-freebookmark.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

