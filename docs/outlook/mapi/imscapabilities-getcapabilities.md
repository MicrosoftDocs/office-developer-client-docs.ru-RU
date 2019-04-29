---
title: Имскапабилитиесжеткапабилитиес
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает сведения о том, что хранилище может поддерживаться в соответствии с указанным селектором.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Параметры

 *mscapSelector* 
  
> возврата Селектор, указывающий, какие возможности следует возвращать.
    
## <a name="return-value"></a>Возвращаемое значение

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Поддержка домашних страниц папок в хранилище, не являющемся хранилищем по умолчанию. Это может быть возвращено, если **мскап_сел_фолдер** указан в *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Если ограничение содержит любые недопустимые аргументы, такие как недопустимые свойства, хранилище игнорирует недопустимые аргументы и обрабатывает только допустимые аргументы. Это может быть возвращено, если **мскап_сел_рестриктион** указан в *mscapSelector* . 
    
ОПРЕДЕЛЕН
  
> Хранилище не поддерживает никакие возможности на основе данного селектора.
    

