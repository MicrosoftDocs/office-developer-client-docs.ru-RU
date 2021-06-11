---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Получает следующую учетную запись в переуметоре.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405991"
---
# <a name="iolkenumgetnext"></a>IOlkEnum::GetNext

Получает следующую учетную запись в переуметоре.
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkEnum](iolkenum.md).
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a>Parameters

_ppunk_
  
> [in] Указатель на **интерфейс IUnknown,** который клиент может запрашивать для получения [интерфейса IOlkAccount.](iolkaccount.md) 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|S_FALSE  <br/> |Переумывчик достиг конца.  <br/> |
   
## <a name="remarks"></a>Примечания

Интерфейс, указанный  *ppunk наследует* **от IUnknown**. Клиент может запрашивать этот интерфейс (с помощью **IUnknown::QueryInterface)** для получения указателя на **интерфейс IOlkAccount** и получения или набора сведений для этой учетной записи. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkEnum::GetCount](iolkenum-getcount.md)  
- [IOlkEnum::Reset](iolkenum-reset.md) 
- [IOlkEnum::Skip](iolkenum-skip.md)

