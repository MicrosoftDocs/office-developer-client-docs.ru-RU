---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415133"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает список регистраций для файла "Личные папки" (PST).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Parameters

 _ppmval_
  
> [in] Указатель на указатель на [структуру SPropValue.](spropvalue.md) Член ulPropTag этой структуры имеет тип PT_MV_UNICODE, а член значения MVszW будет массивом null-terminated строк Юникод. Эти строки являются путями к DLLs, для которых регистрация сохраняется. 
    
> [!NOTE]
> Поддержка PST для ANSI не реализована. 
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов функции был успешным.
    
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

