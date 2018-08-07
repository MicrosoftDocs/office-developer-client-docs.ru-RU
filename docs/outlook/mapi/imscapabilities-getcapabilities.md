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
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809363"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Относится к**: Outlook 
  
Возвращает сведения о хранилище, которое может поддерживать на основании указанного "Выбор".
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Параметры

 *mscapSelector* 
  
> [in] Выбор, определяющее, какие возможности для возврата.
    
## <a name="return-value"></a>������������ ��������

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Поддержка для домашних страниц папок в хранилище не по умолчанию. Можно получить, если указано **MSCAP_SEL_FOLDER** в *mscapSelector* . 
    
MSCAP_RES_ANNOTATION
  
> Если ограничение содержит все недопустимые аргументы, таких как недопустимые свойства, хранилище игнорирует недопустимых аргументов и обрабатывает только допустимые аргументы. Можно получить, если указано **MSCAP_SEL_RESTRICTION** в *mscapSelector* . 
    
NULL
  
> Хранилище не поддерживает все возможности на основании указанного "Выбор".
    

