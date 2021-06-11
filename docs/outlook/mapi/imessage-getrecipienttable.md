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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу получателей сообщения.
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Bitmask флагов, которые контролируют возвращение таблицы. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetRecipientTable** успешно возвращаться, возможно, до того, как таблица будет полностью доступна для вызываемого клиента. Если таблица недоступна, последующий вызов может привести к ошибке. 
    
MAPI_UNICODE 
  
> Столбцы строки должны быть в формате Unicode. Если флаг MAPI_UNICODE не установлен, столбцы строки должны быть в формате ANSI.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу получателей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица получателей была возвращена успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::GetRecipientTable** возвращает указатель в таблицу получателей сообщения, которая включает сведения обо всех получателях сообщения. Для каждого получателя имеется одна строка. 
  
Таблицы получателей имеют другой набор столбцов в зависимости от того, было ли отправлено сообщение. Полный список столбцов в таблице получателей см. в статье [Таблицы получателей.](recipient-tables.md)
  
Некоторые таблицы получателей поддерживают широкий спектр ограничений; другие этого не делают. Поддержка ограничений зависит от реализации поставщика магазина сообщений. 
  
Установка флага MAPI_UNICODE в  _параметре ulFlags_ влияет на следующие вызовы в таблицу получателей: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) для получения строк. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядка сортировки. 
    
Настройка флага Юникод требует, чтобы сведения для любых столбцов строк, возвращались из этих вызовов, были в формате Юникод. Однако, поскольку не все поставщики магазинов сообщений поддерживают Юникод, установка этого флага является только запросом.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете изменить таблицу получателей, пока она открыта, позвонив [методу IMessage::ModifyRecipients.](imessage-modifyrecipients.md) **ModifyRecipients** добавляет получателей, удаляет получателей или изменяет свойства получателей. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

