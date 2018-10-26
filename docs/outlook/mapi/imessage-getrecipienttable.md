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
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579538"
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

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который управляет return таблицы. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetRecipientTable** для возврата успешно, возможно перед таблице доступными для клиента. Если в таблице не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
MAPI_UNICODE 
  
> Строковых столбцов должны быть в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы строки должен быть в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу получателей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> В таблице получателей успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMessage::GetRecipientTable** возвращает указатель на таблицу получателей сообщения, в которой содержатся сведения о всех получателей сообщения. Имеется одна строка для каждого получателя. 
  
Получателей таблицы имеют набор в зависимости от того, является ли сообщение отправлено различных столбцов. Полный список столбцов в таблице получателей [Получатель](recipient-tables.md)см.
  
Некоторые получателей таблицы поддерживает широкий спектр ограничения; некоторые — нет. Поддержка ограничений зависит от реализации поставщика хранилища сообщений. 
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на следующие вызовы получателей таблицы: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения строк. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядок сортировки. 
    
Настройка запросов флаг Юникод, сведения о любой строки столбцов, возвращаемых из них быть в формате Юникод. Тем не менее так как не все поставщики хранилища сообщений поддерживают Юникод, этот флаг установлен представляет собой запрос.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно изменить таблице получателей, когда он открыт путем вызова метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . **ModifyRecipients** добавляет получателей, удаляет получателей и изменение параметров учетной записи получателя. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

