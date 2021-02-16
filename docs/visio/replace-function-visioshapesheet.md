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
description: Заменяет часть текстовой строки, основанную на количестве символов, на другую текстовую строку.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414356"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Заменяет часть текстовой строки, основанную на количестве символов, на другую текстовую строку.
  
## <a name="syntax"></a>Синтаксис

REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Обязательно  <br/> |**Строка** <br/> |Текст, в котором необходимо заменить некоторые символы.  <br/> |
| _start_num_ <br/> |Обязательна  <br/> |**Number** <br/> |Положение символа в  _old_text,_ который необходимо заменить  _на_ new_text . Первый символ в строке — позиция 1.  <br/> |
| _num_chars_ <br/> |Обязательна  <br/> |**Number** <br/> |Количество символов в  _old_text,_ которые необходимо заменить  <br/> |
| _new_text_ <br/> |Обязательно  <br/> |**Строка** <br/> |Текст, который будет заменять символы в _old_text._  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Используйте функцию REPLACE, чтобы заменить текст, который происходит в определенном расположении в текстовой строке. Если вы хотите заменить определенный текст в текстовой строке, используйте функцию SUBSTITUTE.
  
## <a name="example"></a>Пример

REPLACE ("01/03/2002",9,2,"03") 
  
Возвращает 03.01.2003. 
  

