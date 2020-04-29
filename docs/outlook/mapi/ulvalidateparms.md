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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию для проверки параметров клиентские приложения, которые передаются поставщикам услуг и MAPI. 
  
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

 _емесод_
  
> возврата Определяет, по перечислению, метод, который необходимо проверить. 
    
 _First_
  
> возврата Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Не удалось завершить операцию из — за ошибкой.
    
## <a name="remarks"></a>Примечания

Параметры, передаваемые между MAPI и поставщиками услуг, считаются верными и подвергнуты отладке только при проверке с помощью макроса [чеккпармс](checkparms.md) . Поставщики должны проверить все параметры, переданные клиентскими приложениями, но клиенты должны предполагать, что параметры MAPI и provider указаны правильно. Используйте макрос **HR_FAILED** для проверки возвращаемых значений. 
  
Макрос **улвалидатепармс** вызывается по-разному в зависимости от того, является ли вызывающий код C или C++. Этот макрос используется для проверки параметров для нескольких методов **IUnknown** и MAPI, возвращающих ulong, а не значений HRESULT; макрос [валидатепармс](validateparms.md) работает для всех остальных. 
  

