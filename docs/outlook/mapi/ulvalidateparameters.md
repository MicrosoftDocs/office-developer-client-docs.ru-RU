---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315290"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает внутреннюю функцию для проверки параметров клиентские приложения, которые передаются поставщикам услуг и MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Параметры

 _Емесод_
  
> возврата Определяет, по перечислению, метод, который необходимо проверить. 
    
 _First_
  
> возврата Указатель на первый аргумент в стеке.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
МАПИ_Е_КАЛЛ_ФАИЛЕД 
  
> Не удалось завершить операцию из — из — из — из — из — из — из неизвестного источника.
    
## <a name="remarks"></a>Замечания

Макрос **улвалидатепараметерс** был заменен макросом [улвалидатепармс](ulvalidateparms.md) . **Улвалидатепараметерс** работает неправильно на платформах RISC и теперь не может компилироваться. Он по-прежнему компилирует и работает правильно на платформах Intel, но **улвалидатепармс** рекомендуется на всех платформах. 
  

