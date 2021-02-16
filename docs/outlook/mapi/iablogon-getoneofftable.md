---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411878"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу разных шаблонов для создания получателей, добавляемой в список получателей исходяного сообщения.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом строки столбцов, включенных в таблицу. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки столбцов в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки столбцов имеют формат ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на одностолевую таблицу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Односеаленная таблица была успешно извлечена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а поставщик адресной книги не поддерживает Юникод, либо MAPI_UNICODE не установлен, а поставщик адресной книги поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не дает никаких одновключных шаблонов.
    
## <a name="remarks"></a>Примечания

MAPI вызывает **метод GetOneOffTable,** чтобы сделать доступными однофазные шаблоны для создания получателей. Новые получатели добавляются в список получателей исходяющих сообщений. Поставщики адресных книг должны поддерживать уведомления в своей однобайтовой таблице, чтобы сообщить MAPI об изменениях шаблона. MAPI сохраняет разовую таблицу открытой для динамического обновления. 
  
Поставщики адресных книг также могут поддерживать одну таблицу для каждого из своих контейнеров. Звоняющие извлекают эту разную таблицу, вызывая метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера и запрашивая свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md) Шаблоны, доступные в этой таблице, используются для добавления получателей в контейнер. О различиях между двумя типами разовых таблиц см. в One-Off [Таблицы.](implementing-one-off-tables.md)
  
Список необходимых столбцов в одностолбной таблице поставщика адресной книги см. в [статье "Таблицы с одним исключением".](one-off-tables.md)
  
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

