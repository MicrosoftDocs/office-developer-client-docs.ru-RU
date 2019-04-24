---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Разрешает операции сравнения между различными представлениями языка. Его лучше всего использовать для преобразования значений тегов языка для задач проектирования через Интернет (BCP 47) в значения идентификатора языкового стандарта (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327820"
---
# <a name="language-function"></a>LANGUAGE Function

Разрешает операции сравнения между различными представлениями языка. Его лучше всего использовать для преобразования значений тегов языка для задач проектирования через Интернет (BCP 47) в значения идентификатора языкового стандарта (LCID).
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2013
 
  
## <a name="syntax"></a>Синтаксис

 **Language (язык** ) ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Обязательный  <br/> |**String** <br/> |Значение LCID или BCP 47 для языка.  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

Целое число
  
## <a name="example"></a>Пример

 `LANGUAGE("en-us")`
  
Возвращает значение "1033".
  
 `LANGUAGE("es-es")`
  
Возвращает значение "3082".
  

