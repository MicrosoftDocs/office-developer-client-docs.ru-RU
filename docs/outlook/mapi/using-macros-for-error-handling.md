---
title: Использование макроса для обработки ошибок
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435567"
---
# <a name="using-macros-for-error-handling"></a>Использование макроса для обработки ошибок

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Существует несколько макроса, которые упрощают работу со значениями HRESULT.
  
Существует два набора макросов, которые проверяют на сбой или успех: HR_SUCCEEDED и HR_FAILED и SUCCEEDED и FAILED. SUCCEEDED это то же, HR_SUCCEEDED и FAILED то же, что и HR_FAILED.
  
В этом случае используйте макрос **ResultFromScode,** чтобы установить для переменной HRESULT соответствующее значение HRESULT для S_OK. 
  
Часто используемые макрос кратко описаны в следующей таблице.
  
|**Macro**|**Описание**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Строит HRESULT из его компонентов.  <br/> |
|**HR_SUCCEEDED** <br/> |Проверяет HRESULT на успешное состояние или условие предупреждения.  <br/> |
|**HR_FAILED** <br/> |Проверяет HRESULT на состояние ошибки.  <br/> |
|**HRESULT_CODE** <br/> |Извлекает часть кода ошибки HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Извлекает объект из HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Извлекает степень серьезности из степени серьезности.  <br/> |
|**SUCCEEDED** <br/> |Проверяет HRESULT на успешное состояние или условие предупреждения.  <br/> |
|**FAILED** <br/> |Проверяет HRESULT на состояние ошибки.  <br/> |
   

