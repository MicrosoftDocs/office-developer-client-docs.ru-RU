---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424611"
---
# <a name="imessagegetrecipienttable"></a>IMessage::GetRecipientTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу получателей сообщения.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет возвратом таблицы. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetRecipientTable** успешно возвращаться, возможно, до того, как таблица будет полностью доступна вызываемому клиенту. Если таблица недоступна, последующий вызов может привести к ошибке. 
    
MAPI_UNICODE 
  
> Строки столбцов должны быть в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки столбцов должны быть в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу получателей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица получателей возвращена успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::GetRecipientTable** возвращает указатель на таблицу получателей сообщения, которая включает сведения обо всех получателях сообщения. Для каждого получателя существует одна строка. 
  
Таблицы получателей имеют другой набор столбцов в зависимости от того, было ли сообщение отправлено. Полный список столбцов в таблице получателей см. в [таблицах получателей.](recipient-tables.md)
  
Некоторые таблицы получателей поддерживают широкий спектр ограничений; другие этого не делают. Поддержка ограничений зависит от реализации поставщика store сообщений. 
  
Установка флага MAPI_UNICODE в параметре  _ulFlags_ влияет на следующие вызовы таблицы получателей: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) для получения строк. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядка сортировки. 
    
Установка флага Юникода требует, чтобы сведения для всех строкных столбцов, возвращенных этими вызовами, были в формате Юникод. Однако, поскольку не все поставщики параметров хранения сообщений поддерживают Юникод, установка этого флага является только запросом.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете изменить таблицу получателей, когда она открыта, вызывая метод [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) **ModifyRecipients** добавляет получателей, удаляет получателей или изменяет свойства получателей. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

