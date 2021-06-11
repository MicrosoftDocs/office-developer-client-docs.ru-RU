---
title: Функция DEPENDSON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Создает зависимость от ссылок на ячейки.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423470"
---
# <a name="dependson-function"></a>Функция DEPENDSON

Создает зависимость от ссылок на ячейки.
  
## <a name="syntax"></a>Синтаксис

DEPENDSON(** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Обязательный  <br/> |**String** <br/> |Первая ссылка ячейки.  <br/> |
| _cellref2_ <br/> |Необязательный  <br/> |**String** <br/> |Вторая ссылка ячейки.  <br/> |
   
## <a name="remarks"></a>Примечания

Эта функция всегда возвращает FALSE. Это не влияет при его использования в строке Event или ячейке Action. 
  
## <a name="example"></a>Пример

OPENTEXTWIN() + DEPENDSON (PinX,PinY) 
  
Открывает текстовый блок для фигуры всякий раз, когда меняются ячейки PinX или PinY формы. 
  

