---
title: BETWEEN (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Указывает диапазон для тестирования.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429301"
---
# <a name="between-access-custom-web-app"></a>BETWEEN (Доступ к настраиваемой веб-приложению)

Указывает диапазон для тестирования.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 *test_expression* [НЕ **]**  МЕЖДУ BEGIN_EXPRESSION **И** *END_EXPRESSION* 
  
Оператор **Between** содержит следующие аргументы. 
  
|**Аргумент**|**Обязательный**|**Описание**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Да  <br/> |Выражение, для проверки в диапазоне,  *определенном*  begin_expression и  *end_expression*  . Должен быть тот же тип данных, что *и begin_expression* *и end_expression.*  <br/> |
| Возвращает только термины, которые не включают операнд.  <br/> |Нет  <br/> |Указывает, что результат предиката будет отрицаться.  <br/> |
| *begin_expression*  <br/> |Да  <br/> |Допустимые выражения. Должен быть тот же тип данных, что *и test_expression* *и end_expression.*  <br/> |
| *end_expression*  <br/> |Да  <br/> |Допустимые выражения. Должен быть тот же тип данных, что *и test_expression* *и begin_expression.*  <br/> |
| *И*  <br/> |Да  <br/> |Указывает,  *test_expression*  должны быть в пределах диапазона,  *указанных*  begin_expression и  *end_expression*  .  <br/> |
   
## <a name="result-type"></a>Тип результатов

 **Boolean**
  
## <a name="remarks"></a>Примечания

 **МЕЖДУ** возвращает **ЗНАЧЕНИЕ TRUE,** если значение *test_expression* больше или равно значению begin_expression и меньше или равно  *значению end_expression* . 
  
 **НЕ МЕЖДУ** возвращает ЗНАЧЕНИЕ **TRUE,** если значение *test_expression* меньше  значения begin_expression или больше, чем *значение end_expression* . 
  
Чтобы указать эксклюзивный диапазон, используйте большее , чем () и меньше \> операторов ( \< ).
  

