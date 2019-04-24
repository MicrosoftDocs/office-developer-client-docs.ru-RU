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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357129"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Members

 **Улсизе**
  
> Размер структуры.
    
 **Улкреатефлагс**
  
> Значение должно быть равно 0.
    
 **Пвсзпрофиленаме**
  
> Имя профиля.
    
 **Улкапабилитиес**
  
> Битовая маска следующих флагов возможностей.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |Автономный объект способен переходить в автономный режим.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |Автономный объект способен работать в сети.  <br/> |
   
 **Пгуид**
  
> Указатель на GUID, используемый для уникальной идентификации этого типа автономных объектов из других автономных объектов. Гуид_глобалстате ссылается на глобальный автономный объект, который объекты могут использовать в качестве родительского объекта.
    
 **Пинстанце**
  
> Указатель на GUID, который уникально идентифицирует данный автономный объект. Он используется для определения неоднозначности автономных объектов из других объектов.
    
 **Ппарент**
  
> Указатель на автономный объект, который является родительским для этого автономного объекта и изменения, которые наследуются этим автономным объектом.
    
 **Пмаписуппорт**
  
>  Определяет объект поддержки MAPI, который будет использовать этот автономный объект. Например, если этот автономный объект используется для отслеживания состояния автономного и Интернет-хранилища, то это объект поддержки хранилищ. Однако если это автономный объект для объекта без объекта support, он может иметь значение NULL. 
    
 **Паггрегатеинфо**
  
> Указатель на структуру МАПИОФФЛИНЕ_АГГРЕГАТЕИНФО. Дополнительные сведения см. в разделе [мапиоффлине_аггрегатеинфо](mapioffline_aggregateinfo.md).
    
 **Пконнектинфо**
  
> Должно иметь значение null.
    
## <a name="see-also"></a>См. также



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

