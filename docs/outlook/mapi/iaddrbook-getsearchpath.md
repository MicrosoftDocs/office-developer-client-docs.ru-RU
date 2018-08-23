---
title: IAddrBookGetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetSearchPath
api_type:
- COM
ms.assetid: 43b51a66-71fa-4e10-93e4-d533b48af4de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7bf69e560142ab282d6545389e02766389e4d018
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580700"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает упорядоченный список идентификаторов запись контейнеров, которые будут включены в процесс разрешения имен, которые запускаются с помощью метода [IAddrBook::ResolveName](iaddrbook-resolvename.md) . 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип строк, возвращаемых в путь поиска. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> В формате Юникод, возвращенных строк. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _lppSearchPath_
  
> [out] Указатель на указатель упорядоченный список идентификаторов запись контейнера. **GetSearchPath** сохранение упорядоченный список в структуре [SRowSet](srowset.md) . Если в иерархии адресной книги не контейнеров, возвращается ноль в структуре **SRowSet** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Путь поиска был успешно извлечен.
    
## <a name="remarks"></a>Замечания

Клиенты и поставщики услуг вызовите метод **GetSearchPath** для получения пути поиска, который используется для разрешения имен с помощью метода **ResolveName** . Как правило клиенты вызовите метод [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) для установления путь поиска контейнера в профиле перед звонят **GetSearchPath** для его извлечения. Тем не менее вызов **SetSearchPath** не является обязательным. 
  
Если **SetSearchPath** никогда не был вызван, **GetSearchPath** строится путь с выполнением адрес таблиц иерархии книги. Путь поиска по умолчанию, установленные **GetSearchPath** состоит из следующих контейнеров в следующем порядке: 
  
1. Первый контейнер, получившие разрешение на чтение и запись, обычно Личная адресная книга (адресной книги).
    
2. Каждый контейнер, задайте значение DT_GLOBAL свойства **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)). Этот параметр указывает, что в контейнере получателей. 
    
3. Контейнер, назначенный по умолчанию, если нет контейнеров, имеющие флаг DT_GLOBAL в их свойство **PR_DISPLAY_TYPE** и контейнер по умолчанию отличается от первого контейнера получившие разрешение на чтение и запись. 
    
При вызове **SetSearchPath** **GetSearchPath** создает путь с помощью контейнеров адресной книги, сохраненные в профиле. **GetSearchPath** проверяет этот путь до его возврата вызывающего абонента. 
  
После первого вызова **SetSearchPath**последующие вызовы **SetSearchPath** должен использоваться для изменения пути поиска, возвращаемые **GetSearchPath**. Другими словами вызывающей клиента или поставщика не получает путь поиска по умолчанию после первого вызова **SetSearchPath**.
  
## <a name="see-also"></a>См. также



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

