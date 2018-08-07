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
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808722"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Относится к**: Outlook 
  
Возвращает таблицу одноразовых шаблоны для создания получателей для добавления в список получателей исходящих сообщений.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип string столбцов, указанных в таблице. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строку, в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на одноразовых таблицы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице одноразовых был успешно извлечен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и поставщик адресной книги не поддерживает Юникод, или MAPI_UNICODE не было установлено и поддерживает только Юникод в адресной книге.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик адресной книги не предоставляет никаких одноразовых шаблонов.
    
## <a name="remarks"></a>Замечания

MAPI вызывает метод **GetOneOffTable** , чтобы сделать доступных одноразовых шаблонов для создания получателей. Новые получатели добавляются в список получателей исходящих сообщений. Поставщиками адресных книг должны поддерживать уведомлений на их одноразовых таблицу, чтобы информировать MAPI изменения шаблона. MAPI отслеживает одноразовых таблицы, открыть, чтобы включить динамическое обновление. 
  
Поставщиками адресной книги также могут поддерживать одноразовых таблице для каждого из их контейнеров. Вызывающие извлечение одноразовых таблице путем вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера и разрешения на запрос свойства **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Шаблоны, доступные через этой таблице используются для добавления получателей в контейнере. Обсуждение различия между двумя типами одноразовых таблиц [Реализация одноразовых таблиц](implementing-one-off-tables.md)см.
  
Список обязательные столбцы в таблице одноразовых поставщика адресных книг см в [Одноразовых таблиц](one-off-tables.md).
  
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

