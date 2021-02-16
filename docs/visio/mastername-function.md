---
title: Функция MASTERNAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Возвращает имя хозяина листа в качестве строки или возвращает строку "no master", если на листе нет хозяина.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414755"
---
# <a name="mastername-function"></a>Функция MASTERNAME

Возвращает имя хозяина листа в качестве строки или возвращает строку "no master", если на листе нет \< \> хозяина.
  
## <a name="syntax"></a>Синтаксис

MASTERNAME ([ ** *langID_opt* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Необязательна  <br/> |**Number** <br/> |Используется для указания языка для строки, возвращаемой функцией. Используйте 0 (значение по умолчанию) для указания локального языка. Используйте 750 для указания универсального языка.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Если вы передаете запрещенный код языка, используется локальный язык. 
  

