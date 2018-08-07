---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809888"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Относится к**: Outlook 
  
Эта структура используется с [HrCreateOfflineObj](hrcreateofflineobj.md).
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> Размер структуры.
    
 **ulCreateFlags**
  
> Он должен иметь значение 0.
    
 **pwszProfileName**
  
> Имя профиля.
    
 **ulCapabilities**
  
> Битовая маска следующие флаги возможностей.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |Автономные объекта можно перейти в автономный режим.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |Автономные объект способен подключение.  <br/> |
   
 **pGUID**
  
> Указатель на идентификатор GUID, который используется для уникальной идентификации этого типа автономных объектов из других автономных объектов. GUID_GlobalState ссылается на глобальный объект автономной, объекты можно использовать в качестве родительского объекта.
    
 **pInstance**
  
> Указатель на идентификатор GUID, который уникальным образом определяет автономной объект. Он используется для однозначного определения этой автономной объектов из других объектов.
    
 **pParent**
  
> Указатель автономной объект, являющийся родительским объектом автономной, для которых будет наследовать этот объект автономные изменения.
    
 **pMAPISupport**
  
>  Определяет, что этот автономной объект, который будет использовать объект поддержки MAPI. К примеру при автономной объект используется для отслеживания в хранилище автономный режим и состояние online, то это магазины поддержки объекта. Тем не менее если это автономные объект для объекта с помощью объекта без поддержки затем она может быть NULL. 
    
 **pAggregateInfo**
  
> Указатель на структуру MAPIOFFLINE_AGGREGATEINFO. Для получения дополнительных сведений см [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Должен иметь значение null.
    
## <a name="see-also"></a>См. также



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

