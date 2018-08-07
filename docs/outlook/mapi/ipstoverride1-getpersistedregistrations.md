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
ms.openlocfilehash: 56aaf5caf93f90f54d152ab3684ca592cd45cd1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809540"
---
# <a name="ipstoverride1getpersistedregistrations"></a>IPSTOVERRIDE1::GetPersistedRegistrations

  
  
**Относится к**: Outlook 
  
Получение списка регистраций для файл личных папок (PST).
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a>Параметры

 _ppmval_
  
> [in] Указатель на указатель на структуру [SPropValue](spropvalue.md) . Элемент ulPropTag эта структура является типа PT_MV_UNICODE и член значение MVszW будет массив строк Юникод, завершающуюся символом null. Эти строки, путей к библиотеки DLL, для которых были сохранены регистрации. 
    
> [!NOTE]
> Поддержка .pst ANSI не реализован. 
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов функции прошла успешно.
    
## <a name="see-also"></a>См. также



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)
  
[IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

