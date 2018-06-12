---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Получает перечислитель следующего учетной записи.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807884"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Получает перечислитель следующего учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parameters

_ppunk_
  
> [in] Указатель на интерфейс **IUnknown** , клиента запроса можно получить интерфейс [IOlkAccount](iolkaccount.md) . 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|S_FALSE  <br/> |Перечислитель достигнут конец.  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс, указанный *ppunk* наследует от **IUnknown**. Клиент запроса этот интерфейс (с помощью **IUnknown::QueryInterface**) можно получить указатель на интерфейс **IOlkAccount** и получить или задать сведения для этой учетной записи. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

