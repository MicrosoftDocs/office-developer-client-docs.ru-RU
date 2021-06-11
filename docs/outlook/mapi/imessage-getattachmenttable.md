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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу вложений сообщения.
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Bitmask флагов, которые связаны с созданием таблицы. Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Столбцы строк находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, столбцы строк находятся в формате ANSI.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetAttachmentTable** успешно возвращаться, возможно, до того, как таблица будет полностью доступна для вызываемого клиента. Если таблица недоступна, последующий вызов может привести к ошибке. 
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу вложений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица вложений была успешно извлечена.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::GetAttachmentTable** возвращает указатель в таблицу вложений сообщения, которая включает сведения обо всех вложениях в сообщении. Клиенты могут получить доступ к вложениям только через таблицу вложений. С помощью свойства [PR_ATTACH_NUM (PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)клиент может использовать несколько методов **IMessage** для работы с вложением.  
  
Для каждого вложения имеется одна строка. Полный список столбцов в таблице вложений см. в [статье Таблицы вложений.](attachment-tables.md)
  
Обычно вложение не появляется в таблице вложений до тех пор, пока вложение и сообщение не будут сохранены с помощью вызова [в IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Таблицы вложений динамически. Если клиент создает новое вложение, удаляет существующее вложение или изменяет одно или несколько свойств после вызова **SaveChanges** на вложении в сообщении, таблица вложений будет обновлена для отражения новых сведений. 
  
Некоторые таблицы вложений поддерживают широкий спектр ограничений; другие этого не делают. Поддержка ограничений зависит от реализации поставщика магазина сообщений. 
  
При первоначальном вложении таблицы вложений не обязательно сортироваться в любом конкретном порядке. 
  
Настройка флага MAPI_UNICODE в параметре  _ulFlags_ влияет на следующие вызовы в таблицу вложений: 
  
- [IMAPITable::QueryColumns](imapitable-querycolumns.md) для получения набора столбцов. 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md) для получения строк. 
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) для получения порядка сортировки. 
    
Настройка флага Юникод требует, чтобы сведения для любых столбцов строк, возвращались из этих вызовов, были в формате Юникод. Однако, поскольку не все поставщики магазинов сообщений поддерживают Юникод, установка этого флага является только запросом.
  
## <a name="see-also"></a>См. также



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

