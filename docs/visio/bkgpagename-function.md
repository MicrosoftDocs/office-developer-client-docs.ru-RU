---
title: Функция BKGPAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Возвращает имя фоновой страницы в качестве строки.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410317"
---
# <a name="bkgpagename-function"></a>Функция BKGPAGENAME

Возвращает имя фоновой страницы в качестве строки.
  
## <a name="syntax"></a>Синтаксис

BKGPAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Используется для указания языка для строки, возвращаемой функцией. Используйте 0 (значение по умолчанию) для указания локального языка. Используйте 750 для указания универсального языка.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Если страница, для которой используется функция, не имеет фоновой страницы, возвращается строка \< "нет \> фона". 
  
Если вы передаете запрещенный код языка, используется локальный язык. 
  

