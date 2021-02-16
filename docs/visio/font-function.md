---
title: Функция FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Возвращает все значение уникального идентификатора шрифта, указанного по имени.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422175"
---
# <a name="font-function"></a>Функция FONT

Возвращает все значение уникального идентификатора шрифта, указанного по имени.
  
> [!NOTE]
> В большинстве случаев идентификатор шрифта определяется системой. Хотя шрифт остается установленным после использования в файле, функция **FONT** обеспечивает согласованный доступ к определенному шрифту в системах и версиях Visio. Рекомендуется использовать функцию **FONT** для назначения шрифтов, а не ссылаться непосредственно на идентификаторы шрифтов. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **FONT**( _"font_name_string"_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Обязательна  <br/> |**строка** <br/> |Имя шрифта.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="remarks"></a>Замечания

Если строка, font_name_string  *не*  соответствует известному шрифту, эта функция возвращает #VALUE! error. 
  
## <a name="example"></a>Пример

 `FONT("Calibri")`
  
Возвращает значение (4), представляющее уникальный ИД шрифта Calibri.
  

