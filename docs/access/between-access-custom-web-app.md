---
title: МЕЖДУ (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Указывает диапазон, для тестирования.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806957"
---
# <a name="between-access-custom-web-app"></a>МЕЖДУ (приложение настраиваемых web Access)

Указывает диапазон, для тестирования.
  
> [!IMPORTANT]
> Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint. Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб. 
  
## <a name="syntax"></a>Синтаксис

 *test_expression*  [НЕ] **BETWEEN** *begin_expression* **AND** *end_expression* 
  
Оператор **между** содержит следующие аргументы. 
  
|**Аргумент**|**Обязательное**|**Описание**|
|:-----|:-----|:-----|
| *test_expression*  <br/> |Да  <br/> |Выражение для проверки в диапазоне, определенные в *begin_expression* и *end_expression* . Должен быть один и тот же тип данных, как *begin_expression* и *end_expression* .  <br/> |
| *NOT*  <br/> |Нет  <br/> |Указывает, что результат предиката должен быть инвертирован.  <br/> |
| *begin_expression*  <br/> |Да  <br/> |Допустимое выражение. Должен быть один и тот же тип данных, как *test_expression* и *end_expression* .  <br/> |
| *end_expression*  <br/> |Да  <br/> |Допустимое выражение. Должен быть один и тот же тип данных, как *test_expression* и *begin_expression* .  <br/> |
| *AND*  <br/> |Да  <br/> |Указывает, что *test_expression* должны находиться в диапазон, указанный в параметре *begin_expression* и *end_expression* .  <br/> |
   
## <a name="result-type"></a>Тип результата

 **Boolean**
  
## <a name="remarks"></a>Замечания

 **BETWEEN** возвращает **значение TRUE,** Если значение *test_expression* больше или равны значениям *begin_expression* и меньше или равно значению *end_expression* . 
  
 **МЕЖДУ не** возвращает **значение TRUE** , если значение *test_expression* меньше, чем значение *begin_expression* или больше, чем значение *end_expression* . 
  
Для указания исключительных диапазона, используйте больше, чем (\>) и меньше, чем операторы (\<).
  

