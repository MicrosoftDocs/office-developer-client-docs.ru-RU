---
title: Функция TRIM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Удаляет все пространство из текста, за исключением одного пространства между словами.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435721"
---
# <a name="trim-function"></a>Функция TRIM

Удаляет все пространство из текста, за исключением одного пространства между словами. 
  
## <a name="syntax"></a>Синтаксис

TRIM (** *текст* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**String** <br/> |Текст, из которого необходимо удалить пробелы.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Функцию TRIM можно использовать в тексте, полученном из другого приложения, которое может иметь нерегулярные интервалы.
  
## <a name="example"></a>Пример

TRIM ("1 января 2003 г.") 
  
Возвращает "1 января 2003 г.". 
  

