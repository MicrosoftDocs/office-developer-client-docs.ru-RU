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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу разных шаблонов для создания получателей, которые будут добавлены в список получателей исходятго сообщения.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип столбцов строк, включенных в таблицу. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строк находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, столбцы строк находятся в формате ANSI.
    
 _lppTable_
  
> [вышел] Указатель на указатель на разовую таблицу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Разовая таблица была успешно извлечена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а поставщик адресной книги не поддерживает Unicode, либо MAPI_UNICODE не был установлен, а поставщик адресной книги поддерживает только Unicode.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресных книг не поставляет одновековые шаблоны.
    
## <a name="remarks"></a>Примечания

MAPI вызывает **метод GetOneOffTable,** чтобы сделать доступными однофазные шаблоны для создания получателей. Новые получатели добавляются в список получателей исходя из сообщения. Поставщики адресных книг должны поддерживать уведомление на своей разовой таблице, чтобы сообщить MAPI об изменениях шаблона. MAPI сохраняет разовую таблицу открытой, чтобы включить динамическое обновление. 
  
Поставщики адресных книг также могут поддерживать разовую таблицу для каждого из контейнеров. Звонители извлекают эту разовую таблицу, вызывая метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **запрашивая** свойство [PR_CREATE_TEMPLATES (PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md) Шаблоны, доступные в этой таблице, используются для добавления получателей в контейнер. О различиях между двумя типами разовых таблиц см. в таблице [Implementing One-Off Tables.](implementing-one-off-tables.md)
  
Список необходимых столбцов в разовой таблице поставщика адресной книги см. в статье [One-Off Tables.](one-off-tables.md)
  
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

