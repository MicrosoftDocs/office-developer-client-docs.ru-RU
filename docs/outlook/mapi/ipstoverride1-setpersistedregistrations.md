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
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408350"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует файлы личных папок (PST) для автоматической разблокировки, избегая дополнительных вызовов в HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Parameters

_pmval_
  
> [in] Структура [SPropValue,](spropvalue.md) содержающая указатель пути для регистрации библиотеки динамических ссылок (DLL). Структура имеет следующие характеристики: 
    
   - A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Свойство значения MVszW, задаваемого массиву null-terminated строк символов Юникод. Дополнительные сведения см. в [разделе SWStringArray.](swstringarray.md) 
    
> [!NOTE]
> SPropValue хранится в свойстве MAPI во внутреннем диапазоне PST. Это свойство недоступно для обычных приложений MAPI. 
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов функции был успешным.
    
## <a name="remarks"></a>Примечания

Сохраняемая регистрация может отрицательно повлиять на производительность приложений, таких как Outlook и Windows настольный поиск, которые открывают PSTs. Рассмотрите эффект производительности при использовании или расширении использования сохраняющихся регистраций.
  
> [!IMPORTANT]
> Этот метод реализуется только для Unicode. Кроме того, он будет предосудительно сбой, если любой из путей в массиве не имеет расширения имени файла .dll. 
  
## <a name="see-also"></a>См. также

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

