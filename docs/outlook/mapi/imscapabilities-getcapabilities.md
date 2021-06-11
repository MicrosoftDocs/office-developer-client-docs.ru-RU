---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b76c55fd9ddc3aa7698f75aa6ce965544b2c9aae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409260"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает сведения о том, какую поддержку может поддерживать магазин на основе указанного селектора.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parameters

 *mscapSelector* 
  
> [in] Селектор, указывающий, какие возможности нужно возвращать.
    
## <a name="return-value"></a>Возвращаемое значение

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Поддержка домашних страницы папок в магазине по умолчанию. Это может быть возвращено, **если MSCAP_SEL_FOLDER** указан в  *mscapSelector*  . 
    
MSCAP_RES_ANNOTATION
  
> Если ограничение содержит какие-либо недопустимые аргументы, такие как недействительные свойства, магазин игнорирует недействительные аргументы и обрабатывает только допустимые аргументы. Это может быть возвращено, **если MSCAP_SEL_RESTRICTION** указан в  *mscapSelector*  . 
    
NULL
  
> Магазин не поддерживает возможности, основанные на заданном селекторе.
    

