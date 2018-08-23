---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf100ed916080a91366062f45b9e3349516bdb98
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588519"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу вложения сообщения.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, влияющие на создание таблицы. Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Столбцы строку, в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetAttachmentTable** для возврата успешно, возможно перед таблице доступными для клиента. Если в таблице не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
 _lppTable_
  
> [out] Указатель на указатель на таблице вложений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице вложений был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Метод **IMessage::GetAttachmentTable** возвращает указатель на сообщение вложения таблицу, в которой содержатся сведения о всех вложений в сообщения. Клиенты могут получать доступ к вложения только с помощью таблицы вложений. Путем получения вложений номер его свойство **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) клиент может использовать несколько методов **IMessage** для работы с вложением. 
  
Имеется одна строка для каждого вложения. Полный список столбцов таблицы вложения [Вложения](attachment-tables.md)см.
  
Вложение обычно не отображается в таблице вложений до с помощью вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md)были сохранены как вложение и сообщение. Таблицы вложения являются динамическими. Если клиент создает новое вложение, удаляет существующие вложения или изменяет одного или нескольких свойств после **SaveChanges** вызовы, сделанные на вложения в сообщение, в таблице вложения будут обновлены в соответствии с новой информации. 
  
Некоторые таблицы вложений поддерживает широкий спектр ограничения; некоторые — нет. Поддержка ограничений зависит от реализации поставщика хранилища сообщений. 
  
При первом открытии таблицы вложение не сортируются обязательно в любом порядке. 
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на следующие вызовы к таблице вложений: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) для извлечения строк. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядок сортировки. 
    
Настройка запросов флаг Юникод, сведения о любой строки столбцов, возвращаемых из них быть в формате Юникод. Тем не менее так как не все поставщики хранилища сообщений поддерживают Юникод, этот флаг установлен представляет собой запрос.
  
## <a name="see-also"></a>См. также



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

