---
title: Функция Choose (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Возвращает элемент по указанному индексу из списка значений.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414118"
---
# <a name="choose-function-access-custom-web-app"></a>Функция Choose (пользовательское веб-приложение Access)

Возвращает элемент по указанному индексу из списка значений.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**Choose** (*IndexNumber*, *Value*, [*Value_n*]) 
  
Функция **Choose** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *IndexNumber*  <br/> |Integer expression that represents a 1-based index into the list of the items following it.  <br/> |
| *Значение*  <br/> |Список значений любого типа данных.  <br/> |
   
## <a name="remarks"></a>Примечания

Если предоставленный  *IndexNumber*  не является числом, то значение неявно преобразуется в одно или несколько. 
  
Если значение индекса превышает границы массива значений, **choose** возвращает значение NULL. 
  

