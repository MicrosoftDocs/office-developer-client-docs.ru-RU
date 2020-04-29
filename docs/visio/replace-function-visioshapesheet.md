---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Заменяет часть текстовой строки на заданное число символов другой текстовой строкой.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414356"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Заменяет часть текстовой строки на заданное число символов другой текстовой строкой.
  
## <a name="syntax"></a>Синтаксис

Replace (* * *old_text* * *, * * *start_num* * *, * * *num_chars* * *, * * *new_text* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Обязательный  <br/> |**String** <br/> |Текст, в котором нужно заменить некоторые символы.  <br/> |
| _start_num_ <br/> |Обязательна  <br/> |**Number** <br/> |Позиция символа в _old_text_ , который необходимо заменить на _new_text_. Первый символ в строке равен позиции 1.  <br/> |
| _num_chars_ <br/> |Обязательна  <br/> |**Number** <br/> |Число символов в _old_text_ , которые необходимо заменить  <br/> |
| _new_text_ <br/> |Обязательный  <br/> |**String** <br/> |Текст, который заменит символы в _old_text_.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Используйте функцию REPLACE, чтобы заменить текст, который находится в определенном месте в текстовой строке. Если вы хотите заменить определенный текст в текстовой строке, используйте функцию подстановки.
  
## <a name="example"></a>Пример

REPLACE ("01/03/2002", 9, 2, "03") 
  
Возвращает 01/03/2003. 
  

