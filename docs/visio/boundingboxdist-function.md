---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает единицу измерения указанной части ограничительной рамки фигуры.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428279"
---
# <a name="boundingboxdist-function"></a>Функция BOUNDINGBOXDIST

Возвращает единицу измерения указанной части ограничительной рамки фигуры. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXDIST (* * *index* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательный  <br/> |**Number** <br/> |Часть ограничительной рамки фигуры для измерения и возврата. Возможные значения приведены в разделе reMarks.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Number**
  
## <a name="remarks"></a>Примечания

 *Индекс* может принимать одно из следующих значений. 
  
|**Элемент**|**Значение**|
|:-----|:-----|
|Width  <br/> |нуль  <br/> |
|Height  <br/> |1,1  <br/> |
|Закрепление левого края до фигуры  <br/> |2  <br/> |
|Прикрепление фигуры к правому краю  <br/> |4  <br/> |
|Прикрепление фигуры к верхнему краю  <br/> |SP4  <br/> |
|По нижнему краю до фигуры контакта  <br/> |17:00  <br/> |
|Центр ограничительной рамки для PinX  <br/> |ICMPv6  <br/> |
|Центр ограничительной рамки для PinY  <br/> |см  <br/> |
   

