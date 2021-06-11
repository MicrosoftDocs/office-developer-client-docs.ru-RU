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
ms.openlocfilehash: f8c129e772870804ef464765b2035a3582317a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412984"
---
# <a name="iaddrbookgetsearchpath"></a>IAddrBook::GetSearchPath

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает упорядоченный список идентификаторов входных контейнеров, которые будут включены в процесс разрешения имен, инициированный методом [IAddrBook::ResolveName.](iaddrbook-resolvename.md) 
  
```cpp
HRESULT GetSearchPath(
  ULONG ulFlags,
  LPSRowSet FAR * lppSearchPath
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип строк, возвращаемых в пути поиска. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Возвращенные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _lppSearchPath_
  
> [вышел] Указатель на указатель на упорядоченный список идентификаторов записи контейнера. **GetSearchPath** сохраняет упорядоченный список в [структуре SRowSet.](srowset.md) Если в иерархии адресных книг нет контейнеров, в структуре **SRowSet** возвращается ноль. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Путь поиска был успешно извлечен.
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят по **методу GetSearchPath,** чтобы получить путь поиска, используемый для решения имен с помощью **метода ResolveName.** Как правило, клиенты звонят по методу [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) для создания пути поиска контейнеров в профиле, прежде чем вызывать **GetSearchPath** для его получения. Однако вызов **SetSearchPath** необязателен. 
  
Если **SetSearchPath** никогда не назывался, **GetSearchPath** создает путь, проработав таблицы иерархии адресной книги. Путь поиска по умолчанию, установленный **GetSearchPath,** состоит из следующих контейнеров в следующем порядке: 
  
1. Первый контейнер с разрешением на чтение и написание, как правило, личный адрес (PAB).
    
2. Каждый контейнер с **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)имеет свойство DT_GLOBAL. Этот параметр указывает, что контейнер содержит получателей. 
    
3. Контейнер, назначенный по умолчанию, если в свойстве PR_DISPLAY_TYPE установлен флаг DT_GLOBAL, а контейнер по умолчанию отличается от первого контейнера разрешением на чтение и записи.  
    
Если **setSearchPath** был вызван, **GetSearchPath** создает путь с помощью контейнеров адресной книги, хранимых в профиле. **GetSearchPath** проверяет этот путь, прежде чем он возвращает его вызываемой. 
  
После первого вызова **в SetSearchPath** необходимо использовать последующие вызовы **в SetSearchPath** для изменения пути поиска, возвращенного **GetSearchPath.** Другими словами, клиент или поставщик вызовов не получает путь поиска по умолчанию после первого вызова **в SetSearchPath.**
  
## <a name="see-also"></a>См. также



[IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

