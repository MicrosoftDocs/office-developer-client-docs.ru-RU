---
title: Использование макросов для обработки ошибок
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
# <a name="using-macros-for-error-handling"></a>Использование макросов для обработки ошибок

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Существует несколько макросов, позволяющих упростить работу со значениями HRESULT.
  
Существует два набора макросов, которые проверяют наличие ошибок или успехов: HR_SUCCEEDED и HR_FAILED, а также успешно ВЫПОЛНЕНные и неудачные. SUCCEEDED — то же, что и HR_SUCCEEDED и отработка ОТКАЗа — то же самое, что и HR_FAILED.
  
В этом случае используйте макрос **ресултфромскоде** , чтобы присвоить переменной HRESULT СООТВЕТСТВУЮЩЕЕ значение HRESULT для S_OK. 
  
Часто используемые макросы кратко описаны в таблице ниже.
  
|**Macro**|**Описание**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Создает значение HRESULT из компонентов.  <br/> |
|**HR_SUCCEEDED** <br/> |Проверяет значение HRESULT для условия "успешно" или "предупреждение".  <br/> |
|**HR_FAILED** <br/> |Проверяет значение HRESULT для состояния ошибки.  <br/> |
|**HRESULT_CODE** <br/> |Извлекает часть кода ошибки HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Извлекает средство из HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Извлекает бит серьезности из СЕРЬЕЗНОсти.  <br/> |
|**ЗАКОНЧИЛ** <br/> |Проверяет значение HRESULT для условия "успешно" или "предупреждение".  <br/> |
|**СБОЕВ** <br/> |Проверяет значение HRESULT для состояния ошибки.  <br/> |
   

