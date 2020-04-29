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
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429567"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Эта структура используется с [хркреатеоффлинеобж](hrcreateofflineobj.md).
  
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

## <a name="members"></a>"Участники"

 **улсизе**
  
> Размер структуры.
    
 **улкреатефлагс**
  
> Значение должно быть равно 0.
    
 **пвсзпрофиленаме**
  
> Имя профиля.
    
 **улкапабилитиес**
  
> Битовая маска следующих флагов возможностей.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |Автономный объект способен переходить в автономный режим.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |Автономный объект способен работать в сети.  <br/> |
   
 **пгуид**
  
> Указатель на GUID, используемый для уникальной идентификации этого типа автономных объектов из других автономных объектов. GUID_GlobalState относится к глобальному автономному объекту, который объекты могут использовать в качестве родительского объекта.
    
 **пинстанце**
  
> Указатель на GUID, который уникально идентифицирует данный автономный объект. Он используется для определения неоднозначности автономных объектов из других объектов.
    
 **ппарент**
  
> Указатель на автономный объект, который является родительским для этого автономного объекта и изменения, которые наследуются этим автономным объектом.
    
 **пмаписуппорт**
  
>  Определяет объект поддержки MAPI, который будет использовать этот автономный объект. Например, если этот автономный объект используется для отслеживания состояния автономного и Интернет-хранилища, то это объект поддержки хранилищ. Однако если это автономный объект для объекта без объекта support, он может иметь значение NULL. 
    
 **паггрегатеинфо**
  
> Указатель на структуру MAPIOFFLINE_AGGREGATEINFO. Дополнительные сведения см. в разделе [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **пконнектинфо**
  
> Должно иметь значение null.
    
## <a name="see-also"></a>См. также



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

