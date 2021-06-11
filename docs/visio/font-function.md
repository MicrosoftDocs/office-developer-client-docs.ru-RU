---
title: Функция FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Возвращает значение integer уникального идентификатора для шрифта, указанного по имени.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422175"
---
# <a name="font-function"></a>Функция FONT

Возвращает значение integer уникального идентификатора для шрифта, указанного по имени.
  
> [!NOTE]
> В большинстве случаев идентификатор шрифта является системным. Хотя шрифт остается установленным после использования в файле, функция **FONT** обеспечивает последовательный доступ к определенному шрифту в системах и версиях Visio. Рекомендуется использовать функцию **FONT** для назначения шрифтов, а не ссылаясь непосредственно на идентификаторы шрифтов. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **FONT** _(font_name_string)_
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Обязательный  <br/> |**строка** <br/> |Имя шрифта.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="remarks"></a>Замечания

Если строка,  *предусмотренная для font_name_string,*  не соответствует известному шрифту, эта функция возвращает #VALUE! ошибка. 
  
## <a name="example"></a>Пример

 `FONT("Calibri")`
  
Возвращает значение integer (4), представляющее уникальный ID для шрифта "Calibri".
  

