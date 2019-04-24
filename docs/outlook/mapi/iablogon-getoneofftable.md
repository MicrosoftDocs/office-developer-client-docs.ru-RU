---
title: Иаблогонжетонеоффтабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338411"
---
# <a name="iablogongetoneofftable"></a>IABLogon::GetOneOffTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает таблицу из одноразовых шаблонов для создания получателей, добавляемых в список получателей исходящего сообщения.
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип строковых столбцов, включенных в таблицу. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строковые столбцы представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строковые столбцы представлены в формате ANSI.
    
 _Лпптабле_
  
> вышли Указатель на указатель на одноразовую таблицу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица с одноразовым извлечением успешно получена.
    
МАПИ_Е_БАД_ЧАРВИДС 
  
> Установлен либо флаг МАПИ_УНИКОДЕ, либо поставщик адресных книг не поддерживает Юникод, или МАПИ_УНИКОДЕ не задан, а поставщик адресных книг поддерживает только Юникод.
    
МАПИ_Е_НО_СУППОРТ 
  
> Поставщик адресных книг не предоставляет одноразовых шаблонов.
    
## <a name="remarks"></a>Комментарии

MAPI вызывает метод **жетонеоффтабле** , чтобы сделать доступными одноразовые шаблоны для создания получателей. Новые получатели добавляются в список получателей исходящих сообщений. Поставщики адресных книг должны поддерживать уведомления из одноразовой таблицы для информирования MAPI об изменениях шаблонов. Для включения динамического обновления MAPI поддерживает односторонние таблицы Open. 
  
Поставщики адресных книг также могут поддерживать одноразовую таблицу для каждого из их контейнеров. Вызывающие объекты получают эту одноразовую таблицу, вызывая метод контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и запрашивает свойство **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Шаблоны, доступные в этой таблице, используются для добавления получателей в контейнер. Сведения о различиях между двумя типами одноразовых таблиц приведены в статье [Реализация одноразовЫх таблиц](implementing-one-off-tables.md).
  
Список обязательных столбцов в одноразовой таблице поставщика адресных книг представлен в разделе [одноразовЫе таблицы](one-off-tables.md).
  
## <a name="see-also"></a>См. также



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IAddrBook::NewEntry](iaddrbook-newentry.md)
  
[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

