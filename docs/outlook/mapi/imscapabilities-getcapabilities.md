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
ms.openlocfilehash: 0211a326e94c5847c040040e0e0e4e9ddd1d760d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583276"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
    

