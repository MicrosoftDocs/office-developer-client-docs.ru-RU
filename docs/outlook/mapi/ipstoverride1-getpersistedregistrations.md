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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315472"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает список регистраций для файла личных папок (PST).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Параметры

 _ппмвал_
  
> возврата Указатель на указатель на структуру [спропвалуе](spropvalue.md) . Элемент Улпроптаг данной структуры имеет тип ПТ_МВ_УНИКОДЕ, а элемент Мвсзв Value будет массивом строк Юникода с завершающим нулем. Эти строки представляют собой пути к DLL, для которых была сохранена регистрация. 
    
> [!NOTE]
> Поддержка PST для ANSI не реализована. 
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов функции выполнен успешно.
    
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

