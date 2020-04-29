---
title: имессажежетреЦипиенттабле
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
  
> возврата Битовая маска флагов, которые управляют возвратом таблицы. Можно задать следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Разрешает успешное возвращение **жетреЦипиенттабле** , возможно, перед тем, как таблица будет полностью доступна вызывающему клиенту. Если таблица недоступна, то выполнение последующих вызовов может привести к ошибке. 
    
MAPI_UNICODE 
  
> Строковые столбцы должны быть в формате Юникод. Если флаг MAPI_UNICODE не установлен, строковые столбцы должны быть в формате ANSI.
    
 _лпптабле_
  
> вышли Указатель на указатель на таблицу получателей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица получателей возвращена успешно.
    
## <a name="remarks"></a>Примечания

Метод **iMessage:: жетреЦипиенттабле** возвращает указатель на таблицу получателей сообщения, включающий сведения обо всех получателях сообщения. Для каждого получателя существует одна строка. 
  
Таблицы получателей имеют разный набор столбцов в зависимости от того, было ли отправлено сообщение. Полный список столбцов в таблице получателей приведен в разделе [таблицы получателей](recipient-tables.md).
  
Некоторые таблицы получателей поддерживают широкий спектр ограничений; другие пользователи не могут. Поддержка ограничений зависит от реализации поставщика хранилища сообщений. 
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на следующие вызовы таблицы получателей: 
  
- [IMAPITable:: куериколумнс](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable:: QueryRows](imapitable-queryrows.md) для получения строк. 
    
- [IMAPITable:: куерисортордер](imapitable-querysortorder.md) для получения порядка сортировки. 
    
Установка флага Юникода требует, чтобы сведения о строковых столбцах, возвращаемых из этих вызовов, были в формате Юникод. Однако так как не все поставщики хранилищ сообщений поддерживают Юникод, установка этого флага является только запросом.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете изменить таблицу получателей, когда она открыта, вызвав метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) . **МодифиреЦипиентс** добавляет получателей, удаляет получателей или изменяет свойства получателей. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

