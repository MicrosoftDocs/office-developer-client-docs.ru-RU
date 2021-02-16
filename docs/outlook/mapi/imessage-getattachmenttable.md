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
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421174"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу вложений сообщения.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которые связаны с созданием таблицы. Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Строки столбцов в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки столбцов имеют формат ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **getAttachmentTable** успешно возвращаться, возможно, до того, как таблица будет полностью доступна вызываемому клиенту. Если таблица недоступна, последующий вызов может привести к ошибке. 
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу вложений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица вложений успешно извлечена.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::GetAttachmentTable** возвращает указатель на таблицу вложений сообщения, которая содержит сведения обо всех вложениях в сообщении. Клиенты могут получить доступ к вложениям только через таблицу вложений. При искомом номере вложения его **PR_ATTACH_NUM** ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)клиент может использовать несколько методов **IMessage** для работы с вложением. 
  
Для каждого вложения существует одна строка. Полный список столбцов в таблице вложений см. в [таблицах вложений.](attachment-tables.md)
  
Вложение обычно не появляется в таблице вложений, пока вложение и сообщение не будут сохранены с помощью вызова [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Таблицы вложений являются динамическими. Если клиент создает новое вложение, удаляет существующее вложение или изменяет одно или несколько свойств после вызова **SaveChanges** для вложения в сообщении, таблица вложений будет обновлена для отражения новых сведений. 
  
Некоторые таблицы вложений поддерживают широкий спектр ограничений; другие этого не делают. Поддержка ограничений зависит от реализации поставщика store сообщений. 
  
При первом вложении таблицы вложений не обязательно сортироваться в определенном порядке. 
  
Установка флага MAPI_UNICODE в параметре  _ulFlags_ влияет на следующие вызовы таблицы вложений: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) для получения строк. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядка сортировки. 
    
Установка флага Юникода требует, чтобы сведения для всех строкных столбцов, возвращенных этими вызовами, были в формате Юникод. Однако, поскольку не все поставщики параметров хранения сообщений поддерживают Юникод, установка этого флага является только запросом.
  
## <a name="see-also"></a>См. также



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

