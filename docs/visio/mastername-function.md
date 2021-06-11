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
description: Возвращает мастер-имя листа в качестве строки или возвращает строку "нет мастера", если на листе нет мастера.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414755"
---
# <a name="mastername-function"></a>Функция MASTERNAME

Возвращает мастер-имя листа в качестве строки или возвращает строку \< "нет мастера", если на листе нет \> мастера.
  
## <a name="syntax"></a>Синтаксис

MASTERNAME ([ ** *langID_opt* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Необязательный  <br/> |**Number** <br/> |Используйте для указания языка для строки, возвращаемой функцией. Для указания локального языка используйте значение 0 (значение по умолчанию). Используйте 750 для указания универсального языка.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Если вы передаете нелегальный языковый код, используется местный язык. 
  

