---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408350"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Относится к**: Outlook 2013 | Outlook 2016 
  
Регистрирует файлы личных папок (PST) для автоматической разблокировки, избегая дальнейших вызовов hrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Параметры

_pmval_
  
> [in] Структура [SPropValue,](spropvalue.md) которая содержит указатель на путь к динамической библиотеке ссылок (DLL) для регистрации. Структура имеет следующие характеристики: 
    
   - A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Свойство значения MVSzW, задаваемого для массива строк символов Юникода, осекаемого нулью. Дополнительные сведения [см. в разделе SWStringArray.](swstringarray.md) 
    
> [!NOTE]
> SPropValue хранится в свойстве MAPI во внутреннем диапазоне PST. Это свойство недоступно для обычных приложений MAPI. 
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов функции был успешным.
    
## <a name="remarks"></a>Примечания

Сохраняемая регистрация может отрицательно сказаться на производительности приложений, таких как Outlook и windows Desktop Search, которые открывают PTS. Учитывайте влияние производительности при использовании или расширении использования сохраняемой регистрации.
  
> [!IMPORTANT]
> Этот метод реализован только для Юникод. Кроме того, он будет предварительно неудачным, если ни один из путей в массиве не имеет расширения DLL-файла. 
  
## <a name="see-also"></a>См. также

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

