---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419613"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию проверки параметров, которые клиентские приложения передали поставщикам услуг и MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _eMethod_
  
> [in] Указывает путем переумерия метод проверки. 
    
 _First_
  
> [in] Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка не позволяет завершить операцию.
    
## <a name="remarks"></a>Примечания

Параметры, переданные между MAPI и поставщиками услуг, считаются правильными и проходят проверку только отладки с помощью макроса [CheckParms.](checkparms.md) Поставщики должны проверять все параметры, переданные в клиентских приложениях, но клиенты должны предполагать, что параметры MAPI и поставщика являются правильными. Используйте **макрос HR_FAILED** для проверки значений возврата. 
  
Макрос **UlValidateParms** вызывается по-разному в зависимости от того, является ли код вызова C или C++. Этот макрос используется для проверки параметров для нескольких методов **IUnknown** и MAPI, которые возвращают ULONG вместо значений HRESULT; Макрос [ValidateParms](validateparms.md) работает для всех остальных. 
  

