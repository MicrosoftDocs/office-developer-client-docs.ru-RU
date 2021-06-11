---
title: Функция SUBSTITUTE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Заменяет часть текстовой строки другой строкой текста.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346825"
---
# <a name="substitute-function"></a>Функция SUBSTITUTE

Заменяет часть текстовой строки другой строкой текста. 
  
## <a name="syntax"></a>Синтаксис

 SUBSTITUTE (** *text* **, ** *old_text* **, **** new_text ** [, *** start_num* ** ][, ** *ignore_case_opt* ** * * ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**String** <br/> | Текст или ссылка на ячейку, содержащую текст, для которого необходимо заменить символы.  <br/> |
| _old_text_ <br/> |Обязательный  <br/> |**String** <br/> | Текст, который необходимо заменить.  <br/> |
| _new_text_ <br/> |Обязательный  <br/> |**String** <br/> | Текст, который необходимо использовать для замены _old_text._  <br/> |
| _start_num_opt_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Указывает, какие случаи old_text заменить.  <br/> |
| _ignore_case_opt_ <br/> |Необязательный  <br/> |**Логический** <br/> |FALSE, если он чувствителен к делу; в противном случае TRUE. По умолчанию значение FALSE.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

 Если указать _start_num_opt,_ заменяется только _old_text._ В противном случае каждое  _old_text_  _в тексте_ меняется на  _new_text._
  
Используйте функцию SUBSTITUTE, когда необходимо заменить определенный текст в текстовой строке. Если вы хотите заменить текст, который происходит в определенном расположении в текстовой строке, используйте функцию REPLACE.
  
## <a name="example"></a>Пример

SUBSTITUTE ("1 января 2003 г.", "Январь", "JAN") 
  
Возвращает "1 JAN 2003". 
  
SUBSTITUTE ("1 января 2003 г.", "январь", "JAN") 
  
Возвращает "1 января 2003 года". Изменения не вносясь, так как текстовый поиск является конфиденциальным к делу. 
  

