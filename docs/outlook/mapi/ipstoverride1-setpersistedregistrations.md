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
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809564"
---
# <a name="ipstoverride1setpersistedregistrations"></a>IPSTOVERRIDE1::SetPersistedRegistrations

**Относится к**: Outlook 
  
Регистрирует файлы личных папок (PST) для автоматического разблокирование Предотвращение дальнейшие вызовы HrTrustedPSTOverrideHandlerCallback.
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a>Параметры

_pmval_
  
> [in] Структура [SPropValue](spropvalue.md) , содержащая указатель на путь библиотеки динамической компоновки (DLL) для регистрации. Структура имеет следующие характеристики: 
    
   - UlPropTag [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).
    
   - Свойство value MVszW, заданный в массив строк символ Unicode символом null. Дополнительные сведения см в разделе [SWStringArray](swstringarray.md) . 
    
> [!NOTE]
> SPropValue хранится в свойстве MAPI в диапазоне внутренних PST-файлов. Это свойство недоступно для обычных приложений MAPI. 
  
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов функции прошла успешно.
    
## <a name="remarks"></a>Замечания

Постоянные регистраций может отрицательно сказаться на производительности приложения, такие как Outlook и Windows Desktop Search, откройте PST-файлов. Рассмотрите возможность влияют на производительность при использовании или расширении использования постоянных регистрации.
  
> [!IMPORTANT]
> Этот метод реализован только для кодировки Юникод. Более того он будет заблаговременно ошибкой, если какие-либо из следующих путей в массиве имеет расширение имени файла из библиотеки DLL. 
  
## <a name="see-also"></a>См. также

- [IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md) 
- [IPSTOVERRIDEREQ : IUnknown](ipstoverridereqiunknown.md)

