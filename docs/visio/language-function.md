---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Позволяет сравнивать операции между различными языковыми представлениями. Он лучше всего используется для преобразования языковых тегов целевой группы интернет-инженерии (BCP 47) в значения локальных id (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424756"
---
# <a name="language-function"></a>LANGUAGE Function

Позволяет сравнивать операции между различными языковыми представлениями. Он лучше всего используется для преобразования языковых тегов целевой группы интернет-инженерии (BCP 47) в значения локальных id (LCID).
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **LANGUAGE** _(lcid_or_bcp47)_
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Обязательный  <br/> |**String** <br/> |Значение LCID или BCP 47 для языка.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="example"></a>Пример

 `LANGUAGE("en-us")`
  
Возвращает значение '1033'.
  
 `LANGUAGE("es-es")`
  
Возвращает значение "3082".
  

