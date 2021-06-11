---
title: IAddrBookSetSearchPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetSearchPath
api_type:
- COM
ms.assetid: fbff82de-77d3-411e-a30c-a37cefdd92fc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8611249207811446ae47f056486ec498bf1e7eab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426207"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает новый путь поиска в профиле, который используется для процесса разрешения имен. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpSearchPath_
  
> [in] Указатель на структуру [SRowSet,](srowset.md) используемую для удержания пути поиска. Первое свойство для каждого **участника aRow**  в **SRowSet** должно быть PR_ENTRYID [(PidTagEntryId).](pidtagentryid-canonical-property.md)
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Путь поиска был успешно за установлен.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> В одном из контейнеров, описанных в **структуре SRowSet,** не было PR_ENTRYID **свойства.** 
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг звонят по методу **SetSearchPath,** чтобы сохранить изменения, внесенные в порядок поиска контейнера, который используется для решения имен с помощью [метода IAddrBook::ResolveName.](iaddrbook-resolvename.md) Путь поиска сохранен между экземплярами сеанса. 
  
Чтобы изменить путь поиска, клиентам и поставщикам не нужно вызывать метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
## <a name="see-also"></a>См. также



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

