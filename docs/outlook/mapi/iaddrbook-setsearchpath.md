---
title: Иаддрбуксетсеарчпас
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает новый путь поиска в профиле, который используется для процесса разрешения имен. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпсеарчпас_
  
> возврата Указатель на структуру [SRowSet](srowset.md) , используемую для хранения пути поиска. Первое свойство для каждого элемента **аров** в **SRowSet** должно быть **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Путь поиска успешно задан.
    
МАПИ_Е_МИССИНГ_РЕКУИРЕД_КОЛУМН 
  
> Один из контейнеров, описанных в структуре **SRowSet** , не включал свойство **пр_ентрид** . 
    
## <a name="remarks"></a>Примечания

Клиенты и поставщики услуг вызывают метод **сетсеарчпас** , чтобы сохранить изменения, внесенные в контейнер поиска, который используется для разрешения имен с помощью метода [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) . Путь поиска сохраняется между экземплярами сеанса. 
  
Клиентам и поставщикам не нужно вызывать метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) , чтобы сделать изменения пути поиска постоянными. 
  
## <a name="see-also"></a>См. также



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

