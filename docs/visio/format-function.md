---
title: Функция FORMAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Возвращает результат выражения в виде строки, отформатированное в соответствии с formatpicture.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813821"
---
# <a name="format-function"></a>Функция FORMAT

Возвращает результат _выражения_ в виде строки, отформатированное в соответствии с _formatpicture_.
  
## <a name="syntax"></a>Синтаксис

ФОРМАТ (** *выражение* **, "** *formatpicture* **") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Строка** <br/> |Комбинация константы, операторы, функции и ссылки на ячейки таблицы свойств фигуры, которая приводит к значение.  <br/> |
| _formatpicture_ <br/> |Обязательный  <br/> |**Строка** <br/> |Формат рисунка используется для fomat строки.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Тип выражения и тип которых указан формат рисунка управляют поведением Возвращенная строка. _Formatpicture_ должен применяться в тип выражения. Дополнительные сведения о задании форматирование рисунков можно [о формате изображений](about-format-pictures.md).
  
Возвращает ошибку, если результат _выражения_ и типа в _formatpicture_ разного рода или при наличии синтаксических ошибок в _formatpicture_.
  
## <a name="example-1"></a>Пример 1

ФОРМАТ (1cm/4 "0.000 u")
  
Возвращает «0,250 см.»
  
## <a name="example-2"></a>Пример 2

ФОРМАТ (1cm/4 "0,00 U")
  
Возвращает «0,25 см.»
  
## <a name="example-3"></a>Пример 3

ФОРМАТ (1cm/4 "0.0 u")
  
Возвращает «0,3 см.»
  

