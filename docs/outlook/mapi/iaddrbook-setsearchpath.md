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
ms.openlocfilehash: 4f9d2f4d271e467d8fac32b8f17faa8f66cd3f99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808772"
---
# <a name="iaddrbooksetsearchpath"></a>IAddrBook::SetSearchPath

  
  
**Относится к**: Outlook 
  
Задает новый путь для поиска профиля, который используется для процесса разрешения имен. 
  
```cpp
HRESULT SetSearchPath(
  ULONG ulFlags,
  LPSRowSet lpSearchPath
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpSearchPath_
  
> [in] Указатель на структуру [SRowSet](srowset.md) , используемый для хранения путь поиска. Первое свойство для каждого элемента **aRow** в **SRowSet** должно быть **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Путь поиска успешно установлены.
    
MAPI_E_MISSING_REQUIRED_COLUMN 
  
> Один из контейнеров, описанного в структуре **SRowSet** не содержит свойство **PR_ENTRYID** . 
    
## <a name="remarks"></a>Замечания

Клиенты и поставщиков услуг вызовите метод **SetSearchPath** , чтобы сохранить изменения, внесенные в порядке поиска контейнер, используемый для разрешения имен с помощью метода [IAddrBook::ResolveName](iaddrbook-resolvename.md) . Путь поиска сохраняется между экземплярами сеанса. 
  
Клиенты и поставщики не нужно вызвать метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для вступления изменений в путь поиска было постоянным. 
  
## <a name="see-also"></a>См. также



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetPAB](iaddrbook-getpab.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[Каноническое свойство PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

