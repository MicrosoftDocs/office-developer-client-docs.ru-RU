---
title: Иолкенумжетнекст
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Получает следующую учетную запись в перечислителе.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321898"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Получает следующую учетную запись в перечислителе.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкенум](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Параметры

_ппунк_
  
> возврата Указатель на интерфейс **IUnknown** , который клиент может запрашивать для получения интерфейса [иолкаккаунт](iolkaccount.md) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|S_FALSE  <br/> |Достигнут конец перечислителя.  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс, указанный *ппунк* , наследуется от **IUnknown**. Клиент может запросить этот интерфейс (с помощью **IUnknown:: QueryInterface**), чтобы получить указатель на интерфейс **иолкаккаунт** , а также получить или задать сведения для этой учетной записи. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

