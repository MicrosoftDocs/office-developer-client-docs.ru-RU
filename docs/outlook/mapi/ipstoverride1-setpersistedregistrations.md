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
description: 'Дата последнего изменения: 08 ноября 2011 г.'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315479"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует файлы личных папок (PST) для автоматической разблокировки, избегая дальнейших вызовов к Хртрустедпстоверридехандлеркаллбакк.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Параметры

_пмвал_
  
> возврата Структура [спропвалуе](spropvalue.md) , содержащая указатель на путь к регистрируемой библиотеке динамической КОМПОНОВКИ (DLL). Структура имеет следующие характеристики: 
    
   - Улпроптаг [проп_таг](prop_tag.md)(ПТ_МВ_УНИКОДЕ, проп_ид_нулл).
    
   - Свойство Value Мвсзв, заданное для массива строк Юникода, заканчивающихся символами NULL. Дополнительные сведения см. в разделе [свстрингаррай](swstringarray.md) . 
    
> [!NOTE]
> Спропвалуе хранится в свойстве MAPI в внутреннем диапазоне PST-файла. Это свойство недоступно для обычных MAPI-приложений. 
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов функции выполнен успешно.
    
## <a name="remarks"></a>Замечания

Постоянные регистрации могут негативно повлиять на производительность приложений, таких как Outlook и панель поиска Windows, которые открывают PST. Учитывайте снижение производительности при использовании или развертывании постоянных регистраций.
  
> [!IMPORTANT]
> Этот метод реализован только для Юникода. Кроме того, она завершается аварийно, если любой из путей в массиве не имеет расширения имени файла. dll. 
  
## <a name="see-also"></a>См. также

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

