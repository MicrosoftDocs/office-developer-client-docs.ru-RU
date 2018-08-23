---
title: Обработка ошибок с помощью макросов
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567127"
---
# <a name="using-macros-for-error-handling"></a>Обработка ошибок с помощью макросов

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Существует несколько макросов для облегчения работы со значениями HRESULT.
  
Существует два набора макросы, которые проверки успех или сбой: HR_SUCCEEDED и HR_FAILED и SUCCEEDED и FAILED. SUCCEEDED — то же, что HR_SUCCEEDED и FAILED совпадает с HR_FAILED.
  
В этом случае используйте макрос **ResultFromScode** для задания переменной HRESULT соответствующее значение HRESULT для значение S_OK. 
  
В следующей таблице кратко описаны часто используемые макросы.
  
|**Макрос**|**Описание**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Создает HRESULT из ее компонентов.  <br/> |
|**HR_SUCCEEDED** <br/> |Проверяет HRESULT для успеха или предупреждения.  <br/> |
|**HR_FAILED** <br/> |Тесты со знаком для HRESULT ошибки.  <br/> |
|**HRESULT_CODE** <br/> |Извлекает часть кода ошибки HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Извлекает средство из HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Извлекает из СТЕПЕНИ разрядная уровень серьезности.  <br/> |
|**ВЫПОЛНЕНО УСПЕШНО** <br/> |Проверяет HRESULT для успеха или предупреждения.  <br/> |
|**НЕ УДАЛОСЬ** <br/> |Тесты со знаком для HRESULT ошибки.  <br/> |
   

