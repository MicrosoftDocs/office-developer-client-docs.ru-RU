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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает сведения о том, что может поддерживать хранилище на основе указанного селектора.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Параметры

 *mscapSelector* 
  
> [in] Селектор, указывающий возвращаемую возможность.
    
## <a name="return-value"></a>Возвращаемое значение

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Поддержка домашних папок в нестандартном хранилище. Это может быть возвращено, **если MSCAP_SEL_FOLDER** указан в  *mscapSelector*  . 
    
MSCAP_RES_ANNOTATION
  
> Если ограничение содержит недопустимые аргументы, например недопустимые свойства, хранилище игнорирует недопустимые аргументы и обрабатывает только допустимые аргументы. Это может быть возвращено, **если MSCAP_SEL_RESTRICTION** указан в  *mscapSelector*  . 
    
NULL
  
> Хранилище не поддерживает какие-либо возможности на основе заданного селектора.
    

